# Economic Data Analysis

## Importing

## jjjjj
```{r}
st <- sta[, 3:11] # Take numeric variables as goal matrix
library(ellipse) 
library(corrplot)
corMatrix <- cor(as.matrix(st)) # Calculate correlation matrix
col <- colorRampPalette(c("red", "yellow", "blue"))  # 3 colors to represent coefficients -1 to 1.
corrplot.mixed(corMatrix, order = "AOE", lower = "number", lower.col = "black", 
               number.cex = 1.2, upper = "ellipse",  upper.col = col(10), 
               diag = "u", tl.pos = "lt", tl.col = "black") # Mix plots of "number" and "ellipse"
```
![image](https://github.com/hayfordosmandata/hayfordosmandata.github.io/assets/120252752/217bd2fe-6e53-446a-8aed-c236a10afadd)


```{r}
row.names(st) <- sta$State
stars(st, key.loc = c(20, 0.5), draw.segments = T) 
```

![image](https://github.com/hayfordosmandata/hayfordosmandata.github.io/assets/120252752/3efd9d0a-9762-479d-a5d6-3ed1aaccc04a)

# hhhh
## jjj
