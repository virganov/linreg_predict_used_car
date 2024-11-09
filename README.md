# Predicting Used Car Prices Using Regression
This project aims to predict the prices of used cars based on various factors such as manufacturer, production year, fuel type, gear box type, and wheel drive. The goal is to develop a data-driven approach to estimate fair prices for used cars, helping buyers and sellers set competitive and reasonable prices in the market.

## Project Overview
The project employs linear regression to analyze historical data of used cars. The goal is to build a regression model that estimates car prices based on several vehicle characteristics, providing a transparent tool for pricing decisions.

Dataset
The dataset used in this analysis contains the following columns:

ID: Unique identifier for each entry
Price: The price of the vehicle (target variable)
Levy: Tax or additional charges associated with the vehicle
Manufacturer: The brand or maker of the vehicle
Model: Specific model of the vehicle
Prod_year: Production or manufacturing year of the vehicle
Category: Type of vehicle (e.g., SUV, sedan)
Leather_interior: Indicates whether the vehicle has a leather interior (yes or no)
Fuel_type: Type of fuel (e.g., gasoline, diesel)
Engine_volume: Engine displacement or capacity
Mileage: Total distance the vehicle has traveled
Cylinders: Number of cylinders in the engine
Gear_box_type: Type of transmission (e.g., manual, automatic)
Drive_wheels: Drivetrain configuration (e.g., right-hand drive, left-hand drive)
Doors: Number of doors on the vehicle
Wheel: Information about the wheel
Color: Exterior color of the vehicle
Airbags: Total number of airbags
Hypothesis Testing
The project includes hypothesis testing to examine the relationship between car attributes and their prices. The hypotheses are as follows:

1. Manufacturer
H0: The average price of cars produced by TOYOTA is the same as the average price of cars produced by other manufacturers.
H1: The average price of cars produced by TOYOTA is higher than the average price of cars produced by other manufacturers.
2. Production Year (Prod_year)
H0: The average price of cars produced after 2010 is the same as the average price of cars produced before 2010.
H1: The average price of cars produced after 2010 is higher than the average price of cars produced before 2010.
3. Category
H0: The average price of cars in the Jeep category is the same as the average price of cars in other categories.
H1: The average price of cars in the Jeep category is higher than the average price of cars in other categories.
Other Hypotheses:
Leather interior, Fuel type, Gear box type, Wheel, and Airbags also undergo hypothesis testing, with the goal of identifying statistically significant differences in prices based on these factors.
Regression Model
A linear regression model was created to predict used car prices based on five predictors: Manufacturer, Prod_year, Fuel_type, Gear_box_type, and Wheel. The final regression equation is:

makefile
Copy code
y = 17,573.7 + 555.2 × (Prod_year) + β_Manufacturer + β_Fuel_type + β_Gear_box_type + β_Wheel
Where:

β_Manufacturer: Adjustments based on manufacturer (e.g., +3065.55 for Toyota, -1578.04 for Mercedes-Benz)
β_Fuel_type: Adjustments based on fuel type (e.g., -11662.08 for Hybrid, -7704.35 for Petrol)
β_Gear_box_type: Adjustments based on gearbox type (e.g., +8484.3 for Tiptronic, +2256.74 for Manual)
β_Wheel: Adjustment for wheel drive type (e.g., -2436.31 for Right-hand drive)
Model Evaluation
The model was evaluated using various techniques, including:

Logarithmic transformations on both the target variable and predictors to test if any improvements in R² could be achieved.
Hypothesis testing using t-tests to examine relationships between car features and prices.
