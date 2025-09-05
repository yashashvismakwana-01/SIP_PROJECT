library(readr)
print(getwd())
setwd("C:/Users/Bhavika/Documents/R Language")

data=read.csv("bhavika.csv")
print(data)

# Read the CSV file
data <- read.csv("bhavika.csv")

# Display the first 20 records
head(data, 20)

#Display 5 record from bottom
data <- read.csv("bhavika.csv")
data[96:100, ]

#Display column impression and home
data <- read.csv("bhavika.csv")
data[c("Impressions", "From.Home")]

# Display the average of home column
data <- read.csv("bhavika.csv")
mean(data$From.Home)

# Display max of likes 
data <- read.csv("bhavika.csv")
max(data$Likes)

#Display min of likes
data <- read.csv("bhavika.csv")
min(data$Likes)

#display record of follows that have  more than  20 follows.
data <- read.csv("bhavika.csv")
data[data$Follows > 20, ]

#sort the data
data <- read.csv("bhavika.csv")
data[order(data$Likes), ]

#display the column of impression,  shares, comment,likes.
data <- read.csv("bhavika.csv")
data[c("Impressions", "Shares", "Comments", "Likes")]

#scattered chart.
data <- read.csv("bhavika.csv")
plot(data$Impressions, data$Likes)

data <- read.csv("bhavika.csv")
plot(data$Impressions, data$Likes,
     main = "Scatter Plot of Likes vs Impressions",
     xlab = "Impressions", ylab = "Likes",
     col = "blue")

#bar chart
data <- read.csv("bhavika.csv")
barplot(data$Likes[1:10])
barplot(data$Likes, col = rainbow(length(data$Likes)))

data <- read.csv("bhavika.csv")
barplot(data$Likes, col = "skyblue")

#pie chart
data <- read.csv("bhavika.csv")
values <- data$Shares[1:5]
labels <- paste("insta", 1:5)
pie(values, labels = labels, main = "Pie Chart of Shares", col = rainbow(5))

#histogram chart
data <- read.csv("bhavika.csv")
hist(data$Likes, col = "purple", main = "Histogram of Likes", xlab = "Likes")

#add all chart
# Load data
data <- read.csv("bhavika.csv")

# --- Bar Chart (Likes) ---
barplot(data$Likes[1:10],
        col = "skyblue",
        main = "Bar Chart of Likes (Top 10)",
        ylab = "Likes",
        names.arg = paste("insta", 1:10))

# --- Pie Chart (Shares) ---
shares <- data$Shares[1:5]
labels <- paste("Post", 1:5)
pie(shares,
    labels = labels,
    col = rainbow(5),
    main = "Pie Chart of Shares")

# --- Scatter Plot (Impressions vs Likes) ---
plot(data$Impressions, data$Likes,
     main = "Scatter Plot: Impressions vs Likes",
     xlab = "Impressions",
     ylab = "Likes",
     col = "blue",
     pch = 19)

# --- Histogram (Likes) ---
hist(data$Likes,
     col = "purple",
     main = "Histogram of Likes",
     xlab = "Likes",
     border = "black")
