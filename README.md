# Epsilon excel project (sales)

## Overview

This project involves the analysis of sales data using Excel. The raw data was cleaned, relationships were created between the tables, a calendar table was generated, and DAX calculations were implemented to derive various insights. 

## Data Sources

The project uses the following raw data sheets:

1. **Outlets.csv**  
    (OutletId, Outlet Name, Outlet Class, Outlet Type, Employee_Code, Employee_Name, Warehouse Code, Warehouse Name)

2. **Products.csv**  
    (Product ID, Product Code, Product Name, Category, Subcategory, Price)

3. **Reps List.xlsx**  
    (ID, rep_Name, Username, Role, ZONE, Distributor)

4. **Sales.xlsx**  
    (Date, rep data.ID, warehouses.Code, Outlet_Id, Product Code, Product Name, Quantity, Price_Per_Piece, Total Price, sales Cluster, product category, rep_name)

5. **Targets April 2021.xlsx**  
    (ID, Username, rep_Name, Region, Warehouse Name, Target, AC, actual sales, % of sales)

6. **Visits.xlsx**  
    (Warehouse Name, Sales Rep ID, rep_Name, Date, Classification, OutletId, Visit Starting Time, Visit Ending Time, duration of visit, related_duration)

7. **Warehouses.xlsx**  
    (Warehouse Name, Code, Region)

## Data Cleaning and Relationships

The data from the various sheets were cleaned to remove inconsistencies and errors. Relationships were established between the tables based on common fields to enable comprehensive analysis.

## Calendar Table

A calendar table was created to facilitate time-based calculations and analysis. This table includes fields for year, quarter, month, and other relevant date information.

## DAX Calculations

DAX (Data Analysis Expressions) calculations were implemented to derive various insights from the data. The following key analyses were performed:

### Sales by Category
| Row Labels | total_sales |
|------------|--------------|
| Detergent  | $171,523,816.18 |
| Shower gel | $9,356,973.53 |
| Soap       | $75,481,077.52 |
| **Grand Total** | **$256,361,867.23** |

![Sales by Category]

### Highest 5 Sales Reps
| Row Labels      | total_sales         |
|-----------------|---------------------|
| Amgad           | $29,139,597.08      |
| Baher           | $27,235,954.16      |
| Mohamed Hussein | $26,279,832.67      |
| Osama           | $24,906,027.21      |
| Rep 13          | $24,767,224.85      |
| **Grand Total** | **$132,328,635.97** |

![Highest 5 Sales Reps]

### Highest 5 Product Sales
| Row Labels                           | total_sales         |
|--------------------------------------|---------------------|
| Detergent 1L discounted 10%          | $94,880,925.72      |
| Detergent 500ml discounted 10%       | $22,166,956.99      |
| Detergent 50ml                       | $36,840,656.84      |
| Soap 165gm - Normal 4 pcs 4EGP Discount | $21,455,436.25 |
| Soap 165gm - Red 4 pcs 4 EGP Discount  | $15,337,769.65 |
| **Grand Total** | **$190,681,745.45** |

![Highest 5 Product Sales]

### Highest 5 Sales Per Outlets
| Row Labels | total_sales    |
|------------|-----------------|
| ماركت حسن  | $6,047,828.04  |
| بشرة خير    | $4,701,561.45  |
| مو صلاح    | $4,659,618.34  |
| منظفات      | $4,592,844.54  |
| كارمن       | $3,640,436.07  |
| **Grand Total** | **$23,642,288.44** |

![Highest 5 Sales Per Outlets]

### Count of OutletId
- Distinct Count of OutletId: 5166

### Overall Average of % of Sales for All Reps
| Average of % of Sales |
|-----------------------|
| 45.11%                |

### Target Comparison with Actual Sales
| rep name        | Sum of actual sales | Sum of Target   | Sum of % of sales |
|-----------------|---------------------|-----------------|--------------------|
| Amgad           | $175,000.00         | $330,000.00     | 53.03%             |
| Amgad Mohsen    | $110,000.00         | $175,000.00     | 62.86%             |
| Baher           | $190,000.00         | $490,000.00     | 38.78%             |
| Mohamed Hussein | $130,000.00         | $195,000.00     | 66.67%             |
| Omar            | $60,000.00          | $350,000.00     | 17.14%             |
| Osama           | $175,000.00         | $320,000.00     | 54.69%             |
| Rep 13          | $55,000.00          | $150,000.00     | 36.67%             |
| Rep 14          | $65,000.00          | $130,000.00     | 50.00%             |
| Thabet Ali      | $120,000.00         | $460,000.00     | 26.09%             |
| Yasser          | $200,000.00         | $400,000.00     | 50.00%             |
| أمير           | $175,000.00         | $420,000.00     | 41.67%             |
| محمد احمد      | $175,000.00         | $400,000.00     | 43.75%             |
| **Grand Total** | **$1,630,000.00**   | **$3,820,000.00** | **541.33%**        |

![Target Comparison]

### Order Size
| Row Labels       | total_sales       | Count of orders |
|------------------|-------------------|-----------------|
| Very Big Order   | $226,683,546.45   | 28281           |
| Big Order        | $12,844,300.73    | 18106           |
| Normal Order     | $8,772,113.54     | 27260           |
| Small Order      | $6,097,701.32     | 55803           |
| Very Small Order | $1,964,205.19     | 90344           |
| **Grand Total**  | **$256,361,867.23** | **219794**       |

