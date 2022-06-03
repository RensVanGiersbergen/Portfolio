# Learning Outcomes IP
Learning outcomes for my individual project

## Table of contents
- [1. Web application](#1-web-application)
- [2. Software quality](#2-software-quality)
- [4. CI/CD](#4-cicd)
- [8. Professional](#8-professional)

### 1. Web application
Here I will talk about everything that's part of my application. Here's a list of every part I am going to talk about:
- [Xamarin mobile application](#xamarin-mobile-application)
- [Vue.js web application](#vuejs-web-application)
- [Asp.net core web API]

#### Xamarin mobile application
I created a very basic Xamarin mobile application. This application tracks the skater while he is skating. You can start a journey with a given name and the mobile app will request creating a journey using the endpoint in my backend. After getting the new journeys id returned it will add a new position to the journey every 3 seconds. Enough about the logic, more about the application now. I developed it in Xamarin which was a nice experience. The emulator was really cool to use, you can tweak very specific things like battery health, internet connection and even let the emulator start walking a route (which was very great since I didn't have to go skateboard to test my app... which in another way was kinda sad that I no longer had an excuse to go skateboarding under school hours). The app would show you a map while being on a journey which comes from the google maps SDK API en loads in a map from [MapBox](https://www.mapbox.com/) on this map the app draws a route and draws it in a specific color. starting from light-green to red. Every change of color is +10 km/h.

|<image src="https://user-images.githubusercontent.com/58734636/171807407-4d512cb1-0acf-46f2-b013-1e4cf212d8ba.png" height="700px">|
|:--:|
| _Screenshot of my journey to school this morning_ |

#### Vue.js web application
My second frontend is a Vue.js web application. Vue was kind off complicated to start with. You first had to learn the basics, using the components, passing properties with components, routing, using data return and last but definitely not least... the lifecycle hooks. After getting a basic understanding in these difficult but yet easy things. It all started to work out. And I created a very simple yet promising web application. A quick warning though, my frontend developing skills are nowhere to be found.

|![image](https://user-images.githubusercontent.com/58734636/171812758-78ce6a15-ba3f-4d9b-808b-d881e2f8e6ce.png)|
|:--:|
| _List of my journeys_ |

  
|![image](https://user-images.githubusercontent.com/58734636/171812095-d15676f0-2b97-4986-bc99-e774188a538b.png)|
|:--:|
| _Journey overview_ |

### 2. Software quality
I have done quite a lot about the assurance of my software quality. This includes:
- [Unit testing](#unit-testing)
- [Endpoint testing](#endpoint-testing)
- [Code analyzing with Sonarcloud](#code-analyzing-with-sonarcloud)

### Unit testing
Starting with unit testing. The unit tests I wrote were basic tests that involved testing the logic layer of my application. My logic isn't really that advanced though. So these tests were less important then the endpoint tests. Either way I still created them to implement them in my CI (continuous integration) process and test the logic layer. At the bottom of this text is a picture that shows my test explorer in visual studio. I created test for both my collection classes. These have the responsibility to manage the collection of journeys and positions. I wrote only 7 of these tests because there is little logic. it's mostly CRUD-operations <br>

|![image](https://user-images.githubusercontent.com/58734636/170981594-719d9412-a4ab-4f45-a3d8-aa371d67b096.png)|
| :--: |
| _Test explorer of my backend_|

### Endpoint testing
Now onto the Endpoint testing, these tests were way more important compared to the unit tests, because here I can test the full functionality of the backend, from the endpoint. These tests are basically integration tests for the backend. I used a NuGet package (Microsoft.AspNetCore.Mvc.Testing) focussed on testing MVC applications and web api's. As far as I understood correctly this NuGet uses the Startup.cs from the API to create a fake API purely for testing. This will be done before I run the tests and will be done only once. You can even use a different startup then the default one as I did. With this it is possible to let my fake API use my in-memory database. I wrote 11 endpoint tests. For every different status code the api could return I did a test. <br>

|![image](https://user-images.githubusercontent.com/58734636/170985163-74434eab-5b29-4534-831e-11a3fee41dbd.png)|
| :--: |
| _Part of my endpoint tests_|

### Code analyzing with Sonarcloud
At last I used Sonarcloud to analyze my repository in my continuous integration action in github actions. Sonarcloud gives me a nice overview of a lot of things like, code smells (things to improve in your code), bugs, vulnerabilities, code coverage and much more. The cool part about all of this is that Sonarcloud even tells me how to improve all these code smells. It'll tell me how much time it costs to finish and why this is a code smell, what I can do to improve it and most importantly why this improvement is better then my previous code. I use it in my individual project but it's easy to use in group projects as well. You can assign bugs or vulnerabilities to members or add comments under code smells. I Also set up Sonarcloud for our group project. Below are two screenshots of the analyzation Sonarcloud did for my individual project.
|![image](https://user-images.githubusercontent.com/58734636/171047461-34c44fec-716f-4bd8-83d0-d7872acb1ac3.png)|
| :--: |
| _Code smells catched by SonarCloud_|

|![image](https://user-images.githubusercontent.com/58734636/171047662-d565adf8-9f13-4f3b-a9c9-eb88dd70f0a1.png)|
| :--: |
| _Overview page Sonarcloud_|

### 4. CI/CD
I had fun experimenting with github actions and all the crazy possibilities it brings. It felt like learning a new language, at first I was struggeling trying to create my first .yaml file. I didn't really know what I was doing, but after a couple searches on google and experimenting with the yaml file I was able to finish my first .yaml file. It was a simple file that consists mostly of the .net core template auto-generated by Github. But I tweaked a little bit here and there to make it compatible with .net 6. My first file did nothing crazy. It would try to build my application and run the unit tests that I wrote, later it would also test my endpoint tests but I hadn't written them in this point of time.

Later on i extended this yaml file to also publish the build to the Luna servers at fontys using Samkirkland's FTP deploy action. Only if the tests ran successfuly and the build didn't fail it would get published.

|![image](https://user-images.githubusercontent.com/58734636/171802438-497cc4ff-b049-4cf2-8431-9fcffa00ceba.png)|
|:--:|
| _Build, test and publish main .yaml file_ |

Later on in my project I added another Github Action that I would use for my development branch. It included Sonarcloud. This action would simply build the app, run all tests and let Sonarcloud run the scan. I had to struggle a bit with the dotnet code coverage tools to get my code coverage in percent in my Sonarcloud dashboard.

|![image](https://user-images.githubusercontent.com/58734636/171804102-6779e65d-4cf8-4bd0-b043-c4cbe73581d5.png)|
|:--:|
| _developer .yaml file with Sonarcloud_ |

### 8. Professional
