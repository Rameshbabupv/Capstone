# Capstone Project: Predict Department 
### -------- for a given snippnet of conversation or summary
#### Authors:  Ramesh Babu                  
#### DSI-113020  : Mar-04-2021


#### - [Problem Statement](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#problem-statement)
#### - [Project Directory](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#project-directory)
#### - [Executive Summary](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#executive-summary)
#### - [Data Collection](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#data-collection)
#### - [Data Cleaning and EDA](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#data-cleaning-and-eda)
#### - [Modeling](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#modeling)
#### - [Data Limitations and Constraints](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#data-limitations-and-constraints)
#### - [Future Work](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#future-work)
#### - [Final Conclusions and Summary](https://git.generalassemb.ly/rameshbabu/submission/tree/master/projects/Capstone#final-conclusions-and-summary)




## Problem Statement
In Fortune 500 companies , like paypal having 25,000 employes and having 3000 projects / teams, it is a big challenge for a bug to be navigated to a </br>
Right Department , </br>
Right Team ,  </br>
Right Component, </br>
Right developer,</br>
With right Severity.</br>




## Project Directory
```
Capstone-11302020
├── README.md
├── app
│   ├── Pickle_lr_Model.pkl
│   ├── README.md
│   ├── app.py
│   ├── config.py
│   ├── database.py
│   ├── database_file
│   │   ├── images.db
│   │   ├── notes.db
│   │   └── users.db
│   ├── image_pool
│   │   ├── 3afadaa2a3cbc1fffc6d8229ca1936b9760e1c56-made-with-flask.png
│   │   ├── cbebc37b8e9ae56d722fc3966bb78da4ce48f9a6-flask.png
│   │   └── f739cc0a8bc1c3d17cc3dcc4fc5ff70b8266998b-flask-project.png
│   ├── requirements.txt
│   ├── static
│   │   ├── css
│   │   │   ├── bootstrap.min.css
│   │   │   └── bootstrap.min.united.css
│   │   ├── img
│   │   │   ├── flask-powered.png
│   │   │   └── public.jpg
│   │   └── js
│   │       ├── bootstrap.min.js
│   │       └── jquery.min.js
│   └── templates
│       ├── admin.html
│       ├── index.html
│       ├── layout.html
│       ├── page_401.html
│       ├── page_403.html
│       ├── page_404.html
│       ├── page_405.html
│       ├── page_413.html
│       ├── private_page.html
│       └── public_page.html
├── code
│   ├── 01-Get-Data-From-Reddit.ipynb
│   ├── 02-Create-Tickets-in-Jira.ipynb
│   ├── 03-01-EDA-Cooking.ipynb
│   ├── 03-02-EDA-Machine-Learning.ipynb
│   ├── 03-03-EDA-Movies.ipynb
│   ├── 03-04-EDA-Political-Discussion.ipynb
│   ├── 04-01-LogesticRegression-Noencode.ipynb
│   ├── 04-02-Encoded-Logistic-Regression.ipynb
│   ├── 04-03-KNN-Model.ipynb
│   └── 04-04-RNN.ipynb
├── data
│   ├── Cooking_1614479417.csv
│   ├── MachineLearning_1614415561.csv
│   ├── PoliticalDiscussion_1614348717.csv
│   ├── books_1614704119.csv
│   └── movies_1614724349.csv
├── presentation
│   └── Capstone_Presentation.pdf
└── requirements.txt
```

## Executive Summary
This project consists of 4 major components </br>
1. Data Collection from Reddit for proxying 5 different projects. These are 
 <li>Political Discussion
 <li>Machine Learning
 <li>Books
 <li>Cooking
 <li>Movies </br>
2. Tickets need be created in up and running Jira with PostgreSQL backend. <br>
3. Developing Flask application to give user to key in data </br>
4. Model to predict department by looking in to the summary of the snippet <br>


## Data Collection
Data has been collected from Reddit "api.pushshift.io" from Political Discussion, Machine Learning, Books, Cooking, Movies. By giving 1sec delay, I was able to pull past 20,000 posts per topic and able create all posts in respective projects. 


## Data Cleaning and EDA
Since this project is based on NLP , I was able join the ticket Summary and ticket Descrptions and create a stream of text for a given ticket in a given prject . Other than applying regex to remove emoji's and escape charaters, I did not see any major issues.


## Modeling
For Modelling, I took about 10,000 rows from each project and started building Logistic Regression and base prediction. Since data is faily distributed amoung projects, so the Null model is 0.20 

## Data Limitations and Constraints
I have run the training in my local laptop and with this huge dataset it took very large time . When I get a real data in a company having GPU, I should be able to train the huge dataset



## Future Work
Web development started from static page, then to dynamic page, and asychronize call populating few areas fof the page . With the prediction model, we should be able to implement Question-Answer model and replace Frontline resourses 


## Final Conclusions and Summary
with this project as proof of concept, we can ealiy replace Triage, and Frontline team in a company. During the triage process when human makes any assignment issue, we cannot rank and rectify it in future. But with this prediction model,  every success and failure are captured and we can retain the models. As days pass and when our models see more data , it will get better and better


