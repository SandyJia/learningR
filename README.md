# learningR
The notes for learning R programming

# full.namesh= TRUE is very usefull when the working directory is not exact the one you want to open the .csv files
files1 <- list.files( path, full.names = TRUE)
read.csv(files1)

pollutantmean <- function(directory, pollutant, id=1:332){
	
	files <-list.files(directory, full.names=TRUE)
	filedata<-data.frame()
	for(i in id){
		
		filedata <- rbind(filedata, read.csv(files[i]))
	}
	mean(filedata[,pollutant], na.rm=TRUE)
}


for(i in 1 : 2){
	dat2<- data.frame()
	dat2 <-cbind(dat2,read.csv(testfile[i]))
}

pollutantmean <- function(directory, pollutant, id=1:332){
	
	files <-list.files(directory, full.names=TRUE)
	
	for(i in id){
		
		filedata <- read.csv(files[i])
	}
	mean(filedata[,pollutant], na.rm=TRUE)
}

files <-list.files("specdata", full.names=TRUE)
	
	for(i in 1:2){
		
		filedata <- read.csv(files[i])
		}

pollutantmean <- function(directory, pollutant, id=1:332){
	
	files <-list.files(directory, full.names=TRUE)
	
	for(i in id){
		filedata<-data.frame()
		filedata <- rbind(filedata, read.csv(files[i]))
	}
	mean(filedata[,pollutant], na.rm=TRUE)
}
	
# It's different that filedata<-data.frame() come out of the for() sentence or not. 
# filedata<- read.csv(files[i]) cannot save a series csv files in the filedata, a data.frame is needed.
