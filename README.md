## Getting and Cleaning data

Raw data
Tidy (processed) data

Code book

#Downloading files:

Knowing working directory is important when we are downloading the data

getwd()
setwd()

## Checking for and creating directories

file.exists("directory name")
dir.create("directory name")

Example :  if(!file.exists("data"))
            { dir.create("data")}
            
download.file()

important parameters: url, destfile, method
useful for : csv excel tab-delimited

##Reading local files

read.table() -- Reads data into RAM
file, header, sep, row.names, nrows, quote, na.strings, skip

read.csv(), read.csv2()

Example : cameradata <- read.table("./data/camera.csv", sep=",", header = TRUE)
            header(cameradata)


Example:  fileUrl <- ""
          download.file(fileUrl, destfile="./data/camera.csv", method="curl)
          list.files("./data")
          
##Reading JSON

library(jsonlite)
jsondata <- fromJSON("")
names(jsondata)

##data.table package

Inherits from data.frame package
Much much faster at subsetting, grouping and updating

library(data.table)

DF <- data.frame(x=rnorm(9), y=rep(c("a","b","c"), each=3), z=rnorm(9))
head(DF,3)

DT <- data.table(x=rnorm(9), y=rep(c("a","b","c"), each=3), z=rnorm(9))
head(DT,3)

