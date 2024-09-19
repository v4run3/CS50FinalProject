# DataDashBoard
a simple yet interactive web-based data dashboard built using Streamlit. The application allows users to upload a CSV file and provides several tools for data exploration, filtering, and visualization.

## Features

The dashboard provides a range of features, from data previews and summaries to advanced filtering and data visualization. Below is a detailed description of each component and its functionality

### Title and File Uploader

Upon launching the application, the user is greeted with a simple, intuitive interface that displays the title "DATA DASHBOARD" at the top. Directly beneath this title is a file uploader widget. This widget allows users to upload CSV files, which are the primary data source for the application. The file uploader is restricted to .csv files to ensure compatibility and smooth processing with pandas, a popular data analysis library in Python.

The user can select any CSV file from their local system using the file uploader. If no file is selected, the application displays a message stating "Waiting for file upload..." to indicate that the app is idle and awaiting user input.

### Reading and Previewing the Data

Once the user uploads a CSV file, the application reads the file using pandas' pd.read_csv() function, which loads the contents of the CSV file into a pandas DataFrame for further processing. The app provides a preview of the dataset by displaying the first five rows using the df.head() function. This preview allows users to quickly inspect the contents of the CSV file to ensure the data was loaded correctly.

The data preview is displayed under a subheader titled "Data Preview," providing a clear demarcation between different sections of the dashboard. This feature is especially useful for users working with large datasets, as it offers a quick way to view a sample of the data without scrolling through the entire file.

### Data Summary

In addition to providing a preview of the data, the application offers a summary of the dataset’s numerical columns under the subheader "Data Summary." The summary is generated using the df.describe() method from pandas, which returns a statistical summary of the dataset. This summary includes key metrics such as:

    Count: The number of non-missing values in each column.
    Mean: The average value of each numerical column.
    Standard Deviation: A measure of how spread out the values are from the mean.
    Min: The minimum value in each column.
    25th Percentile, 50th Percentile (Median), 75th Percentile: These represent the values at the respective quartiles, providing insight into the distribution of the data.
    Max: The maximum value in each column.

The statistical summary is especially useful for quickly understanding the distribution and range of values in the dataset, helping users identify potential outliers or trends without manually inspecting the data.

### Data Filtering

The dashboard includes a powerful data filtering feature that allows users to focus on specific subsets of the data. Under the subheader "Filter Data," users can select a column from the dataset using a dropdown menu. This dropdown is populated with the list of column names from the uploaded CSV file. Once the user selects a column, a second dropdown appears, which allows the user to choose from the unique values within the selected column.

After the user selects a column and value, the app filters the data to show only the rows where the selected column matches the chosen value. This filtered subset of data is displayed immediately below the dropdown menus, providing real-time feedback to the user.

This filtering feature is particularly useful when dealing with datasets that contain categorical variables. For instance, if the dataset contains sales data from multiple regions, the user can filter the data to show only sales from a specific region, allowing for more targeted analysis.

### Data Visualization

In addition to data filtering, the application includes a visualization feature that allows users to create bar charts based on the filtered dataset. Under the subheader "Plot Data," users can select two columns: one for the X-axis and one for the Y-axis. The dropdown menus for these columns are populated with the list of column names from the dataset.

Once the user has selected the X and Y columns, they can generate the bar chart by clicking the "Generate Plot" button. The bar chart is then displayed within the app, providing a visual representation of the data. The chart helps users quickly identify patterns, trends, or anomalies in the dataset. The chart is also dynamically updated based on the filtered data, meaning users can filter the dataset and immediately visualize the changes.

### Requirements

    Python 3.x
    Streamlit
    Pandas

You can install the required dependencies using the following command:

    pip install streamlit pandas
### Screenshots

![image](https://github.com/user-attachments/assets/7a9a9ff3-4772-4e26-bb4b-0c06b0551b84)
![image](https://github.com/user-attachments/assets/2ba3eef2-b06c-4877-987c-c4bc5b49f11e)
![image](https://github.com/user-attachments/assets/c9804ae9-2d71-4a30-a155-da53c7890641)




