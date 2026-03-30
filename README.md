# Gold Recovery Prediction in Industrial Processes

## Project Overview
This project aims to predict gold recovery rates in an industrial process using machine learning models and advanced data preprocessing.

## Objectives
- Predict rougher and final recovery rates
- Improve operational decision-making
- Handle missing and delayed data features

## Tools & Technologies
- Python (pandas, NumPy, scikit-learn)
- Jupyter Notebook

## Methodology
- Data validation (recovery calculation verification)
- Handling missing values and unavailable features
- Outlier detection and removal
- Exploratory Data Analysis (EDA)
- Model training with cross-validation
- Evaluation using sMAPE

## Key Visualizations

### Temporal Analysis of Missing Values for Rougher Recovery
![Patrón temporarl de valoresa usentes](Images/Patrón_temporal_de_valores_ausentes.png)
These visualizations identify significant data gaps and seasonal missingness patterns in the rougher.output.recovery feature between 2016 and 2018.
The timeline and monthly frequency charts reveal systematic clusters of missing data—particularly in early 2018—suggesting recurring sensor downtime or process maintenance periods that must be addressed during data cleaning.


### Average Metal Concentration Trends per Purification Stage
![Comparación de concentraciones por etapa](Images/Comparación_de_concentraciones_por_etapa.png)
These line charts track the concentration of Gold (Au), Silver (Ag), and Lead (Pb) through three key processing stages: Rougher, Primary Cleaner, and Final.
While gold concentration increases significantly as intended by the purification process, silver shows a sharp decline, and lead experiences a slight upward trend, indicating successful mineral separation and enrichment.


### Distribution Comparison: Training vs. Test Feed Size
![Distribuciones](Images/Distribuciones.png)
These histograms compare particle size distributions between training and test sets, confirming that both datasets share nearly identical shapes and scales.
The overlapping distributions for both Rougher and Primary Cleaner stages ensure that model evaluations will be consistent and representative of the training conditions.


### Total Concentration Variance Across Processing Stages 
![Concentraciones](Images/Concentraciones.png)
These box plots track total substance concentration from raw material through the rougher and final stages, highlighting a clear increase in enrichment density.
While the median concentration rises and the IQR narrows at the final stage, a significant volume of low-value outliers persists, indicating potential inefficiencies or measurement noise.


### Model Performance: Prediction vs. Actual Recovery Distribution
![Comparaciones](Images/Comparaciones.png)
These charts show the model accurately captures central recovery trends at both stages but remains conservative by narrowing the overall variance.
The box plots further highlight that the model fails to fully replicate the frequent low-recovery outliers present in the actual training data.


## Models Used
- Linear Regression (baseline)
- Random Forest (final model)

## Performance
- Final model: Random Forest
- sMAPE: **8.09%**
- Improved performance vs baseline

## Key Findings
- Strong relationship between rougher and final stages
- Recovery depends on multiple variables → complex system
- Linear models are insufficient for capturing system behavior

## Business Impact
- Model can support operational decisions
- Helps detect inefficiencies in the process
- Useful for predicting performance trends

## Limitations
- Should not be the only decision-making tool
- Sensitive to changes in process conditions

## Next Steps
- Incorporate more process variables
- Test advanced models (XGBoost, LightGBM)
- Deploy model for real-time monitoring


pip install -r requirements.txt

