# *R to SAS cheatsheet* --- a collection of snippets

This list was written to help quickly translate R code to the equivalent in SAS.

<pre><code class='language-r'>d = read.table(a=1)


<pre><code class='language-r'>DATA d ;<br/>  INPUT make $  mpg rep78 weight foreign ;<br/>  CARDS;<br/>  AMC     22 3 2930 0<br/>  AMC     17 3 3350 0<br/>  AMC     22 . 2640 0<br/></code></pre>


