# Assigment 2


This readme file explains how to use and implement the R script, Assignment2.R.

Lines beginning with the # symbol are comments. Furthermore, lines beginning with #> signify the output produced in response to the commands executed.


  #Steps:

  # Open the R script
  # replace the "filepath" with the directory in which the file is saved

source("filepath/Assignment2.R")

  # create a "square" matrix (because the program only handles square matrices)


  # create the matrix while calling makeCacheMatrix()

a <- makeCacheMatrix( matrix(c(1,2,12,13), nrow = 2, ncol = 2) );

summary(a);
  #>            Length Class  Mode    
  #> set        1      -none- function
  #> get        1      -none- function
  #> setinverse 1      -none- function
  #> getinverse 1      -none- function

a$get();
#>      [,1] [,2]
#> [1,]    1   12
#> [2,]    2   13

cacheSolve(a)
#> [,1]        [,2]
#> [1,] -1.1818182  1.09090909
#> [2,]  0.1818182 -0.09090909

  # the 2nd time we run the function,we get the cached value

cacheSolve(a)
#> getting cached data
#> [,1]        [,2]
#> [1,] -1.1818182  1.09090909
#> [2,]  0.1818182 -0.09090909

# Alternatively, the matrix can also be created after calling the makeCacheMatrix function without arguments.

# read the R script
# replace the "filepath" with the directory in which the file is saved

source("filepath/Assignment2.R")

# calling the makeCacheMatrix function without arguments

a <- makeCacheMatrix();
summary(a);
#>            Length Class  Mode    
#> set        1      -none- function
#> get        1      -none- function
#> setinverse 1      -none- function
#> getinverse 1      -none- function

# creating a square matrix

a$set( matrix(c(1,2,12,13), nrow = 2, ncol = 2) );
a$get();
#>      [,1] [,2]
#> [1,]    1   12
#> [2,]    2   13

cacheSolve(a)
#> [,1]        [,2]
#> [1,] -1.1818182  1.09090909
#> [2,]  0.1818182 -0.09090909

# the 2nd time we run the function, we get the cached value

cacheSolve(a)
#> getting cached data
#> [,1]        [,2]
#> [1,] -1.1818182  1.09090909
#> [2,]  0.1818182 -0.09090909
