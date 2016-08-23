---
layout: page
---

## Demo2: Useful R functions for working with strings
Barry Grant &lt; <http://thegrantlab.org> &gt;


It is important to note that all strings in R are stored as vectors. For example both of the below are vectors of strings.

``` r
v1 <- c("A", "B", "C", "D", "E")
v2 <- "ABCDE"
v1
```

    ## [1] "A" "B" "C" "D" "E"

``` r
v2
```

    ## [1] "ABCDE"

The first vector **v1** has 5 elements (i.e values A to E) and is thus of length 5. The second vector **v2** has only one element and is of length 1:

``` r
length(v1)
```

    ## [1] 5

``` r
length(v2)
```

    ## [1] 1

To find out how many characters (i.e. letters) are in each element of a vector we can use the **nchar()** function:

``` r
nchar(v1)
```

    ## [1] 1 1 1 1 1

``` r
nchar(v2)
```

    ## [1] 5

> Note that the example **nchar(v1)** here shows that the **nchar()** function is vectorized - that is, it will operate on every element of our input vector without having to explicitly loop over these elements. This is a really cool feature of R!

The paste() function
--------------------

A particularly useful function is **paste()**, which constructs strings by “pasting” together the parts. The **paste()** function takes any number of arguments and concatenates them together using the separating string specified by the sep argument (which is a space by default). Like many of R’s functions, paste() is vectorized:

``` r
paste("chr", c(1:22, "X", "Y"), sep="")
```

    ##  [1] "chr1"  "chr2"  "chr3"  "chr4"  "chr5"  "chr6"  "chr7"  "chr8" 
    ##  [9] "chr9"  "chr10" "chr11" "chr12" "chr13" "chr14" "chr15" "chr16"
    ## [17] "chr17" "chr18" "chr19" "chr20" "chr21" "chr22" "chrX"  "chrY"

What do you think would happen with the following example?

``` r
paste(v1, 1)
```

    ## [1] "A 1" "B 1" "C 1" "D 1" "E 1"

How about these examples?

``` r
paste(v1, c(1:5))
```

    ## [1] "A 1" "B 2" "C 3" "D 4" "E 5"

``` r
paste(v1, c(1:3))
```

    ## [1] "A 1" "B 2" "C 3" "D 1" "E 2"

In the last example above, **paste(v1, c(1:3))** we see **recycling** in operation - in this case the shorter input vector got "recycled" until it matched the length of the longer input vector to produce our output. This is a feature, not a bug!

Pattern matching and replacement with grep() and sub()
------------------------------------------------------

The **grep()** function, like its UNIX namesake, is useful for finding matches within and between strings. Here are some simple examples:

``` r
x <- c("AGCTAG", "ATA", "GATCTGAG", "")
length(x)
```

    ## [1] 4

``` r
nchar(x)
```

    ## [1] 6 3 8 0

``` r
grep("AT",x)
```

    ## [1] 2 3

``` r
grep("AT[CG]",x)
```

    ## [1] 3

``` r
grep("AT[CG]",x, value=TRUE)
```

    ## [1] "GATCTGAG"

Unlike **grep()**, the related **regexpr(pattern, x)** function returns where in each element of x it matched pattern. If an element doesn’t match the pattern, regexpr() returns –1. For example:

``` r
regexpr("AT[CG]",x)
```

    ## [1] -1 -1  2 -1
    ## attr(,"match.length")
    ## [1] -1 -1  3 -1
    ## attr(,"useBytes")
    ## [1] TRUE

Note from the output here the pattern **AT\[CG\]** is not found in first, second and fourth element of the vector **x** but is found in the third element starting at the second character continuing for 3 characters.

The **sub()** function is useful for replacement of pattern matched segments of strings. For example:

``` r
sub("AT[CG]", "--barry--", x)
```

    ## [1] "AGCTAG"         "ATA"            "G--barry--TGAG" ""

If you want to match and replace more than the first occurrence of your pattern you will want to use the related **gsub()** function.

Extracting values from a string
-------------------------------

The final function essential to string processing in R is **strsplit(x, split)**, which splits string **x** by **split**. Like R’s other string processing functions, **strsplit()** supports optional *perl* and *fixed* arguments.

For example, if we had a string like *gene=LEAFY;locus=2159208;gene\_model=AT5G61850.1* and we wished to extract each part, we’d need to split by “;”:

``` r
y <- "gene=LEAFY;locus=2159208;gene_model=AT5G61850.1"
strsplit(y, ";")
```

    ## [[1]]
    ## [1] "gene=LEAFY"             "locus=2159208"         
    ## [3] "gene_model=AT5G61850.1"

Also, like all of R’s other string functions, **strsplit()** is vectorized, so it can process entire character vectors at once. Because the number of split chunks can vary, **strsplit()** always returns results in a list.
