# Understanding Consumer Segmentation Using Machine Learning

This project aims to understand customer segments using clustering and RFM Score analysis. It helps businesses target their customers better by identifying valuable customer groups based on their purchasing behavior.

## Objective

To identify and segment customers based on their purchasing patterns using:
- RFM Score
- K-Means Clustering

## Project Structure

- `Code.ipynb`: Main Jupyter Notebook containing all steps from data preprocessing to clustering.
- `Final_Customer_Segmentation.csv`: Final customer segmentation result using K-Means clustering.
- `Final_Customer_Segmentation_RFM_score.csv`: Final RFM scores used for customer segmentation.
- `requirements.txt`: List of Python packages required to run this project.

## Dataset
The dataset used in this project is the **Online Retail Dataset**, which contains transactional data from an online retail store. It includes the following columns:
- **InvoiceNo**: A 6-digit integral number uniquely assigned to each transaction. Starting letter 'c' indicates a cancellation.
- **InvoiceDate**: The day and time when each transaction was generated.
- **CustomerID**: A 5-digit integral number uniquely assigned to each customer.
- **StockCode**: Product (item) code. A 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name.
- **Quantity**: The number of units of the product purchased.
- **UnitPrice**: The price per unit of the product.
- **Country**: The name of the country where each customer resides.

##  Workflow

1. **Data Preprocessing**
   - Removed missing values and duplicates
   - Filtered out transactions with negative quantities (`Quantity < 0`)
   - Removed transactions from **December 2011**
   - Excluded cancelled transactions (those with `Invoice` containing 'C')
   - Removed outliers from data

2. **Feature Engineering**
   - Calculated Recency, Frequency, and Monetary values for each customer\
   - Performed log transformation to reduce skewness
  
3. **Exploratory Data Analysis (EDA)**:
   - Visualize distributions of `Quantity` and `UnitPrice`.
   - Analyze skewness in RFM metrics and apply log transformation.
   - Pair Plot of Recency, Monetary and Frequency
   - Performed log transformation and handled skewness
   - 3D Plot of Recency, Frequency, and Monetary

4. **RFM Scoring**
   - Quantile-based scoring for RFM attributes
   - Combined scores to segment customers

5. **Clustering**
   - Normalized data
   - Used Elbow method and Silhouette Score to determine optimal clusters
   - Applied K-Means clustering

6. **Results**
   - Customers are categorized into different clusters (segments) based on behavior
   - CSVs of segmentation are generated for further analysis or visualization

## Outputs

- `Final_Customer_Segmentation.csv`: Includes customer ID and their cluster label.
- `Final_Customer_Segmentation_RFM_score.csv`: By RFM scores, segmentation label.

## Dependencies
The project requires the following Python libraries:

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- scipy

## Acknowledgments
- **Dataset**: UCI Machine Learning Repository
- **Inspiration**: RFM analysis and customer segmentation techniques


