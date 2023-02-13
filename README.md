# Polynomial Fit and Plot
This is a python script that performs polynomial fits and plots the results. It uses the numpy, pandas, scipy, sklearn, and matplotlib libraries.

## Input Data
The input data is a CSV file named Bx_Bc_data.dat_2.40_-4.95_5.80. It contains data for columns a, b, c, Z, ex_calc, ec_calc, exc_calc, ex_exact, ec_exact, exc_exact, ex_lda, ec_lda, and exc_lda.

## Data Pre-processing
The following operations are performed on the input data:

The data is read into a pandas dataframe using the pd.read_csv function.
The columns of the dataframe are named using the df1.columns attribute.
New columns are created: exc_exact-lda, exc_calc-lda, x, and exc_calc-exact.
The x column is calculated as the power of -1/3 of the values in the Z column.
The values in the newly created columns are calculated using the corresponding columns in the dataframe.
## Polynomial Fits
The following polynomial fits are performed:

A second degree polynomial fit is performed on the values of exc_exact-lda for the first 4 rows of the dataframe.
A second degree polynomial fit is performed on the values of exc_calc-lda for the next 4 rows of the dataframe.
A second degree polynomial fit is performed on the values of exc_calc-lda for the next 4 rows of the dataframe.
## Plotting
The following plots are generated:

A scatter plot of the values of exc_exact-lda for the first 4 rows of the dataframe. The points are colored green.
A scatter plot of the values of exc_calc-lda for the next 4 rows of the dataframe. The points are colored blue.
A scatter plot of the values of exc_calc-lda for the next 4 rows of the dataframe. The points are colored red.
A line plot of the polynomial fit performed on exc_exact-lda for the first 4 rows of the dataframe. The color is green and the line is labeled with (E_{xc}(exact)-E_{xc}(LDA))/Z.
A line plot of the polynomial fit performed on exc_calc-lda for the next 4 rows of the dataframe. The color is blue and the line is labeled with (E_{xc}(LSIC)-E_{xc}(LDA))/Z.
A line plot of the polynomial fit performed on exc_calc-lda for the next 4 rows of the dataframe. The color is red and the line is labeled with (E_{xc}(LSIC^+)-E_{xc}(LDA))/Z.
The r2_score is calculated for each of the polynomial fits and the
