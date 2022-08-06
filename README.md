# Authenticate Bank Notes Using Machine Learning

## 📌Introduction
This Machine Learning Web Application uses a several features of Banknotes like **variance**, **skewness**, **curtosis** and **entropy** to predict the Authenticy of Banknotes weither it is Genuine or Forged with an **accuracy of 99.02%** using **Random Forest Classifier**.This Dataset is taken from UCI Repository and also available in Kaggle,Data were extracted from images that were taken from genuine and forged banknote-like specimens. For digitization, an industrial camera usually used for print inspection was used. The final images have 400x 400 pixels. Due to the object lens and distance to the investigated object gray-scale pictures with a resolution of about 660 dpi were gained. Wavelet Transform tool were used to extract features from images,In this ml model we are considering 0 for geniune bank note and 1 for forged bank note.

## 🎯 Purpose of the Project
Whether we pull out paper bills or swipe a credit card, most of the transactions we engage in daily use currency. Indeed, money is the lifeblood of economies around the world. Currency refers to paper money or coins that are in circulation. But currency is actually only a small piece of the monetary economy and just one consideration when looking at the total money supply.

Indeed, most money today exists as credit money or as electronic records stored in databases in banks or financial institutions. But still, the bread and butter of everyday transactions is currency, and that is what we will look more closely at here.

## Why Bank Notes Genuinity is Important ?

As now a days many transactions take place using plastic money , But Bank Notes and Coins are still is in the use and used by more than 56% of Indians as surveyed in 2019 and the major transactions from buying daily households to spending money in various places to buy things in small commodities shop to Barber Shops and Groceries are taken place in notes and if the notes used by people of the country are forged or duplicate this will leads to unstable economy and rise of crimes in country with illegal transactions, so we need to autheticate notes so that it can leads to stable economy and leads towards a well development of country.

Our Model performs fairly well with an **accuracy of 99%** and an** F1 Score of 95%** and **Recall Score of 92%** as we have used **Bagging** Technique which is **Random Forest Classifier** with Sklearn library. This provides a handy tool to utilize the power of Machine Learning and Artificial Intelligence in Binary Classification Problems where time and accuracy is the paramount objective of classification.

## 🏁 Technology Stack

    FastAPI
    SkLearn
    Streamlit
    Heroku
    Flask
    Swagger UI
    Docker
    
## Use FastAPI to Build a Fast API
![image](https://user-images.githubusercontent.com/91668225/183245239-912e32f0-cd26-45f6-ab55-5175f42d3e5e.png)


Run the **FastAPI** using this CMD:
     uvicorn app:app --reload

     INFO: Uvicorn running on http://127.0.0.1:8000 / 

One of the best FastAPI feature is you will get **Swagger UI** a best testing enviroment for your API inbuilt. For acessing it :

  Go to http://127.0.0.1:8000/docs and enjoy the application

## Dockerizing our Application
![image](https://user-images.githubusercontent.com/91668225/183245229-26de5638-fd0a-48aa-b7a9-7b15680779d4.png)

1.Creating a Dockerfile to create a Docker Image.

FROM python:3.7-buster
COPY . /app
EXPOSE 5000
WORKDIR /app
  RUN pip install -r requirements.txt
  CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "5000"]

2.Building the Docker Image

  docker build -t {Name_of_Image}

3.Running our Docker Image

  docker run -p 5000:5000 bank_auth

Note: bank_auth is a docker image name.
Now your Docker Container is running at http://127.0.0.1:8000/docs and this is the **Swagger UI** of FastAPI.






