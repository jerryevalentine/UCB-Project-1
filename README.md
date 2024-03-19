# UCB-Project-1

## Data Source ##
https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data?resource=download

## Datasets ##

### Prefered dataset ###
- We will first need to determine the feasibility of using the car sales dataset.
- Need to check for nulls and use regular expressions to search for any garbage (corrupt data, data that should not be in the cell, etc.).  If the car sales is not appropriate then we will evaluate the credit card fraud dataset.
- Note the dataset has a 10 usability score, which I believe is the highest.  This notebook is for due dillegence and also providing the metadata for the dataset.

-https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data/data

-https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction

## Criteria for inclusion: ##
-Sufficiently large (558,837 records)
-Loads in about 15 seconds on mny computer
-11% of the Transmission records are null

-https://www.kaggle.com/code/yusupibrahim/selling-price-predic-with-stacked-gen-r2-0-96 provides good example code

## Kaggle Data Card ##

About Dataset

Dataset Description:
The "Vehicle Sales and Market Trends Dataset" provides a comprehensive collection of information pertaining to the sales transactions of various vehicles. This dataset encompasses details such as the year, make, model, trim, body type, transmission type, VIN (Vehicle Identification Number), state of registration, condition rating, odometer reading, exterior and interior colors, seller information, Manheim Market Report (MMR) values, selling prices, and sale dates.

Key Features:
Vehicle Details: Includes specific information about each vehicle, such as its make, model, trim, and manufacturing year.

Transaction Information: Provides insights into the sales transactions, including selling prices and sale dates.

Market Trends: MMR values offer an estimate of the market value of each vehicle, allowing for analysis of market trends and fluctuations.

Condition and Mileage: Contains data on the condition of the vehicles as well as their odometer readings, enabling analysis of how these factors influence selling prices.

Potential Use Cases:

Market Analysis: Researchers and analysts can utilize this dataset to study trends in the automotive market, including pricing fluctuations based on factors such as vehicle condition and mileage.

Predictive Modeling: Data scientists can employ this dataset to develop predictive models for estimating vehicle prices based on various attributes.

Business Insights: Automotive industry professionals, dealerships, and financial institutions can derive insights into consumer preferences, market demand, and pricing strategies.

Format: The dataset is typically presented in tabular format (e.g., CSV) with rows representing individual vehicle sales transactions and columns representing different attributes associated with each transaction.

Data Integrity: Efforts have been made to ensure the accuracy and reliability of the data; however, users are encouraged to perform their own validation and verification processes.

Update Frequency: The dataset may be periodically updated to include new sales transactions and market data, providing fresh insights into ongoing trends in the automotive industry.


Car attribute columns that will be merged with car prices (shown above)
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 70823 entries, 0 to 70822
Data columns (total 79 columns):
 #   Column                                    Non-Null Count  Dtype  
---  ------                                    --------------  -----  
 0   id_trim                                   70823 non-null  int64  
 1   make                                      70823 non-null  object 
 2   model                                     70823 non-null  object 
 3   Generation                                70819 non-null  object 
 4   Year_from                                 70586 non-null  float64
 5   Year                                      70189 non-null  float64
 6   Year_to                                  70823 non-null  object 
 7   Series                                    70823 non-null  object 
 8   Trim                                      52252 non-null  object 
 9   Body_type                                 3363 non-null   object 
 10  load_height_mm                            64696 non-null  object 
 11  number_of_seats                           64660 non-null  object 
 12  length_mm                                 64660 non-null  object 
 13  width_mm                                  64660 non-null  object 
 14  height_mm                                 64660 non-null  object 
 15  wheelbase_mm                              49473 non-null  object 
 16  front_track_mm                            49473 non-null  object 
 17  rear_track_mm                             53710 non-null  object 
 18  curb_weight_kg                            8236 non-null   object 
 19  wheel_size_r14                            39670 non-null  object 
 20  ground_clearance_mm                       13171 non-null  object 
 21  trailer_load_with_brakes_kg               23799 non-null  float64
 22  payload_kg                                11198 non-null  float64
 23  back_track_width_mm                       11204 non-null  float64
 24  front_track_width_mm                      10523 non-null  object 
 25  clearance_mm                              39682 non-null  float64
 26  full_weight_kg                            6357 non-null   object 
 27  front_rear_axle_load_kg                   42729 non-null  object 
 28  max_trunk_capacity_l                      3337 non-null   object 
 29  cargo_compartment_length_width_height_mm  2235 non-null   object 
 30  cargo_volume_m3                           45953 non-null  float64
 31  minimum_trunk_capacity_l                  59598 non-null  object 
 32  maximum_torque_n_m                        57680 non-null  object 
 33  injection_type                            1 non-null      object 
 34  overhead_camshaft                         59544 non-null  object 
 35  cylinder_layout                           59544 non-null  float64
 36  number_of_cylinders                       6538 non-null   object 
 37  compression_ratio                         59878 non-null  object 
 38  engine_type                               59334 non-null  float64
 39  valves_per_cylinder                       23498 non-null  object 
 40  boost_type                                51354 non-null  float64
 41  cylinder_bore_mm                          51346 non-null  float64
 42  stroke_cycle_mm                           6625 non-null   object 
 43  engine_placement                          5 non-null      object 
 44  cylinder_bore_and_stroke_cycle_mm         59498 non-null  object 
 45  turnover_of_maximum_torque_rpm            7620 non-null   float64
 46  max_power_kw                              12830 non-null  object 
 47  presence_of_intercooler                   59837 non-null  object 
 48  capacity_cm3                              59877 non-null  float64
 49  engine_hp                                 59408 non-null  object 
 50  engine_hp_rpm                             59872 non-null  object 
 51  drive_wheels                              2 non-null      object 
 52  bore_stroke_ratio                         58292 non-null  float64
 53  number_of_gears                           40708 non-null  float64
 54  turning_circle_m                          59842 non-null  object 
 55  transmission                              40566 non-null  float64
 56  mixed_fuel_consumption_per_100_km_l       33987 non-null  object 
 57  range_km                                  22232 non-null  object 
 58  emission_standards                        57847 non-null  object 
 59  fuel_tank_capacity_l                      40181 non-null  float64
 60  acceleration_0_100_km/h_s                 43074 non-null  object 
 61  max_speed_km_per_h                        39043 non-null  float64
 62  city_fuel_per_100km_l                     1829 non-null   float64
 63  CO2_emissions_g/km                        58715 non-null  object 
 64  fuel_grade                                38769 non-null  float64
 65  highway_fuel_per_100km_l                  59454 non-null  object 
 66  back_suspension                           59405 non-null  object 
 67  rear_brakes                               59799 non-null  object 
 68  front_brakes                              59800 non-null  object 
 69  front_suspension                          2 non-null      object 
 70  steering_type                             11765 non-null  object 
 71  car_class                                 12365 non-null  object 
 72  country_of_origin                         13124 non-null  float64
 73  number_of_doors                           1012 non-null   object 
 74  safety_assessment                         1012 non-null   object 
 75  rating_name                               15 non-null     object 
 76  battery_capacity_KW_per_h                 15 non-null     float64
 77  electric_range_km                         7 non-null      object 
 78  charging_time_h                           0 non-null      float64