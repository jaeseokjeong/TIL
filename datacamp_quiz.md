## 1.

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
### Find unique rows of columns x and y
df %>% 
    distinct(x, y)

## 2.
semi_join(df1, df2, by = "customer_id")
semi_join ?


## 3. T/F일때, mean해주면 percentage

Following is a preview of the tibble trains: 
### A tibble: 20 x 3
      id cancelled delayed
   <chr>     <dbl>   <lgl>
 1   F28         0   FALSE
 2   I38        NA   FALSE
 3   J39         0   FALSE
 4   T21         1    TRUE
 5   T30         1    TRUE
 6   N20        NA    TRUE
 # ... with 14 more rows


output


### A tibble: 1 x 1
  dperc
  <dbl>
1   0.4

script

library(dplyr)
### Find the percentage of trains delayed
trains %>% 
    summarise(dperc = mean(delayed))
    
## 4. 내림차순 정렬

arrange(df, desc(x3))




