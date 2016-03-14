# *R to SAS cheatsheet* --- a collection of snippets

This list was created to quickly translate a R code to its equivalent in SAS.

I wrote these snippets to be as short as possible and to reflect my own coding style. There are many ways to skin a cat: you might know another way to write a similar code in R and SAS. Don't hesitate to drop me a line if you know a better way.

## Data loading

### Loading inline data

Typically copy and paste a few lines of data in CSV format.

##### R:
 
```R
d = read.table(sep=',', text='AMC   ,  22 ,3 ,2930 ,0
AMC   ,  17 ,3 ,3350 ,0
AMC   ,  22 , ,2640 ,0
Audi  ,  17 ,5 ,2830 ,1
Audi  ,  23 ,3 ,2070 ,1
BMW   ,  25 ,4 ,2650 ,1
Buick ,  20 ,3 ,3250 ,0
Buick ,  15 ,4 ,4080 ,0
Buick ,  18 ,3 ,3670 ,0
Buick ,  26 , ,2230, 0
Buick ,  20 ,3 ,3280 ,0
Buick ,  16 ,3 ,3880 ,0
Buick ,  19 ,3 ,3400 ,0')```


```SAS
DATA d;
INFILE CARDS DELIMITER = ',';
  INPUT make $  mpg rep78 weight foreign ;
  CARDS;
  AMC   ,  22 ,3 ,2930 ,0
  AMC   ,  17 ,3 ,3350 ,0
  AMC   ,  22 , ,2640 ,0
  Audi  ,  17 ,5 ,2830 ,1
  Audi  ,  23 ,3 ,2070 ,1
  BMW   ,  25 ,4 ,2650 ,1
  Buick ,  20 ,3 ,3250 ,0
  Buick ,  15 ,4 ,4080 ,0
  Buick ,  18 ,3 ,3670 ,0
  Buick ,  26 , ,2230, 0
  Buick ,  20 ,3 ,3280 ,0
  Buick ,  16 ,3 ,3880 ,0
  Buick ,  19 ,3 ,3400 ,0
  ;
```
