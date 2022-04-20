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
### 5. Cultural differences and ethics
### 6. Requirements and design 
### 7. Business processes
### 8. Professional

