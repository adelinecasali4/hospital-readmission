# Identifying Risk Factors and Preferred Hospitals for Hip/Knee Replacements: An Analysis of 2019-2022 Hospital Readmission Reduction Program Data  
Adeline Casali* and Scott Eugley*  
*Each author contributed equally to the design, coding & development, analysis, and writing of this project


## Project Overview  
This study utilized machine learning to analyze data from the Hospital Readmission Reduction Program (HRRP) to identify significant risk factors associated with hospital readmission rates for hip/knee replacement surgery patients and classify hospitals as either preferred or non-preferred for this procedure. Machine learning models were trained using HRRP data from 2019-2022, and tested on 2024 HRRP data.  

The key question of the analysis is: What risk factors are most significantly linked to readmission rates after hip and knee replacement surgery? The analysis found that the most important predictors were complications like accidental cuts during treatment, wounds reopening after surgery, and kidney problems following the procedure. Overall hospital satisfaction ratings from Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS) surveys were also a top factor. This supports the hypothesis that higher patient satisfaction scores often correlates with better patient outcomes.  

A Random Forest model was able to accurately classify hospitals as preferred or non-preferred with 98% accuracy. This suggests it could be a useful tool for health insurance companies to guide patients to hospitals with better outcomes. However, there is also concern about potential overfitting and data leakage within the model that warrants further investigation.  

The findings from the analysis highlight areas in which hospitals could focus on to reduce readmissions, such as reducing surgical complications and improving the overall patient experience. With further investigation and refinement, this approach may help improve patient outcomes and also reduce healthcare costs associated with hospital readmissions after hip/knee replacement surgeries.  

### Data
The data for this research can be accessed [here](https://data.cms.gov/provider-data/topics/hospitals). 

### User Testing
Code successfully self-tested and user-tested as of 8/23/2024. 
