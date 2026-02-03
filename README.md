Programming with Data Midterm Project


DATA SOURCES:
A total of 3 sources is used for this project. All included in the archive folder.
1. scraped_data.json - backup JSON file in case web scraping fails
2. GCB2022v27_MtCO2_flat.csv - raw CO2 emission data from the Global Carbon Project
3. database_glacier.csv - raw glacier data from National Snow and Ice Data Center


OUTPUT FILES:
After running the notebook, 5 additional csv files will be saved into the archive folder in the current directory.
1. cleaned_co2_30_years.csv - cleaned datafile of first CO2 emission source
2. cleaned_co2_3_centuries.csv - cleaned datafile of second CO2 emission source
3. merged_co2_data.csv - combined datafile of CO2 emission sources
4. cleaned_glacier_data.csv - cleaned glacier datafile
5. merged_co2_glacier_data.csv - combined datafile of CO2 emissions and glacier data


REQUIREMENTS:
The project requires the following Python libraries:
- selenium
- webdriver-manager
- pandas
- matplotlib
- seaborn
- scikit-learn
- scipy
Install them using '!pip install -r requirements.txt' command.
Note: This command is already included in the notebook.

HOW TO SET UP:
Please check all data source files 'scraped_data.json', 'GCB2022v27_MtCO2_flat.csv', 'database_glacier.csv' is in the archive folder.
Please ensure the archive folder is in the current directory. 
Run each cell in sequence. Output files will be saved into the archive folder.
