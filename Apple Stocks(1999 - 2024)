# Name: Allswell Sam Obeng
# ALY6000 Project 4
# 1oth October 2024

cat("\014") # clears console
rm(list = ls()) # clears global environment
try(dev.off(dev.list()["RStudioGD"]), silent = TRUE) # clears plots
try(p_unload(p_loaded(), character.only = TRUE), silent = TRUE) 
# clears packages
options(scipen = 100) # disables scientific notion for entire R session
library(pacman)
p_load(tidyverse)

# Load necessary libraries
library(tidyverse)
library(lubridate)

## Data Inspection and Cleaning
# Loading the dataset
data <- read.csv("AAPL_stock_price.csv")

# Inspecting the first few rows
head(data)

# Checking the structure of the data
str(data)

# Converting 'Date' column to Date type
data$Date <- ymd(data$Date)

# Checking for missing values
sum(is.na(data))

## Data Analysis
# Calculate the daily percentage change in the 'Close Price'
data <- data %>%
  arrange(Date) %>%
  mutate(Daily_Returns = (Close.Price / lag(Close.Price) - 1) * 100)

# Display the first few rows with the new column
head(data)

## Data Analysis

# Calculate the daily percentage change in the 'Close Price'
data <- data %>%
  arrange(Date) %>%
  mutate(Daily_Returns = (Close.Price / lag(Close.Price) - 1) * 100)

# Display the first few rows with the new column
head(data)

## Data Visualizations
# Plot 1: Close Price Over Time
ggplot(data, aes(x = Date, y = Close.Price)) +
  geom_line(color = "blue") +
  labs(title = "Apple Stock Close Price Over Time",
       x = "Date", y = "Close Price (USD)") +
  theme_minimal()

# Plot 2: Trading Volume Over Time
ggplot(data, aes(x = Date, y = Volume)) +
  geom_line(color = "green") +
  labs(title = "Apple Stock Trading Volume Over Time",
       x = "Date", y = "Volume") +
  theme_minimal()

# Plot 3: Histogram of Daily Returns
ggplot(data, aes(x = Daily_Returns)) +
  geom_histogram(bins = 50, fill = "purple", alpha = 0.7) +
  labs(title = "Distribution of Daily Returns (%)",
       x = "Daily Returns (%)", y = "Frequency") +
  theme_minimal()

 ##Correlation Analysis
# Scatter plot to check correlation between Close Price and Volume
library(gridExtra)
p1 <- ggplot(data, aes(x = Volume, y = Close.Price)) +
  geom_point(color = "blue", alpha = 0.6) +
  geom_smooth(method = "lm", color = "red", se = FALSE) +
  labs(title = "Scatter Plot: Close Price vs. Volume",
       x = "Volume", y = "Close Price") +
  theme_minimal()
print(p1)

# Calculate correlation between Close Price and Volume
cor_value <- cor(data$Close, data$Volume, use = "complete.obs")
cat("Correlation between Close Price and Volume:", cor_value, "\n")

## Descriptive Statistics
# Summary statistics for numerical columns
summary(data)

# Calculate mean, median, and standard deviation of Daily Returns
mean_return <- mean(data$Daily_Returns, na.rm = TRUE)
median_return <- median(data$Daily_Returns, na.rm = TRUE)
sd_return <- sd(data$Daily_Returns, na.rm = TRUE)

cat(sprintf("Mean Daily Return: %.2f%%\n", mean_return))
cat(sprintf("Median Daily Return: %.2f%%\n", median_return))
cat(sprintf("Standard Deviation of Daily Returns: %.2f%%\n", sd_return))



