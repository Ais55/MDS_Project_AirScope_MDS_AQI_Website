# AirScope — MDS AQI Project Website

A responsive static website built with HTML, CSS, and JavaScript. It has the three requested tabs: **Project**, **Results**, and **Team**. The homepage begins with the problem statement.

## Run locally
1. Extract the ZIP file.
2. Open `index.html` in a modern browser. An internet connection is needed to load Chart.js and Google Fonts from their CDNs; the rest is local.
3. For a local server, run `python -m http.server 8000` in this folder and open `http://localhost:8000`.

## Customize
- Edit the four placeholder member cards in `index.html` to match your actual team size, names, bios, contribution tags, and photos.
- Edit the visual styling in `styles.css`.
- Chart data and notebook-reported metrics are in `app.js`.

## Data provenance and interpretation
Content is grounded in the uploaded `MDS_Project_AQI (2).ipynb`, which loads `city_day.csv`. The notebook reports 29,531 rows and 16 columns before preprocessing, 26 cities, and no duplicate rows. The website uses reported output values where available. Some exploratory charts in the notebook were saved as plots without their underlying numeric series in the notebook output, so the website does not invent those values.

Reported metrics are labeled by evaluation stage. The final Gradient Boosting regression test metrics are MAE 16.4729, RMSE 26.2242, and R² 0.8807596. The final Random Forest classification test metrics are accuracy 0.7811159, precision 0.8005655, recall 0.7811159, and F1 0.7674076. The notebook's model-comparison classification table is a validation-stage comparison and shows Gradient Boosting accuracy 0.8011806 and F1 0.7964510.

The notebook has a few inconsistencies in intermediate model comparisons, so this site keeps the final test results separate from validation comparisons rather than blending them.
