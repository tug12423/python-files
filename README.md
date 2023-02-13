# Polynomial Fit and Plot
This is a python script that performs polynomial fits and plots the results. This code is a data analysis script in python using the libraries numpy, pandas, scipy, sklearn and matplotlib.

## Input Data
The input data is a CSV file named Bx_Bc_data.dat_2.40_-4.95_5.80. It contains data for columns a, b, c, Z, ex_calc, ec_calc, exc_calc, ex_exact, ec_exact, exc_exact, ex_lda, ec_lda, and exc_lda.

## Method
The script starts by importing the necessary libraries. The data is then loaded into a pandas dataframe using the read_csv method. The data is read from a file named 'Bx_Bc_data.dat_2.40_-4.95_5.80', with a specified delimiter and with the 'python' engine. The columns in the data are then named.

Next, the script performs some calculations on the data and creates new columns. Three new columns are created with the difference between two energy values, and another two columns with the absolute value of the difference between two energy values divided by Z, where Z is a column in the data. The value of Z is also raised to the power of -1/3 and stored in a new column.

The script then fits a 2nd degree polynomial regression to three sets of data points using the np.polyfit method and stores the polynomial coefficients in separate variables (coeffs6, coeffs7, coeffs8). The resulting polynomials are stored in variables p6, p7, p8.

Next, the script uses the polynomials to make predictions and calculates the R-squared values using the r2_score method. The R-squared values are stored in variables r1squared, r2squared, and r3squared.

Finally, the script plots the original data points and the fitted polynomials. The polynomials are smoothed using the UnivariateSpline method and are plotted on the same graph with different colors and labels. The graph is labeled with the x and y axis labels, and the R-squared values are annotated on the plot.
