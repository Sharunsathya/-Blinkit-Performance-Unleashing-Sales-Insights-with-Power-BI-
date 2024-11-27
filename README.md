# -Blinkit-Performance-Unleashing-Sales-Insights-with-Power-BI-

## Project Description

This project focuses on analyzing Blinkit's sales performance, customer satisfaction, and inventory distribution through the power of data visualization and business intelligence using Power BI. The goal is to uncover key insights and opportunities for optimization by leveraging various KPIs and interactive visualizations.

### **Key Features:**
- **KPI Metrics**:
  - Total Sales
  - Average Sales
  - Number of Items Sold
  - Average Rating
- Interactive Dashboards with dynamic slicers
- Visualizations based on key metrics to assess sales performance, customer satisfaction, and inventory distribution

---

## **Steps for Building the Power BI Dashboard**

### 1. **Requirement Gathering / Business Understanding**
- **Objective**: Conduct a comprehensive analysis of Blinkit’s:
  - Sales performance
  - Customer satisfaction
  - Inventory distribution
  - Identify opportunities for optimization using KPIs and visualizations.
  
**Key KPIs to Track**:
  - Total Sales
  - Average Sales
  - Number of Items Sold
  - Average Rating

### 2. **Data Walkthrough**
- Load and explore the dataset in Power BI.
- **Objectives**:
  - Understand the dataset structure, including:
    - Column names
    - Data types
    - Missing or invalid data
  - Identify relationships and fields for calculated columns/measures.
  
**Example columns** to expect in the dataset:
  - Sales, Item Type, Fat Content, Outlet Size, Outlet Type, Rating, Outlet Establishment Year, etc.

### 3. **Data Connection**
- Import the dataset into Power BI.
  - **Source**: Excel, CSV, SQL Database, or any other data source.
  - Use **Home > Get Data** option to connect your data source.

### 4. **Data Cleaning / Quality Check (Power Query Editor)**
- **Steps**:
  1. **Remove Empty Rows/Columns**: Filter out unnecessary data.
  2. **Handle Missing Values**: Use data imputation or remove null values.
  3. **Change Data Types**: Ensure columns like Sales (Currency), Rating (Decimal), etc., are assigned correct data types.
  4. **Filter Data**: Keep relevant rows/fields.
  5. **Transform Columns**:
     - Extract Year from the establishment date.
     - Split concatenated fields if any.
  
- **Note**: Save these changes in the **Applied Steps** section.

### 5. **Data Modeling**
- **Steps**:
  1. Create relationships between tables (if applicable).  
     Example: Link **Sales** to **Outlet** and **Item Type**.
  2. Use **Star Schema** for efficient analysis.
  3. Define **Primary** and **Foreign Keys**.
  4. Ensure relationships are set to **One-to-Many** for better filtering.

### 6. **DAX Calculations**
- Write custom measures to calculate KPIs:
  - **Total Sales**:  
    ```DAX
    Total_sales = SUM('BlinkIT Grocery Data'[Sales])
    ```
  - **Average Sales**:  
    ```DAX
    Average_sales = AVERAGE('BlinkIT Grocery Data'[Sales])
    ```
  - **Number of Items Sold**:  
    ```DAX
    No_of_Items = COUNTROWS('BlinkIT Grocery Data')
    ```
  - **Average Rating**:  
    ```DAX
    Average_ratings = AVERAGE('BlinkIT Grocery Data'[Rating])
    ```

- **Steps to Add**:
  - Go to **Modeling > New Measure**.
  - Add the DAX formulas for each KPI.

### 7. **Dashboard Layout Setup**
- Go to **View > Canvas Settings**:
  - Height: 800px
  - Width: 1400px
  - Alignment: Middle
  - Background: White, Transparency: 40%
  
- **Style Customization**:
  1. Insert shapes (rounded tabs) for visual sections.
  2. Apply Blinkit’s brand color palette:
     - **Yellow**: `#FFD200`
     - **Green**: (Complementary tones)
  3. Add app branding:
     - Insert **Text Box**: Write "Blinkit" as the title (no background).
     - Align text and position appropriately.

### 8. **Charts Development**
**Charts and Objectives**:
  1. **Donut Chart (Total Sales by Fat Content)**:  
     - Add KPIs: Total Sales, Average Sales, Number of Items, Average Rating.
  2. **Bar Chart (Total Sales by Item Type)**:  
     - Analyze item performance.
  3. **Stacked Column Chart (Fat Content by Outlet)**:  
     - Compare total sales segmented by fat content.
  4. **Line Chart (Total Sales by Outlet Establishment Year)**:  
     - Evaluate how the outlet's age impacts sales.
  5. **Pie/Donut Chart (Sales by Outlet Size)**:  
     - Analyze sales distribution across outlet sizes.
  6. **Funnel Chart (Sales by Outlet Location)**:  
     - Assess geographic sales performance.
  7. **Matrix Card (All Metrics by Outlet Type)**:  
     - Provide a breakdown of KPIs by outlet types.

### 9. **Formatting Visuals**
- **Steps for Each Chart**:
  1. Add titles, legends, and data labels.
  2. Apply consistent colors (Yellow/Green tones).
  3. Resize visuals to fit within the layout grid.
  4. Set **Interactions** for cross-filtering between charts:  
     Format > **Edit Interactions > Filter**.

### 10. **Insights Generation**
- Analyze charts to derive actionable insights:
  - Identify trends (e.g., highest/lowest sales by outlet or fat content).
  - Highlight underperforming areas for improvement.

### 11. **Final Touches**
- **Slicers** for easy filtering:
  - Outlet Location, Outlet Size, Item Size.
  
- Adjust interactions between visuals.

- **Export and Publish the Dashboard**:
  - Save the file as `.pbix`.
  - Publish to **Power BI Service** for sharing.

---

### **Additional Notes:**
- Keep a **Metrics Slicer** to toggle between KPIs like Total Sales, Average Sales, etc.
- Use **Bookmarks** for switching between dashboard views.
- Perform a **Data Refresh Test** to ensure the dataset updates dynamically.

---

## Technologies Used
- **Power BI**
- **DAX (Data Analysis Expressions)**
- **Power Query Editor**
  
---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