![Order Size]

### Sales Details per Category
| total_sales    | Detergent      | Shower gel     | Soap          | **Grand Total** |
|----------------|----------------|----------------|---------------|-----------------|
| **2020 Q1**    | $31,246,085.18 | $4,805,819.15  | $19,757,160.69 | $55,809,065.02 |
| **2020 Q2**    | $26,261,945.58 | $2,459,954.27  | $19,276,415.90 | $47,998,315.75 |
| **2020 Q3**    | $34,687,903.04 | $631,186.16    | $18,194,542.89 | $53,513,632.09 |
| **2020 Q4**    | $37,827,335.17 | $462,571.71    | $8,978,418.66  | $47,268,325.54 |
| **2021 Q1**    | $35,143,855.01 | $794,958.01    | $7,900,370.52  | $43,839,183.54 |
| **2021 Q2**    | $6,356,692.20  | $202,484.23    | $1,374,168.86  | $7,933,345.29 |
| **Grand Total**| $171,523,816.18| $9,356,973.53  | $75,481,077.52 | $256,361,867.23 |

![Sales Details per Category]

### Sales Details per Region
| total_sales    | Cairo/Giza     | Delta          | Upper         | **Grand Total** |
|----------------|----------------|----------------|---------------|-----------------|
| **2020 Q1**    | $3,311,728.34  | $34,206,074.44 | $18,291,262.24 | $55,809,065.02 |
| **2020 Q2**    | $2,584,823.88  | $26,306,963.23 | $19,106,528.64 | $47,998,315.75 |
| **2020 Q3**    | $3,102,113.21  | $31,074,477.15 | $19,337,041.73 | $53,513,632.09 |
| **2020 Q4**    | $3,129,390.24  | $25,309,733.50 | $18,829,201.80 | $47,268,325.54 |
| **2021 Q1**    | $2,997,199.84  | $23,875,811.17 | $16,966,172.53 | $43,839,183.54 |
| **2021 Q2**    | $274,999.91    | $4,771,774.80  | $2,886,570.58  | $7,933,345.29 |
| **Grand Total**| $15,400,255.42 | $145,544,834.29| $95,416,777.52 | $256,361,867.23 |

![Sales Details per Region]

### Sales Details per Size
| total_sales     | Big Order     | Normal Order   | Small Order   | Very Big Order   | Very Small Order | **Grand Total** |
|-----------------|---------------|----------------|---------------|------------------|-------------------|-----------------|
| **2020 Q1**     | $2,192,503.64 | $1,315,586.75  | $887,622.52   | $51,181,726.49   | $231,625.62       | $55,809,065.02  |
| **2020 Q2**     | $2,395,638.93 | $1,589,865.73  | $1,055,667.63 | $42,728,578.64   | $228,564.82       | $47,998,315.75  |
| **2020 Q3**     | $2,815,084.21 | $1,872,169.11  | $1,287,718.83 | $47,159,362.24   | $379,297.70       | $53,513,632.09  |
| **2020 Q4**     | $2,535,701.70 | $1,835,307.49  | $1,316,226.45 | $41,077,910.27   | $503,179.63       | $47,268,325.54  |
| **2021 Q1**     | $2,433,522.39 | $1,811,883.22  | $1,288,493.30 | $37,785,855.29   | $519,429.34       | $43,839,183.54  |
| **2021 Q2**     | $471,849.86   | $347,301.24    | $261,972.59   | $6,750,113.52    | $102,108.08       | $7,933,345.29   |
| **Grand Total** | $12,844,300.73| $8,772,113.54  | $6,097,701.32 | $226,683,546.45  | $1,964,205.19     | $256,361,867.23 |

![Sales Details per Size]

### Sales Category per Year
| Values             | total_sales        |
|--------------------|--------------------|
| soap_2020          | $66,206,538.14     |
| soap_2021          | $9,274,539.38      |
| Detergent_2020     | $130,023,268.97    |
| Detergent_2021     | $41,500,547.21     |
| Shower gel 2020    | $8,359,531.29      |
| Shower gel 2021    | $997,442.24        |

![Sales Category per Year]

### Very Big Order per Rep
| Values             | total_sales        |
|--------------------|--------------------|
| rep 1 very big order sales | $23,697,520.78 |
| rep 2 very big order sales | $18,858,438.80 |
| rep 3 very big order sales | $14,217,375.96 |
| rep 4 very big order sales | $24,737,966.85 |
| rep 5 very big order sales | $13,221,981.05 |
| rep 6 very big order sales | $14,161,674.31 |
| rep 7 very big order sales | $21,812,452.65 |
| rep 8 very big order sales | $26,780,003.74 |
| rep 9 very big order sales | $11,807,690.06 |
| rep 10 very big order sales | $19,355,273.68 |
| rep 11 very big order sales | $22,197,737.35 |
| rep 12 very big order sales | $15,835,431.22 |

![Very Big Order per Rep]

## Conclusion

The analysis provides comprehensive insights into the sales data, highlighting key trends and performance metrics across different categories, regions, products, and sales representatives.

