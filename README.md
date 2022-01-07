- README.md includes concise summary of project with all data science steps
- README.md links to presentation and sources
- README.md includes instructions for navigating the repository
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

*The following repository content information is for the main branch only, other branches should be ignored*

### Overview 

Hasko, Heinzel & Viscarra is a real estate company that has been buying and selling residential properties in King County, Washington, for the past 25 years. Our company uses data to predict the value of your home. We specialize in helping people new to the area find homes. With over 2 million people, King County is the largest county in Washington State. It can be daunting for someone who is not familiar with the area to begin their home search. HH&V can save you time by locating the most likely places you’ll find a home with the features you want within your budget.

### Business Problem

There is no single variable that affects house price. Many different factors determine how much homes get sold for. What HH&V does is help you answer the most important questions in your home search:
- Which factors have the biggest effect on house price?
- How much does house size affect its price?
- Where should you buy a house?

We use data from historical home sales in King County to predict home price. Our dataset includes 21,597 homes sold between 2014–2015 and includes a number of variables about the homes being sold, such as the number of bathrooms, total square footage of living area, quality of construction materials, if it has a scenic view, and if the property is located by water. We supplemented this data with the median income per zip code in King County in order to better narrow down search radiuses.

Before constructing our models, we explored the data and preprocessed it. This included rounding numbers, replacing special characters with numbers, turning dates into date fields, and label-encoding the categorical data. We also had to deal with NaN values. We typically did this by replacing NaNs with the column median value where it made sense. For example, we changed the 2,353 missing values for waterfront to “No” because the vast majority of homes had a “No” value. We also corrected a house priced at $640,000 with 33 bathrooms. Since the number of bathrooms was mostly likely a data entry error, we changed the number of bathrooms to 3. This preprocessing cleaned up the data and prepared it for modeling.




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
