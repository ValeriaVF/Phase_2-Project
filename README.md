### Final Project Submission
- Students' names: Olgert Hasko, Sally Heinzel, Valeria Viscarra Fossati
- Students' pace: full time
- Scheduled project review date/time: 01/07/22 12:15 pm
- Instructor name: Skylar English
- Blog post URL:

## Real Estate Company Regression Models

### Repository Contents

Branches:
- main: contains finalized project notebooks, to be used by public
- Valeria: contains unorganized notebooks, not for public use
- olgerthasko: contains unorganized notebooks, not for public use
- sally: contains unorganized notebooks, not for public use

*The following repository content information is for the main branch only*

### Overview 

Hasko, Heinzel & Viscarra is a real estate company that has been buying and selling residential properties in King County, Washington, for the past 25 years. Our company uses data to predict the value of your home. We specialize in helping people new to the area find homes. With over 2 million people, King County is the largest county in Washington State. It can be daunting for someone who is not familiar with the area to begin their home search. HH&V can save you time by locating the most likely places you’ll find a home with the features you want within your budget.

### Business Problem

There is no single variable that affects house price. Many different factors determine how much homes get sold for. What HH&V does is help you answer the most important questions in your home search:
- Which factors have the biggest effect on house price?
- How much does house size affect its price?
- Where should you buy a house?

We use data from historical home sales in King County to predict home price. Our dataset includes 21,597 homes sold between 2014–2015 and includes a number of variables about the homes being sold, such as the number of bathrooms, total square footage of living area, quality of construction materials, if it has a scenic view, and if the property is located by water. We supplemented this data with the median income per zip code in King County in order to better narrow down search radiuses.

Before constructing our models, we explored the data and preprocessed it. This included rounding numbers, replacing special characters with numbers, turning dates into date fields, and label-encoding the categorical data. We also had to deal with NaN values. We typically did this by replacing NaNs with the column median value where it made sense. For example, we changed the 2,353 missing values for waterfront to “No” because the vast majority of homes had a “No” value. We also corrected a house priced at $640,000 with 33 bathrooms. Since the number of bathrooms was mostly likely a data entry error, we changed the number of bathrooms to 3. This preprocessing cleaned up the data and prepared it for modeling.

### Data Understanding

We used data provided to us (kc_house_data) as well as income by zipcode data that we got from kagle.com ([https://www.kaggle.com/miker400/washington-state-home-mortgage-hdma2016?select=Washington_State_HDMA-2016.csv](url)).

Once we read both datasets, we combined the datasets which resulted in 21,420 data points. From there we prepared our data to build our models.

First we ran functions to change date to a usable format and bin(ed) dateds into seasons. We also filtered our data by price so that we only worked with houses prices $100,000 to $1,500,000, we then filtered by bedrooms, bathrooms and sqft_living so that the houses we worked with has less than 7 bedrooms, less than 6 bathrooms, and were less than 8000 square feet. We did this after looking at box plots of each variable and seeing that outliers were present beyond those bounds.

Once our data was prepared we started fitting our dataframe intro different regression models.

### Conclusion & Recommendations

Potential homeowners have a multiplicity of factors to consider when purchasing a home. They should consider which features are most and least important to them. Our models can aid them in choosing which home features they need to compromise on in order to be able to afford the features that are most important to them. Our model can also help them find the largest home possible for their budget by telling them how much their price increases for every additional square foot added to their home, all other things held constant. Further, we recommend narrowing the home search by looking at the price per square foot of home based on location as well as the median income of zip codes. This will save time by allowing people to focus their home searches in areas that will yield the highest number of homes for sale within their budget.

For future next steps, one helpful route of inquiry would be to acquire more years of housing data. Currently, with data spanning less than 2 years, we have a limited view of how house prices may fluctuate over time. Getting more data over various years would strengthen our predictions.
Another additional area to examine is school districts. Often families pick homes based on the school districts in which they are in. Being able to offer clients information about the quality of nearby school districts when deciding on purchasing a home would be helpful information to filter choices.
Finally, we could consider a home’s location in relation to downtown Seattle or other popular attractions. For home buyers interested in living near or within walking distance to certain places, knowing how much prices homes change in relation to proximity would be a useful additional factor.



### Repository Structure
```

├── Notebooks: unorganized notebooks used to clean & analyze data and set up code for master notebook.
|   ├── data_clean.ipynb
|   ├── olgerthasko.ipynb
|   ├── olgerthasko_models.ipynb
|   ├── student.ipynb
|   ├── student-checkpoint.ipynb

├── Plots: pngs of plots
|   ├── pairplot.png
|   ├── prediction.png
|   ├── waterfront_yr_renovated.png

├── Outputs: pngs for model outputs
|   ├── high_error_preds.png
|   ├── prediction.png
|   ├── output.png

├── .gitignore
├──  Final.ipynb: organized project notebook for public use
├── README.md: includes summary of project with all data science steps, links to presentation and sources, instructions for navigating the repository

```
