# Data-driven real estate investment risk model
This repository contains, a folder containing input csv files, a folder containing results data, python codes carrying out specific task mentioned below, ipython notebooks going over the steps and execution and files associated with flask app.
* Clean and combine data For this project I combined data from multiple sources into one datatable. Also, I identify different markets on the basis of MSA (Metropolitan Statistical Area) code. All the Input data is saved in the '/Data' folder and after running the code Data_cleaning.ipynb a new cleaned datatable is generated, and is saved in file 'Input_data_market_risk_model'.
Adding new market data To add data of a new market first check if the MSA code for that market is present in the NCREIF property index data or not. You can look at Data cleaning ipython notebook for the list of MSA codes in NCREIF property index data. If the MSA code is listed then add following things to the '/Data' folder:
1.	To the excel file 'MSA_codes.xlsx', add MSA code, 'Market_name', for the Market by refering to the NCREIF manual.
2.	To the excel file 'HomeOwnershipRate.xlsx', add 'Market_name', for the Market.
3.	Add folder containing employment data, unemployment rate data and Costar data in folder '/Data/Market_name'. Save the files in '.xlsx' format and name them as '{Market}_Employment.xlsx', '{Market_name}_Unemployment.xlsx' and '{Market_name}_Costar.xlsx', respectively.
4.	Add population estimate data in folder /Data/MSAwise populationwise estimate'. Save the file in '.xlsx' format and name it '{Market_name}_PopEst.xlsx'.
Note: Keep the Market_name the same at all places as it is used in the codes.
* Model training and results Run the code Model_training.ipynb and quartiles of weights are generated for all markets individually and all markets combined. A table and a figure is saved in folders '/Results/Figure' and '/Results/Figure'.
* Flask app Once you run the code FLask_app.ipynb, following weblink is generated http://127.0.0.1:5000/. Copy and past the link in the web browser (incognito to avoid caching the result image). Also, clear the images in static/images folder after closing the app.
Here is the link to the video demo-ing the [app.](https://youtu.be/tNwAyyntD7U)
