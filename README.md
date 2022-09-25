### DIY Modelling
To run, download the RMD and both CSV files, and place in the same folder. Then run the RMD file.
/
/
/
/
/

For this project, I decided to dive deep into how different optimisation techniques worked, specifically looking at the Least Squares and Maximum Likelihood. The purpose of this is to better understand how different optimisation techniques are used to find the best estimates for a given model.

In R, we can use the default _lm_ function to model independent vs dependent variables which is fitted using the least squares criterion. In my project, I create two functions which manually produces the output of the _lm_ function, as well as find the standard errors and confidence intervals by bootstrapping. To evaluate the accuracy of my functions I compared these bootstrapped results with the standard output from _lm_.

As R uses least squares to calculate the estimates, I decided to write similar functions as above but use Maximum Likelihood as the optimisation method rather than Least Squares. 

I tested both the Least Squares and Maximum Likelihood estimators using the Climate dataset, and they produced similar estimates and standard errors as the _lm_ function in R.

Looking at the wombat dataset, I noticed that the relationship for the number of burrows and the number of wombats suited a poisson distribution. I used the MLE/Bootstrap code to reproduce the _glm_ function outputs and standard errors for a Poisson models, and compared them with the R function with (family = poisson) and (family = quasipoisson). The model produced outputs more similar to the quasipoisson model, which could be due to the assumptions for a poisson model to be not met.



