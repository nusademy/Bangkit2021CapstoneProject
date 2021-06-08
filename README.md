# Bangkit2021CapstoneProject
Public repository for Bangkit Academy 2021 Capstone Project Submission.

**Team ID        :** Capstone Team B21-CAP0289 
**Selected theme    :** National Identity & Character Building  
**Mentor        :** Trisna Gelar Abdillah  
**Member         :**  
Rachvika Cindy Gayatri [Github Link](https://github.com/rachvika18)  
Ahmad Tomi Sholikin [Github Link](https://github.com/AhmadTomi)  
Andreas Abi Permana [Github Link](https://github.com/andreasabipermana)  
Matin Muhith [Github Link](https://github.com/matinmuhith)  
Muhammad Nanda Jabar Rozaq [Github Link](https://github.com/muhnandajr)  
Libby Lisandra [Github Link](https://github.com/libbylisandra)  


# Nusademy
![](https://github.com/nusademy/Bangkit2021CapstoneProject/raw/main/logo/logo.png)

:#1 App Solutions of Indonesia Fundamental Educational Problems


## Backgrounder

Indonesia was ranked 60th of 61 countries in terms of reading interest. Unequal distribution of teachers and lack of teachers welfare is one of the biggest problems in our country. We know that teachers play a big role in producing the quality of their graduates. If we can't have the best teachers and the best education, we can’t guarantee that we will have talented graduates. From that we come to solve those problems. 
Nusademy is an ecosystem platform that provides a new way of learning for Indonesia's young generation. Nusademy connects the best talent in Indonesia into school to solve educational inequality caused by unequal distribution of teachers, low reading interest and passion discovery. We are using chatbots to identify the passion of students and give books recommendations that can improve their ability to develop their potential. Can you imagine is just like Gojek that connect driver and passenger we also do the same to connect best talent or teacher into school and give supporting things that need in Indonesian education



## Features

- Helps identify young Indonesian’s Passion and Career Possibility with Passion Identifier Chatbot;
- Connecting Platform for Teachers and Schools Throughout Indonesia with Android based App;
- Giving solutions to users with lack of interests in Reading with Video Book Narrations;



# Nusademy App Workflow
Nusademy Android Application using Retrofit Application to Connect with Backend API
![](https://github.com/nusademy/Bangkit2021CapstoneProject/blob/main/logo/Android%20App%20Architecture.png)
# Nusademy Machine Learning Architecture
Passion and Job Recommendation using MBTI Datasets Architecture
![](https://github.com/nusademy/Bangkit2021CapstoneProject/blob/main/logo/ML%20Architecture.png)
# Cloud Computing
Nusademy uses Google Cloud Platform as its cloud infrastructure. The following is Nusademy's cloud architecture:
![](https://github.com/nusademy/Bangkit2021CapstoneProject/raw/main/Cloud-Computing/Nusademy%20Cloud%20Architecure%20Design.png)
## Services used
### App Engine
App Engine is used to deploy Backend API applications from Nusademy. we deploy api backend application using Standard Environment and nodejs runtime. Details about deploying to App Engine can be found in the following Backend API repository link <https://github.com/nusademy/nusademy-backend-api>.
### Cloud Run
Cloud Run is used to deploy the Webhook Machine Learning API application from Nusademy. This application uses the python programming language to carry out the learning process and provide API services. Details about deploying to Cloud Run can be found in the following Webhook ML repository link <https://github.com/nusademy/webhook-ml>.
### Storage Bucket
The Storage Bucket is used to accommodate files and directories on the App Engine service, Cloud Build logs and artifacts, accommodate Nusademy landing page files <https://github.com/nusademy/landing_page> , and accommodate several important files used by the Nusademy Application.
### Load Balancing Services
HTTP(S) Load Balancing Services is used to create a custom landing page web service from Storage Bucket. HTTP(S) Load Balancing Services will direct traffic to the Storage Bucket so that clients can access the html files that are there. This HTTP(S) Load Balancing Services uses the Storage Bucket backend and HTTP(S) frontend services. The nusademy landing page can be accessed at the following link <https://nusademy.id>
### Cloud Build
Cloud Build is used to perform Continuous Integration and Continuous Delivery (CI/CD) on Backend API, Webhook ML API, and Landing Page applications. here we automate processes from deploy to App Engine, Cloud Run, and rsync processes from buckets used to host landing pages. Configuration details can be found in the cloudbuild.yaml file in each of the application's repos.
### Cloud DNS
Cloud DNS is used for record management from the nusademy.id domain. Each domain record of an application running on our Google Cloud Platform is linked to a subdomain of Cloud DNS.
### Cloud SQL
Cloud SQL is used as a Database service for the Nusademy API Backend. The Nusademy backen API uses the Postgre SQL version 13.

## Cloud Architecture Description
### Cloud IAM
Because Machine Learning Dev and Android Dev don't need infrastructure on Google Cloud, therefore for IAM members only cloud engineers, namely c2031998@bangkit.academy and c2031998@bangkit.academy.
### Cloud DNS
We use Cloud DNS to connect Google Cloud with the nusademy.id domain which is used for the landing page. Then we created a subdomain api.nusademy.id which was used for the backend api and webhook.nusademy.id which was used for the webhook machine learning.
### API Backend Infrastucture
For the backend infrastructure we created on github for the repository with the link https://github.com/nusademy/nusademy-backend-api . Then we create CLoud SQL using Postgree SQL for the database with name nusademy. Then we also create a Cloud Storage with name nusademy used to store app.yaml. Then create Continuous Integration and Continuous Development using Cloud Build after it is deployed on App Engine.
###	Webhook ML Infrastucture
For Machine Learning we create datasets and train datasets outside Google Cloud and store them in a repository with the link https://github.com/nusademy/webhook-ml . Then we connect to Cloud Build for Continuous Integration and Continuous Development after it is deployed on Cloud RUN.
###	Landing Page Infrastucture
Then for the landing page infrastructure, we put the source code in the repository with the link https://github.com/nusademy/landing_page . Then we connect to Cloud Build for Continuous Integration and Continuous Development after that it is stored in Cloud Storage nusademy.id. Then connected to the domain using load balancing.

# Android App User
## Features Basic User
- User Registration;
- Login;
- Access Chabot Passion Identifier;
- Access Video Book Narration;

## Features Teacher/Top Talent
- User Registration;
- Login;
- Access Chabot Passion Identifier;
- Access Video Book Narration;
- Request Teaching into School (Temporary and Guest Request);
- Reject/Approve Teaching Invitation by School;

Details about the Android App User can be found on the following github repository link <https://github.com/nusademy/android-dev>.

# Android App School
## Features
- User Registration;
- Login;
- Add and Edit School Profil;
- School Management: Class and Subjects;
- Invite Temporary Teacher into School;
- Invite Guest Teacher into School;
- Reject/Approve Teaching Request by Teacher;

Details about the Android App School can be found on the following github repository link <https://github.com/nusademy/android-school-app-dev>.

# Machine Learning
## Features
- Passion Identifier using MBTI Datasets based on users input;
- Job Recommendation based on user's passion;

Details about the Machine Learning can be found on the following github repository link <https://github.com/nusademy/webhook-ml>.

# Web API Android Application
## Users Type
- Admin;
- Basic User;
- Top Talent;
- Teacher;
- School Manager;

## Features
- User Management
- Teacher and Top Talent Advanced Profile
- School Information, Class, and Subject Management
- Connect Top Talent into School (Invitation and Approval)
- Connect Teacher into School (Invitation and Approval)
- Teachers and Top Talent Job Vacancy
- Book Narration Videos
- Donation

Details about the Machine Learning can be found on the following github repository link <https://github.com/nusademy/nusademy-backend-api>.

# Importat Link
Dataset Link:  <https://www.kaggle.com/datasnaek/mbti-type>

Deployed Link: 

| **Solutions** | **Link** |
| :------------ | :------------ |
|  User and Teacher App (.apk) | **Comming Soon**  |
|   School App (.apk) | **Comming Soon**  |
|  Notebooks |  <https://colab.research.google.com/drive/1VQiiGNxneu42VCTr8kh7v93o9FT1nmpM?usp=sharing>  |
|  Web API Nusademy |  <https://api.nusademy.id> |
|  Webhook API |  <https://webhook.nusademy.id> |
|   Landing Page| <https://nusademy.id>  |


Github Repo Link: 

| **Solutions** | **Link** |
| :------------ | :------------ |
|  Public Git Repository Nusademy | <https://github.com/nusademy> |
|  API Repository | <https://github.com/nusademy/nusademy-backend-api> |
|  Machine Learning Webhook | <https://github.com/nusademy/webhook-ml> |
|  Android School App | <https://github.com/nusademy/android-school-app-dev> |
|  Android Basic User and Teacher App  | <https://github.com/nusademy/android-dev>  |
|  Landing Page Repository | <https://github.com/nusademy/landing_page>  |
|  Architecture Nusademy | <https://github.com/nusademy/Bangkit2021CapstoneProject> |

Academic Paper Link: **Comming Soon**

# End
