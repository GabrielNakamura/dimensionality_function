# dimensionality_function
Function to calculate the dimensionality of biodiversity based on evenness of eingenvalues obtained from a PCA, performed on a matrix M (communities described by metrics of biodiversity).
The function are performed accondingly to logic propposed by [Stevens and Tello 2014](http://onlinelibrary.wiley.com/doi/10.1111/geb.12192/abstract) to measure the dimensionality of biodiversity.

# arguments
inputs:

matrix.M= a matrix with communities in rows and values of metrics in columns; 

scale= logical argument, if TRUE the matrix.M will be standardized acordingly to the argument contained in methods, if FALSE no standardization is performed;

method= If scale= TRUE, method correspond to the type of standardization imposed to matrix.M. The arguments to be used are the same to be passed  to the argument method in function decostand() in vegan. Default argument is "standardize", where the metrics are standardized by zero mean and unit variance.

evenness= index of evenness to be applied in eingenvalues derived from PCA on matrix M. May be one of the following arguments: "Camargo" to calculate evenness based on Camargo's index; "Pielou" to calculate evenness based in Pielou's evenness or "both", to calculate both index

output:
numeric, with a value represent the degree of evenness based in one of the two index options or a list with length two containing the results of evenness based on the two option of indexes. The greater the index, greater the dimensionality of the set of communities described by matrix M. 
