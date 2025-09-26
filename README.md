# Delivery Time Prediction

A machine learning project to predict delivery times for orders placed through Porter using Linear Regression. This project analyzes various factors that influence delivery time and builds a predictive model to optimize operational efficiency.

## Project Overview

The objective of this project is to build a regression model that predicts the delivery time for orders based on multiple input features such as:
- Items ordered
- Restaurant location
- Order protocol
- Availability of delivery partners
- Market conditions

## Dataset Features

The dataset contains the following key features:

| Field                     | Description                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------- |
| market_id                 | Integer ID representing the market where the restaurant is located                          |
| created_at                | Timestamp when the order was placed                                                         |
| actual_delivery_time      | Timestamp when the order was delivered (target variable)                                   |
| store_primary_category    | Category of the restaurant (e.g., fast food, dine-in)                                      |
| order_protocol            | Integer representing how the order was placed (e.g., via Porter, call to restaurant, etc.) |
| total_items               | Total number of items in the order                                                          |
| subtotal                  | Final price of the order                                                                    |
| num_distinct_items        | Number of distinct items in the order                                                       |
| min_item_price            | Price of the cheapest item in the order                                                     |
| max_item_price            | Price of the most expensive item in the order                                               |
| total_onshift_dashers     | Number of delivery partners on duty when the order was placed                               |
| total_busy_dashers        | Number of delivery partners already occupied with other orders                              |
| total_outstanding_orders  | Number of orders pending fulfillment at the time of the order                              |
| distance                  | Total distance from the restaurant to the customer                                          |

## Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook

### Required Libraries
Install the required dependencies using pip:

```bash
pip install pandas
pip install numpy
pip install scikit-learn
pip install matplotlib
pip install seaborn
pip install statsmodels
```

Or install all at once:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels
```

## Data Requirements

The project expects a CSV file named `porter_data_1.csv` containing the order data with the features described above.

## Usage

1. **Clone the repository:**
```bash
git clone https://github.com/Bhuvanshree922/delivery_time_prediction.git
cd delivery_time_prediction
```

2. **Install dependencies:**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn statsmodels
```

3. **Place your data file:**
   - Ensure `porter_data_1.csv` is in the project root directory

4. **Run the analysis:**
   - Open `LR_Delivery_Time_Prediction_Bhuvanshree.ipynb` in Jupyter Notebook
   - Execute the cells sequentially to run the complete analysis

## Project Structure

```
delivery_time_prediction/
├── LR_Delivery_Time_Prediction_Bhuvanshree.ipynb  # Main analysis notebook
├── README.md                                       # Project documentation
└── porter_data_1.csv                              # Dataset (not included)
```

## Data Pipeline

The project follows a structured data science pipeline:

1. **Data Loading** - Import the Porter delivery data
2. **Data Preprocessing and Feature Engineering** - Clean and prepare the data
3. **Exploratory Data Analysis** - Analyze patterns and relationships
4. **Model Building** - Develop Linear Regression model using scikit-learn and statsmodels
5. **Model Inference** - Evaluate model performance and make predictions

## Model Details

- **Algorithm:** Linear Regression
- **Libraries Used:** scikit-learn, statsmodels
- **Target Variable:** Delivery time (derived from created_at and actual_delivery_time)
- **Features:** Market ID, order characteristics, restaurant type, delivery partner availability, distance

## Key Insights

The model helps understand the key factors influencing delivery time:
- Number of available delivery partners
- Distance from restaurant to customer
- Order complexity (number of items)
- Market conditions and outstanding orders
- Restaurant category and order protocol

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a Pull Request

## Future Enhancements

- Implement additional regression algorithms (Random Forest, XGBoost)
- Add time-series analysis for delivery patterns
- Include weather and traffic data for improved predictions
- Develop a web application for real-time predictions
- Add automated model retraining pipeline

## Author

**Bhuvanshree922**

## Acknowledgments

- Porter for providing the delivery data
- The scikit-learn and pandas communities for excellent documentation and tools