### Project Overview: Electric Vehicle Market Analysis for AtliQ Motors

#### Live Dashboard: [Live](https://app.powerbi.com/view?r=eyJrIjoiYmI2ZTY4MzMtY2UxNC00ZDBlLTlmODctYThkNGRjOGI0ZDU2IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)
#### Vedio Presentation Link: [Link](https://www.youtube.com/embed/3_pHC9RWLT4)

#### Objective:
The primary objective of this project is to conduct a detailed market study of the existing electric and hybrid vehicle market in India to support AtliQ Motors' expansion plans. This analysis aims to provide insights into market trends, consumer behavior, competitive landscape, and growth opportunities for AtliQ Motors' bestselling models. As a part of their expansion plans, they wanted to launch their bestselling models in India where their market share is less than 2%

#### Data Sources:
1. **electric_vehicle_sales_by_state.csv**: Contains monthly sales data of electric and total vehicles by state and vehicle category.
2. **electric_vehicle_sales_by_makers.csv**: Contains monthly sales data of electric vehicles by maker and vehicle category.
3. **dim_date.csv**: Contains date dimensions including fiscal year and quarter information.

#### Key Metrics and Calculations:
1. **Penetration Rate**:
   - **Formula**: Penetration Rate =  (Electric Vehicles Sold / Total Vehicles Sold) * 100
   - Indicates the adoption level of electric vehicles within specific regions or categories.

2. **Compound Annual Growth Rate (CAGR)**:
   - **Formula**:CAGR = [(Ending Value / Beginning Value) ** 1/n] -1
   - Measures the mean annual growth rate of electric vehicle sales over a specified period.
3. **Peneration Rate for 2022_24 Change** :
   -**Formula**:    ![image](https://github.com/user-attachments/assets/97e566b2-a681-40ca-abe0-eb456d3e0f6d)
4. **Projected EV Sales 2024:** ProjectedEVSales2024 = [SecondEndingValueStatesEV] * POWER(1 + [CAGR_statesEV22_23], 1)
5. **Projected EV Sales 2030:** ProjectedEVSales2030 = [CAGR2022_state]*POWER(1+[CAGR_statesEV],8)
6. **CAGR_State(Compound Anual Growth Rate State)**: CAGR_statesEV = CALCULATE(POWER(DIVIDE([CAGR2024_state],[CAGR2022_state],0),0.5)-1,ALL(dim_date))
7. **CAGR_Makers(Compound Anual Growth Rate Maker)**: CAGR_MakersEV = POWER(DIVIDE([CAGR2024_maker],[CAGR2022_maker],0),0.5) -1

#### Data Analysis:
1. **Market Trends**:
   - Analyze overall sales trends of electric vehicles by state and by maker.
   - Calculate the penetration rate for different states in Electric vehicle categories.
   - Identify top-performing states and makers in terms of EV sales.
   - Determine growth trends using CAGR.

2. **Competitor Analysis**:
   - Compare sales performance of different makers in the electric vehicle segment.
   - Analyze market share distribution among leading manufacturers.

3. **Consumer Behavior**:
   - Examine consumer preferences for 2-Wheeler vs. 4-Wheeler electric vehicles.
   - Identify regional variations in EV adoption.

4. **Policy and Infrastructure**:
   - Review the impact of government policies and incentives on EV sales.
   - Assess the availability and distribution of charging infrastructure.

#### Dashboard Design:
1. **Overview Page**:
   - **KPI Cards**: Gross Sales of Electric Vehicle and Total Vehicle sales in current year and previous year
   - **Donut Chart**: Distribution of 2-wheeler and 4 wheeler in (EV sales and vehicle category) / Compare Electric vehicle in Revenue get different year 2022_24 and 2023_24
   - **Bar Chart**: Top states by EV sales in fiscal Year.

2. **Trend Analysis**:
   - **Line Chart**: Quarterly by EV sales trend makers/ PenetrationRate %fiscal Year with State/ Month with Average Sales Electric vehicle .
   - **Ribbon Chart**: Makers Sales with Fiscal Year sold by EV vehicle
   - **Scatter Chart**: compare with Total Electric Vehicle vs Total Vehicle Sold in different State (And the category is 2-4Wheeler)

3. **Comparative Analysis**:
   - **Bar Chart**: Geographical distribution visual different Bar Chart different States ( different 2-4 wheeler)
   - **Map Visual**: State with different 2-4Wheeler EV sales 

4. **Metrixs Analys**:
   - **Matrix**: Create different Metrics table like state,makers are compare with different TV,TEV,PR%, CPR and CAGR_EV or total

#### Tools Used:
- **PowerBI**: For data visualization and dashboard creation.
- **DAX (Data Analysis Expressions)**: For calculating key metrics like Penetration Rate and CAGR.
- **PowerPoint**: For creating the final presentation.

### Next Steps:
1. **Data Preparation**: Load and clean the data in PowerBI.
2. **Dashboard Design**: Create the visualizations and arrange them logically in the dashboard.
3. **Interactivity**: Implement slicers and filters for an interactive experience.
4. **Presentation Preparation**: Compile the insights and visualizations into a PowerPoint presentation.

This comprehensive analysis will provide Bruce Haryali and AtliQ Motors with valuable insights into the Indian EV market, helping them make informed decisions about their expansion strategy.

### Data Model: 
![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/datamodel.png)  

### DashBoard Screenshot:
**1) Home**
![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/0%20Home.png)

**2)Dashboard 1**:
![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_1.png)

![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard%201.2.png)

![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_1.2.png)

![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_1.3.png)

![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_1.4.png)

**3) Dashboard 2**:
![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_2.png)

![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_2.2.png)

![image](https://github.com/dinesh6351/Electric_Vehicle_Market_Analysis_for_AtliQ_Motors/blob/main/Screenshot/Dashboard_2.3.png)
