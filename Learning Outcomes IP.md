# Learning Outcomes IP
Learning outcomes for my individual project

## Table of contents
- [1. Web application](#1-web-application)
- [2. Software quality](#2-software-quality)
- [4. CI/CD](#4-cicd)
- [8. Professional](#8-professional)

### 1. Web application

### 2. Software quality
I have done quite a lot about the assurance of my software quality. This includes:
- Unit testing
- Endpoint testing
- Code analyzing with Sonarcloud

Starting with unit testing. The unit tests i wrote were basic tests that involved testing the logic layer of my application. My logic isn't really that advanced though. So these tests were less important then the endpoint tests. Either way i still created them to implement them in my CI (continuous integration) process and test the logic layer. At the bottom of this text is a picture that shows my test explorer in visual studio. I created test for both my collection classes. These have the responsibility to manage the collection of journeys and positions. I wrote only 7 of these tests because there is little logic. it's mostly CRUD-operations <br>

|![image](https://user-images.githubusercontent.com/58734636/170981594-719d9412-a4ab-4f45-a3d8-aa371d67b096.png)|
| :--: |
| _Test explorer of my backend_|

Now onto the Endpoint testing, these tests were way more important compared to the unit tests, because here i can test the full functionality of the backend, from the endpoint. These tests are basically integration tests for the backend. I used a NuGet package (Microsoft.AspNetCore.Mvc.Testing) focussed on testing MVC applications and web api's. I wrote 11 endpoint tests. For every different status code the api could return i did a test. <br>

|![image](https://user-images.githubusercontent.com/58734636/170985163-74434eab-5b29-4534-831e-11a3fee41dbd.png)|
| :--: |
| _Part of my endpoint tests_|


### 4. CI/CD

### 8. Professional
