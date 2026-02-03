# Project Rubric

Use this rubric to understand and assess the project criteria.

---

## Part 1: Preparing the Environment

| Criteria | Submission Requirements |
|----------|------------------------|
| **1.1 Verifying Python and Jupyter Installations** | Both Python and Jupyter Notebook are installed and with the latest version. |
| **1.2 Installing Required Libraries** | Ensure the correct libraries (`datasets`, `pandas`, `matplotlib`, `seaborn`, and `pyarrow`) are installed. |

---

## Part 2: Downloading and Analyzing the Reviews Dataset

| Criteria | Submission Requirements |
|----------|------------------------|
| **2.2 Loading and Handling Large Datasets with a Sample Limit** | Load the Amazon Reviews dataset from Hugging Face and ensure the first 100 items are successfully loaded into a pandas DataFrame with a for loop that goes up to 100 and then breaks for the `reviews_dataset`. |
| | • Set the `sample_limit` to an integer value of **100** so that no more than 100 data items will be collected from the dataset |
| | • Create a for loop like you learned about from class so that you increment up to and including 100 data samples |
| | • Use boolean operators to set the missing `load_dataset` parameters to `True` |
| **2.3 Inspecting the Data** | Use `reviews_df.head()` to display the first few rows of the DataFrame. The data should display correctly with appropriate columns and rows. |
| **2.4 Customizing Data Output with an Integer Limit** | • Set the `Items_To_Print` value to an integer of **10** |
| | • Ensure an output of only the first 10 items of the DataFrame, overwriting Pandas' default output |

---

## Part 3: Metadata Dataset Analysis

| Criteria | Submission Requirements |
|----------|------------------------|
| **3.1 Loading Metadata Dataset** | • Set the `metadata_limit` to an integer value of **100** so that no more than 100 data items will be collected from the dataset |
| | • Create a for loop like you learned about from class so that you increment up to and including 100 data samples |
| | • Use boolean operators to set the missing `load_dataset` parameters to `True` |
| **3.2 Analyzing the Reviews Metadata Dataset with `.head()`** | Compare the Reviews and Metadata datasets by printing the column names and data types of both with the `.head()` method again to analyze the pandas dataframe. |
| **3.3 Safeguarding Data Access with Large Data Sets and Handling Exceptions** | • Review the items with and without a price |
| | • Finish the `get_product` lookup function by handling the exception case where the product title or price is not found using `try-except` blocks in order to return valid product prices or error messages for invalid inputs |

---

## Part 4: Cleaning and Preparing Data for Machine Learning

| Criteria | Submission Requirements |
|----------|------------------------|
| **4.1 Reviewing the columns of the datasets with `.columns`** | Leverage our pandas DataFrames several ways, such as looking at the columns in each dataset from the data objects we've created in `reviews_df` and `item_metadata_df` |
| **4.2 Creating a Loop to Output the Items in a List for Better Visibility** | Create a for loop to iterate over the two dataframes with the `.columns` method appended to them, so each dataframe can be outputted as a list. |
| **4.3 Create a Concise Summary of a DataFrame with `.info()`** | • Review the data types for each dataset with `.dtypes` and analyze the various types of data types as taught in the course |
| | • Print the info for the `reviews_df` DataFrame |
| | • Print the info for the `item_metadata_df` DataFrame |

---

## Part 5 & 6: Optimizing the Information for Data Visualization

| Criteria | Submission Requirements |
|----------|------------------------|
| **5.1 Clean the data for the requested parameters** | Create a new DataFrame called `top_products_df` with these parameters: |
| | • has a title |
| | • the average rating is greater than or equal to **4.5** |
| | • there is a value for the price |
| | • Specify the 3 columns we want in the new dataframe `item_metadata_cleaned_df` |
| | • Set the `average_rating_filter` variable to the correct **float** data type that is sought after in the instructions above |
| **5.3 Calculating the Percentage of Cleaned Data** | • Complete the function `calculate_percentage` to perform this calculation. Use your knowledge from the course to write a part-of-whole division equation. |
| | • Ensure to use the `return` keyword so that your `calculate_percentage` function returns the result. |
| **5.4 & 5.5 Package the dataset up for analysis** | In order to save our new dataset, package it up into a `.csv` file and a `.parquet` file for analysis of the outputs. |
| **5.6 Collecting the Top Rated Product Titles** | • Create an empty array called `top_rated_titles` which will be our list |
| | • Create a for loop to iterate over the `top_products_df` DataFrame and then use the `.append` method for the titles to add them to the `top_rated_titles` list |
| | • Print the results of the `top_rated_titles` list |

---

## Part 6: Visualizing the Data

| Criteria | Submission Requirements |
|----------|------------------------|
| **6.1 Map the distribution of Prices for Highly Rated Products as a Histogram Chart** | • Use the `top_products_df` dataframe for the histogram graph |
| | • Use the `price` column from the `top_products_df` |
| | • Use a boolean operator to set the missing `sns.histplot` parameter `kde` to `True` |
| **6.2 Map the distribution of Prices for Highly Rated Products as a Scatterplot Graph** | • Use the `top_products_df` dataframe for the scatterplot graph |
| | • Plot your graph with the `price` for the x axis and `average_rating` on the y axis |
| **6.4 Narrow down on the handful of products that will be most meaningful** | Specify a cutoff threshold for the results as **float** data type **4.7** |
| **6.5 Create a Dashboard of Your New Findings** | • Set the `highly_rated_products_df_cutoff` with the desired float threshold value |
| | • Update the `highly_rated_products_df` to use the `.sort_values` method like you learned in class |
| | • Fill in the code to display the new sorted DataFrame |
| | • Complete the code to create a scatterplot using Seaborn |

> ⚠️ **Important:** Be sure to complete the wrap up step to create a text output file of your answers to each question in the Notebook!

---

## Required Deliverables

Your project submission should consist of these **4 elements**:

| # | Deliverable |
|---|-------------|
| 1 | The Jupyter Notebook with your cell outputs included |
| 2 | The `user_inputs.txt` file with your answers to all reflection questions |
| 3 | The `top_products.csv` dataset |
| 4 | The `top_products.parquet` dataset |

---

## 🌟 Suggestions to Make Your Project Stand Out

### Extended Data Analysis
Students can personalize their project by performing additional analyses, such as clustering products based on price and rating or exploring further insights from the metadata. Consider how to use various types of loops to iterate over the big datasets and create either new data objects, or explore how the information can be consolidated, aggregated, or organized to add additional value to the project.

### Custom Visualizations
Students can create other types of visualizations, such as box plots or heatmaps, to provide further insight into the data. While the knowledge around data visualization will not be assessed during the PCEP exam, these skills are fantastic for presenting your Python competencies and skillsets during job interviews, or highlighting your work as part of your portfolio.

### Advanced Data Formats
Explore beyond the `.csv` and `.parquet` data formats to learn about how data can be formatted in various ways in Python, and what Python-specific APIs or SDKs can be used or leveraged to analyze the datasets you worked with in the project. Python is a data-focused programming language, so learning how to work with big datasets will be excellent skills to hone as you continue your work as a Python engineer.

### Real-World Use Cases
Relate the data findings to potential business use cases, such as optimizing product pricing based on customer reviews. Build out your portfolio project into one that expands upon these business optimization principles, which will demonstrate to you, a potential interviewer, or to anyone that stumbles upon your GitHub account or website that you can take business ideas and create code that ties it all together, gleans insights from business data, and can help solve problems companies like Transformational AI are struggling with.
