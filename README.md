# DocPlus Application # 


This project is a Doctor Appbuilt using Spring Boot with Java.

---

## Framework Used
* Spring Boot

---

## Language Used
* Java

---

## Data Model

The Doctor model is defined in the doctor class, which has the following attributes:
```
doctorId : unique identifier for each doctor
doctorName : name of the doctor
specialization : Doctor specialized in which field
appointments : what are the appointments doctor have 

```
The Patient model is defined in the patient class, which has the following attributes:
```
patientId : unique identifier for each patient
patientFirstName :first name of the patient
patientLastName :last name of the patient
patientEmailId :email id of patient
patientPassword : password for the patient 
patientContact : mobile number of the patient

```
The Appointment model is defined in the appointment class, which has the following attributes:
```
id : unique identifier for Appointment
doctor : doctor assigned to that appointment
patient : patient assigned to that doctor


```

---

## Data Flow

```
The user sends a request to the application through the API endpoints.
```


```
The API receives the request and sends it to the appropriate controller method.
```


```
The controller method makes a call to the method in service class.
```


```
The method in service class builds logic and retrieves or modifies data from the database, which is in turn given to controller class
```


```
The controller method returns a response to the API.
```


```
The API sends the response back to the user.
```

---



### API Endpoints :-

### for Doctor ###

* PostMapping: /doctor
```
In database we add a new doctor given through API.
```

* GetMapping: /doctor/{docID}/appointments"
```
This endpoint gives us the data of all appointments belongs to particular doctor
```

## for patient ##

* PostMapping: "/patient/signup"
```
This endpoint is used to sign up the patient
```
* PostMapping: "/patient/signin"
```
This endpoint is used to sign in the patient
```
* GetMapping: "doctor"
```
This endpoint gives us the data of all doctors assigned to particular patient based on patient email address
```

* DeleteMapping : "appointment"
```
This end point will take the patient email address and appointment Id and deletes the appointment
```
### for Appointment ###
* PostMapping : "appointment"
```
This end point will
```
This end point will accept the appointment and save in to database

---

## Data structure Used
* SQL
```
We have used SQL data structure as a database to implement CRUD Operations 
```
---

## Project Summary

The project "Doctor App" is developed using the Spring Boot framework and focuses on managing entities such as doctors, patients, and appointments. The application provides functionalities for signup and signin for patients to book appointments. It also includes authorization features to ensure secure access to the system. The project utilizes CRUD operations for all the models and the database used is SQL.

The Doctor App aims to facilitate the appointment booking process between doctors and patients. The entities involved are:

Doctor: Represents the doctors in the system. It includes attributes such as name, specialization, contact details, and availability.

Patient: Represents the patients who can book appointments. It includes attributes like name, contact information, and any relevant medical history.

Appointment: Represents the appointments made by patients with doctors. It includes details such as the doctor involved, the patient, appointment time, and any additional information.

The application provides a signup and signin mechanism for patients, ensuring that only authorized users can access the system. This authentication process enhances security and protects sensitive patient information.

CRUD operations (Create, Read, Update, Delete) are implemented for all the models involved. This means that doctors, patients, and appointments can be created, retrieved, updated, and deleted as required.

The project utilizes a SQL database to store and manage data. SQL databases are widely used for their relational nature and ability to handle structured data effectively. This choice allows for efficient storage, retrieval, and management of doctor, patient, and appointment information.

In summary, the DocPlus developed using Spring Boot is a comprehensive application that facilitates appointment booking between doctors and patients. It includes features like signup, signin, and authorization for patients, as well as CRUD operations for managing doctors, patients, and appointments. The use of a SQL database ensures efficient data storage and retrieval.