# JointCSsurv
JointCSsurv (which stands for <ins>**Joint**</ins> model for <ins>**C**</ins>luster <ins>**S**</ins>ize and <ins>**surv**</ins>ival outcome) is a package that performs semiparametric estimation and inference for clustered interval-censored data with informative cluster size using the method proposed by Lee et al. (2022) <DOI: xx/xxxx>.

**JointCSsurv** relies on the R-packages stats, stabledist, numDeriv, MASS, which is hosted on CRAN.

# How to import the Functions
> install.packages("devtools")<br />
> library(devtools) <br /> 
> source_url("https://github.com/lcyjames/WeibullCMs/blob/845d70f953b0ce692536bfd928fc0c72165fb4a8/CoreFunctions.R?raw=TRUE")

# Functions
> wmcmEM(Yi, cen, X, Z, trace=FALSE, tolerance=10^{-4}) <br />
This is the estimation procedure of the Weibull Mixture Cure Model based on the EM algorithm.

> wnmcmEM(Yi, cen, X, Z, trace=FALSE, tolerance=10^{-4}) <br />
This is the estimation procedure of the Weibull Non-Mixture Cure Model based on the EM algorithm

Both functions take the arguments below:
>- Yi is a vector of the right censoring times, with size n 
>- cen is the corresponding censoring indicator with 1 being cases and 0 being censored, with size n
>- X is a covariate matrix for the incidence component with size n times the number of covariates
>- Z is a covariate matrix for the latency component with size n times the number of covariates; X and Z do not contain a column of 1 (i.e. no intercept is required); X can be completely, partially, or not different from Z.<br />
>- trace=FALSE by default. For tracking the converging path of the parameter estimation, set trace=TRUE 
>- tolerance is the converging criteria typically assigned to be 10^{-4}
