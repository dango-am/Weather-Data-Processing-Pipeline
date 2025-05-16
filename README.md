# Step-by-step instructions to run the pipeline locally
git clone https://github.com/dango-am/Weather-Data-Processing-Pipeline
cd Weather-Data-Processing-Pipeline
mkdir inputs outputs scripts
type nul > scripts\weather_pipeline.py
type nul > requirements.txt
pip install -r requirements.txt
jupyter notebook scripts/weather_proj.ipynb
# Approach and challenges faced
## Approach Used
First the csv file was read using pandas.
The second step was handling the missing values so the way I handeld it are as follows
   - I replaced Missing temperature value with their mean.
   - Rows with missing dates were dropped.
   - Rows with missing or unknown weather conditions were removed.
Third step was standardzing the date so in this step dates were converted to `YYYY-MM-DD` and the different data separators like , and / were changed to 
Fourth step was creating a new column `temperature_fahrenheit` by using the formula given  
The final step was saving the chaged data and visualizing it by using bar chart
