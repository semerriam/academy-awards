# Academy Awards Database Scraping

This repository scrapes the [Academy Awards Database](https://awardsdatabase.oscars.org/search/) for the International Feature Film category previously called Foreign Language Film. The ultimate output is a html and js file for a map of each country having had a film win the award from the Academy's beginnings. When rolling over each country, information for the year, number of awards by country, film title, and acceptance speech information comes up with a few glitches here and there. 

## Notebook

The notebook, [Merriam_Academy_Awards_Scraping_International_Films.ipynb](Merriam_Academy_Awards_Scraping_International_Films.ipynb)
 scrapes the Academy Awards Database for Best International Feature Film Winners and their Acceptance Speeches using Selenium WebDriver and Beautiful Soup. The ultimate output is a geojson file with the information for film wins by country.
 


[Oscars_International_Films.csv](Oscars_International_Films.csv) is a manually edited version of the final csv backup to be read into the notebook. The csv includes each film receiving an Academy Award in the International Feature Film category with information such as year, country, category name, acceptance speech. This file has an added column for the number of International Feature Film Award wins per country and the excess html in the speech column has been removed.


## HTML & Mapbox

[Critics'_Choice_mapbox_screenshot.png](Critics'_Choice_mapbox_screenshot.png)

[Critics_Choice_map.html](html+mapbox/Critics_Choice_map.html) is the final html file including Mapbox API information with the Mapbox access token removed.

[Oscars_International_Films_Summary2.csv](html+mapbox/Oscars_International_Films_Summary2.csv) is a version of the backup_Oscars_International_Films.csv file with row informaiton combined by country and an additional column named summary_per_country with the summaries of each film combined by each country. This CSV is read into the notebook to merge with the geojson file, [world_custom.geo2.json](html+mapbox/world_custom.geo2.json).

[geo-data.js](html+mapbox/geo-data.js) is a duplicated and renamed version of the geo-data12-22.js file for input into the html document. 


## Outputs: Backup CSVs
 
[backup_Oscar_speeches_International_Films_1957_to_2020.csv](outputs-backup-csvs/backup_Oscar_speeches_International_Films_1957_to_2020.csv) provides a backup of the Acceptance Speeches from 1957 — 2020 before the p class and p tags are removed. 
 
[oscars_International_1957_to_2020.csv](outputs-backup-csvs/oscars_International_1957_to_2020.csv) provides a backup of the 1957 — 2020 merged dataframe including the information for each winner: film title, award category, year, country of origin, and acceptance speech.
 
[backup_Oscars_International_1947_2020.csv](outputs-backup-csvs/backup_Oscars_International_1947_2020.csv) provides a backup of the 1947 — 2020 merged dataframe including the information for each winner: film title, award category, year, country of origin, and acceptance speech unless it was unavailable in the Academy Awards database. Much of the 1947 — 1956 information could not be scraped in the same form as the other year, so the information was added manually in the notebook. 

[backup_Oscars_International_Films.csv](outputs-backup-csvs/backup_Oscars_International_Films.csv) provides a backup to the edited dataframe from Oscar_International_Films.csv with an added column called summary combining multiple columns into one per film. 

[geo-data12-22.js](outputs-backup-csvs/geo-data12-22.js) is the final output of the notebook, a geojson file for input into the html. This file contains the film information by country and the geojson information.


## Licensing
All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). Files in the output/ directory are available under the [Creative Commons Attribution 4.0 International (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/).


