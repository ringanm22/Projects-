library(ggplot2)

x = floor(198 * dpois(1:8, 2.33)) + 1;x
z = c()
for(i in 1:8){
  y = rnorm(x[i], 0.4 *i, i*0.05)
  z = c(z,y)
}
df <-  as.data.frame(z)
ggplot(df, aes(z)) +
  geom_histogram(aes(y = ..density..),
                 colour = 1, fill = "light blue") +
  theme_minimal() +
  geom_density(adjust = 1/3, size = 1, col = "blue") +
  scale_x_continuous(breaks = seq(0, 3.8, 0.2), limits = c(0,3.6)) +
  geom_vline(xintercept = seq(0.4, 3.2, 0.4), size = 1, color = "red", linetype = "dashed")
