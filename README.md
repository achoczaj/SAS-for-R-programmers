# *R to SAS cheatsheet* --- a collection of snippets

This list was written to help quickly translate R code to the equivalent in SAS.

```R
d = read.table(a=1)
```

```SAS
DATA d ;
  INPUT make $  mpg rep78 weight foreign ;
  CARDS;
  AMC     22 3 2930 0
  AMC     17 3 3350 0
  AMC     22 . 2640 0
  ```


