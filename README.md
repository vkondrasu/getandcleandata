# getandcleandata

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


Example:  fileUrl <- ""
          download.file(fileUrl, destfile="./data/camera.csv", method="curl)
          list.files("./data")

