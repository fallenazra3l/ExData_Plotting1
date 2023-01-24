# unzip and read data (downloaded 1/23/23/ at 2137 EST, link provided by rdpeng)
households <- read.table(unz("exdata_data_household_power_consumption.zip", 
                             filename = "household_power_consumption.txt"), 
                         sep=";", header = TRUE)

# subset values (select only the first two days of feb)
newData <- households[households$Date == "1/2/2007" | 
                        households$Date == "2/2/2007",]

# create a new variable storing all dates/times as single posixCT values
posixTime <- as.POSIXct(paste(newData$Date,newData$Time,sep=" "), 
                        format = "%d/%m/%Y %H:%M:%OS")

png(filename = "plot3.png", width = 480, height = 480, units = "px")