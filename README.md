# assi6a
data <- read.csv("twitter1.csv")
print(data)
relation <- lm(likes~retweet)
print(summary(relation))
relation <- lm(likes~retwett)
# Give the chart file a name.
png(file = "linearregression.png")
# Plot the chart.
plot(y,x,col = "blue",main = "likes & retweet Regression",
abline(lm(likes~retweet)),cex = 1.3,pch = 16,xlab = "likes",ylab = "twitter")
# Save the file.
dev.off()
output:
lm(formula = y ~ x)
Residuals:
 Min 1Q Median 3Q Max 
-6.3002 -1.6629 0.0412 1.8944 3.9775 
Coefficients:
 Estimate Std. Error t value Pr(>|t|) 
(Intercept) -38.45509 8.04901 -4.778 0.00139 ** 
x 0.67461 0.05191 12.997 1.16e-06 ***
---
Signif. codes: 0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 3.253 on 8 degrees of freedom
Multiple R-squared: 0.9548, Adjusted R-squared: 0.9491 
F-statistic: 168.9 on 1 and 8 DF, p-value: 1.164e-06
#corelation
my_data <- read.csv(twitter1.csv)
my_data <- mtcars
head(my_data, 6)
library("ggpubr")
ggscatter(my_data, x = "likes", y = "retweet", 
 add = "reg.line", conf.int = TRUE, 
 cor.coef = TRUE, cor.method = "pearson",
 xlab = "likes", ylab = "retweets")
