# myRmdTemplates

My R Markdown template 

* pdf_ja: Japanese PDF template using XeTeX (XeLaTeX)
* slide-xaringan: Presentation slide using xaringan

## Using `slide-xaringan`
To use `slide-xaringan`:

```
devtools::install_github("yihui/xaringan")
devtools::install_github("gadenbuie/xaringanthemer")
```

To run `slide-xaringan` offline: 

1. Locate `remark-latest.min.js` and `MathJax.js`
```r
xaringan::summon_remark(version = "latest", to = "libs/")
# Windows
file.copy(from="C:/Program Files/RStudio/resources/mathjax-26/MathJax.js", to="libs/")
```
1. Modify YAML front matter
```YAML
output: 
  xaringan::moon_reader:
    chakra: "libs/remark-latest.min.js"
    mathjax: "libs/mathjax-26/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
```

To convert `slide-xaringan` HTML to PDF: 

1. Install [decktape](https://github.com/astefanutti/decktape) and 
```
decktape remark url filename
```

### Install decktape

1. (Install Node.js)
1. Install Python 2.7
1. Install Windows visual C++ build tool 2015
1. config: 
```
npm config set python C:\python27\python.exe
npm config set msvs_version 2015
```
1. Insatall decktape
```
npm -g install decktape
```
