# Normalization vs. Standardization

**Standardization** is a subset of normalization where we subtract mean and divide by std. This is also called the z-score.

**Normalization** commonly include the following methods:

- **z-score** (or *standardization* as mentioned above)

  $z_i = \frac{x_i - \bar{x} }{\sigma} $

- **rescaling** data to values between 0 and 1

  $x_{new} = \frac{x - x_{min} }{x_{max} - x_{min}}$

- **Standardizing residuals**: used in regression analysis to force residuals into the shape of a normal distribution.

- **Normalizing Moments**: using the formula μ/σ.

- **Normalizing vectors** to a norm of one. This means to transform a vector so that it has a length of one.

(source: https://www.statisticshowto.datasciencecentral.com/normalized/)