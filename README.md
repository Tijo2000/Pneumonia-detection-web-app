# Pneumonia-detection-web-app

# Pneumonia detection web app using deep learning

The main aim of this project is the detection of pneumonia by automatically locating lung opacities on chest 
radiographs with a target accuracy of more than 90% (using transfer learning) and low false 
negatives , using various pretrained models like VGG16, Resnet50 and Densenet121 in a flask web application 
to display the results.


## Related

Here are some articles and news which were inspiration for this project.

[An advisor to the Maharashtra govt's Covid-19 task force said the new strain of the virus is causing pneumonia in patients in the early stages of the disease.](https://www.indiatoday.in/coronavirus-outbreak/story/new-variant-of-covid-19-virus-is-causing-pneumonia-in-early-stages-of-disease-maharashtra-official-1771055-2021-02-19)

[Doctors, who said they are seeing a rise in COVID-19 pneumonia cases, pointed out that the pandemic is likely to increase all-cause pneumonia deaths by more than 75%.](https://www.thehindu.com/news/national/karnataka/nearly-80-increase-in-covid-19-pneumonia-cases-say-doctors/article33135824.ece)

[Many city hospitals report rise in post-Covid pneumonia case ..](https://timesofindia.indiatimes.com/city/patna/many-city-hospitals-report-rise-in-post-covid-pneumonia-cases/articleshow/79844319.cms)

[Divergences on expected pneumonia cases during the COVID-19 epidemic in Catalonia: a time-series analysis of primary care electronic health records covering about 6 million people](https://bmcinfectdis.biomedcentral.com/articles/10.1186/s12879-021-05985-0)



  
## Background


Pneumonia is an infection that inflames the air sacs in one or both lungs. The air sacs may fill with fluid or pus (purulent material), causing cough with phlegm or pus, fever, chills, 
and difficulty breathing. Pneumonia can range in seriousness from mild to life-threatening. 
It is most serious for infants and young children, people older than age 65, and people with 
health problems or weakened immune systems. It is curable disease especially if detected in 
the early stages.

Signs and symptoms of pneumonia vary from mild to severe, depending on factors such as 
the type of germ causing the infection, and your age and overall health

- Chest pain when you breathe or cough
- Confusion or changes in mental awareness (in adults age 65 and older)
- Cough, which may produce phlegm
- Fatigue
- Fever, sweating and shaking chills
- Lower than normal body temperature (in adults older than age 65 and people with weak immune systems)

Most common causes of pneumonia are bacteria and viruses(COVID 19) in the air we breathe. 
Pneumonia is classified according to the types of germs that cause it and where you got the 
infection for example Community acquired (outside of hospitals or other health care 
facilities), Hospital acquired or Aspiration acquired.


Chest radiographs are preferred for diagnosis of pneumonia as they are less expensive than 
CT scans and show both - presence and visual depiction of the spread of the disease unlike 
blood tests. In addition, a chest X-ray can be used to diagnose many conditions and diseases 
such as pleurisy, pulmonary edema, pneumonia, bronchitis, cysts, tumours, cancers, asthma, 
pericarditis, cardiomegaly, heart failure, pneumothorax, and rib fractures.

  
## Drawbacks of previous problem, solution to this problem

1. Diagnosis manifests as an area(s) of increased opacity on a chest radiograph (CXR) which needs 
to be reviewed by highly trained specialists.

2. Although very common and curable, accurately diagnosing pneumonia is difficult

3. Challenges faced in diagnosis using CXR are-
   - Lung conditions : fluid overload (pulmonary edema), bleeding, volume loss (atelectasis/collapse), lung cancer, or post-radiation.
   - Outside of the lungs, fluid in the pleural space (pleural effusion) also appears as increased 
     opacity on CXR. 
   - Positioning of the patient and depth of inspiration High workload on radiologist.

Thus, there is a requirement for a faster method to predict pneumonia using a CXR.

So this project will be very useful to automatically locate lung opacities on chest radiographs and 
predict if the patient is suffering from pneumonia through a user friendly web app.

User may upload the images of chest x ray and simply submit them. The model will 
accurately predict pneumonia and return the result in 5 seconds
The suitability of this deep learning model for clinical use has not been validated! The neural network 
achieved accuracy exceeding 90% on the relevant test set of more than 5000 x-rays. Please note that the 
predictive accuracy of the model, depends on the quality and quantity of the training data. Therefore, the 
model has limitations and cannot be used for definite clinical predictions! Instead, it can be used for 
research purposes and for comparison with other similar model.



  
## Tech Stack

- Used pretrained transfer learning models like VGG16 , Resnet50 , Densenet121 , Inceptionv3 from Keras applications.
- html
- css
- javascript
- flask

**Task 1 — Model Training and Validation**
Training and model validation are performed in Integrated Development Environment (IDE) or 
Notebook either on your local machine or on cloud. In our project we used Jupyter Notebook to develop 
our deep learning pretrained models. 
In our case, we have performed four model evaluations. The first model i.e VGG16 performed well with 
92 % accuracy . The second model ie. Resnet also performed well with 91 % accuracy and our denset 
model with 93 % accuracy . Our inception v3 model performed average with 77 % 
After finishing our first task of training and selecting a model for deployment. The final model is now 
saved as a file in the local drive under the location defined in the save_model() function in .h5 format

**Task 2 — Building Web Application**
After loading our model we started building a web application that can connect to them and generate 
predictions on new data in real-time. There are two parts of this application:
 - Front-end (designed using HTML)
 - Back-end (developed using Flask in Python)
The front-end of web applications is built using HTML .
CSS (also known as Cascading Style Sheets) describes how HTML elements are displayed on a screen. 

## Installation

For proper execution of application firstly create an environment, then to install prerequisite libraries execute below command in terminal.

```bash
  pip install -r requirements.txt
```

To run the app use this command
```bash
  app.run(debug=True, use_reloader=False)
```
    
## Deployment

This app is currently live and can be found at: https://pneumonia-detection-web-app.herokuapp.com/.

SCREENSHOTS

![Screenshot (414)](https://user-images.githubusercontent.com/56153083/128311781-668d863a-1970-4328-a9f4-0847241b1ee5.png)
![Screenshot (415)](https://user-images.githubusercontent.com/56153083/128311800-35996f31-4e14-485a-bfee-ebf109f5aa94.png)
![Screenshot (416)](https://user-images.githubusercontent.com/56153083/128311814-2ab6e485-81df-41dd-96d4-a10664854e59.png)
![Screenshot (417)](https://user-images.githubusercontent.com/56153083/128311824-c8865c48-a461-4fb9-ad2d-67c6208b8101.png)
![Screenshot (418)](https://user-images.githubusercontent.com/56153083/128311832-1b1dd527-f59f-4a12-b3ab-8cb4d4a29def.png)
![Screenshot (419)](https://user-images.githubusercontent.com/56153083/128311836-80794d1c-e04e-463e-85d1-49fceef2765f.png)
