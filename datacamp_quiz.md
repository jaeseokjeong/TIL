1.
Following is a preview of the data frame df: 
  x y  z
1 A P  7
2 A P  8
3 B P  9
4 B P 10
5 A Q 11
6 B Q 12


output


  x y
1 A P
2 B P
3 A Q
4 B Q



script

library(dplyr)
# Find unique rows of columns x and y
df %>% 
    distinct(x, y)

2.
semi_join(df1, df2, by = "customer_id")
semi_join ?

