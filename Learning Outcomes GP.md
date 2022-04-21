# Learning Outcomes GP
Learning Outcomes for the Group Project
## Table of contents
- [1. Web application](#1-web-application)
- [3. Agile method](#3-agile-method)
- [5. Cultural differences and ethics](#5-cultural-differences-and-ethics)
- [6. Requirements and design](#6-requirements-and-design)
- [7. Business processes](#7-business-processes)
- [8. Professional](#8-professional)

### 1. Web-application
#### User Friendly:
For the group project I did some research about UX (User Experience) and how to improve it. We were making a dashboard for Bert (from Isaac A.K.A. IO) and after the dashboard was finished it was my job to test it on some basic rules to create a user friendly dashboard. Down below is a screenshot of the tips and tops I gave Rick for his UI.

| <img src="https://user-images.githubusercontent.com/58734636/164194398-c8a75c0a-fe20-4245-a515-66456a1f6b63.png" width="500" height="500" /> |
| :--: |
| _Results of the research I did on UX (in Dutch)_ |

#### Full-stack:
I was responsible for most of the logic in the backend of our application. The things i created for the logic in our backend are the MQTT-client (listener) and the algorithm for the sensors. The MQTT-client is part of our backend, it receives messages from the sensors at Isaac's office. These messages contain temperature and humidity measurements. They send in their data every 30 seconds. We will then store the data in a cache. So if the most recent data is needed we can simply take it out of the cache, so there is no need to run a database query.

If a sensor were to fail to send data my algorithm would get the temperature of the closest sensor. The closest sensor would be calculated using none other than the famous pythagorean theorem (A<sup>2</sup> + B<sup>2</sup> = C<sup>2</sup>). The sensors are on a grid, so it is easy to get the two points of the missing sensor and the other active sensors. Using the theorem we can calculate the distance between the missing sensor and all active sensors and make a list of closest sensors to replace their data with the missing sensors data.
| <img src="https://user-images.githubusercontent.com/58734636/164228667-1792dae7-f9c9-4054-a8ec-8595bee433c5.png" width="1000" height="500" /> |
| :--: |
| _Sensor grid in the office of Isaac_ |

I also helped Yannick out a bit with the backend architecture. We're using Entity framework core for the Data Access Layer. The api-endpoints were my responsibility. I Discussed what kind of data was needed for the heatmap with Rick and Maikel, so I was sure they would get everything they needed.
| ![image](https://user-images.githubusercontent.com/58734636/164219507-c04cdc8e-9ff1-4868-8290-7f6bc77a9451.png) |
| :--: |
| _Screenshot of the architecture of our backend_ |

### 3. Agile method
We work in an agile process in our group project. Every morning we start with the daily stand-up. Here we will discuss what everyone will be doing for the day and where we currently are in the project (in terms of what is completed and what still needs to be done). We will grab our notion board and start assigning tasks (see picture below). At the end of the day we will perform the daily stand-down. Here we will discuss how everything went this day. Think about problems that may have occurred throughout the day, or things that just didn't go as planned.   
| <img src="https://user-images.githubusercontent.com/58734636/164235377-e98aad38-8905-4ecb-aa04-9e9170b56239.png" width="700" height="600" />| 
| :--: |
| _Screenshot of our notion board_ |

We end every sprint with a sprint review and a sprint retrospective. The sprint review is with the product owner. We will talk about what has priority, we gather feedback to improve our product and we take a look at what we are going to focus on upcoming sprint. But most importantly we will deliver parts of the product af often as possible to get as much feedback as possible. After the sprint review we will start the sprint retrospective with our group. We will ask ourselves a lot of questions about how it went this sprint. If anything is not to our liking, we will inspect it and adapt ourselves to improve it.
| <img src="https://www.flowsphere.ch/wp-content/uploads/2017/02/ScrumFramework_17x11-1024x663.png" width="800" height="500" />| 
| :--: |
| _The scrum workflow we apply in our project_ |

### 5. Cultural differences and ethics

### 6. Requirements and design 
We try to get as much feedback as possible from our stakeholder. We try to meet every week, so we can improve our product as much as possible. Bert (our stakeholder) gives us feedback. For example our heatmap. We used a date and time picker to select a specific date and time for the heatmap to show the data of that specific date and time. Afther feedback from Bert we are now using a slider to pick the time and a date picker for the date. This is just an example of how we process the given feedback to improve our product. Let's take another example. At first we would have the lowest sensor value as the lowest point in the legend and the highest sensor value as the highest point in the legend. Afther feedback from Bert we now have a minimum value and a maximum value in the legend, the problem was that if the lowest sensor value was 24 degrees, the color in the legend would have been green.. this could give users a wrong indication of how warm it is.
|![temperature_distribution](https://user-images.githubusercontent.com/58734636/164425656-3a2769cb-121b-4ede-a318-0d91b53e7a28.png)|
| :--: |
| _Legend of the heatmap_ |

I've discussed a lot with Yannick about the design of our backend. An example of this is when we were discussing a way to easily return the most recent data


### 7. Business processes
### 8. Professional

