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

Now onto the Endpoint testing, these tests were way more important compared to the unit tests, because here i can test the full functionality of the backend, from the endpoint. These tests are basically integration tests for the backend. I used a NuGet package (Microsoft.AspNetCore.Mvc.Testing) focussed on testing MVC applications and web api's. As far as I understood correctly this NuGet uses the Startup.cs from the API to create a fake API purely for testing. This will be done before i run the tests and will be done only once. You can even use a different startup then the default one as I did. With this it is possible to let my fake API use my in-memory database. I wrote 11 endpoint tests. For every different status code the api could return i did a test. <br>

|![image](https://user-images.githubusercontent.com/58734636/170985163-74434eab-5b29-4534-831e-11a3fee41dbd.png)|
| :--: |
| _Part of my endpoint tests_|

At last I used Sonarcloud to analyze my repository in my continuous integration action in github actions. Sonarcloud gives me a nice overview of a lot of things like, code smells (things to improve in your code), bugs, vulnerabilities, code coverage and much more. The cool part about all of this is that Sonarcloud even tells me how to improve all these code smells. It'll tell me how much time it costs to finish and why this is a code smell, what i can do to improve it and most importantly why this improvement is better then my previous code. I use it in my individual project but it's easy to use in group projects as well. You can assign bugs or vulnerabilities to members. I Also set up the Sonarcloud for our group project. Below are two screenshots of the analyzation Sonarcloud did.
|![image](https://user-images.githubusercontent.com/58734636/171047461-34c44fec-716f-4bd8-83d0-d7872acb1ac3.png)|
| :--: |
| _Code smells catched by SonarCloud_|

|![image](https://user-images.githubusercontent.com/58734636/171047662-d565adf8-9f13-4f3b-a9c9-eb88dd70f0a1.png)|
| :--: |
| _Overview page Sonarcloud_|

### 4. CI/CD

### 8. Professional
