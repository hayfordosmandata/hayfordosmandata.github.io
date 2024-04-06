

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
