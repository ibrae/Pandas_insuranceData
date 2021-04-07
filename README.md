# insuranceData

# 1. import all the libraries needed in this project
- import pandas as pd
- import seaborn as sns
- import matplotlib.pyplot as plt
# Import the csv file to pandas to read data
- df = pd.read_csv("chidata_for_assignment_5.csv")
- df

# Display columns in the data set
- df.columns
# Generates a count plot for Insurance
- insurance_count = sbn.countplot(x="Insurance", data=df)
#add title
- insurance_count.set_title("Insurance Distribution.")
# Contigency cross table of the two data fields
- contigency = pd.crosstab(df.Gender, df.Insurance, margins = True, margins_name="Totals") 
- contigency
# Create a heatmap fo the contingency cross table
- gender_count = sbn.heatmap(contigency)
- gender_count.set(title=" Jubilee customers Insurances ", xlabel="Gender", ylabel="Status")
