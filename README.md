# Robot-lift
This document aims to provide an initial proposal for the implementation of Omni Robot with Kone elevator through Service Robot API 

# Background

![image](https://user-images.githubusercontent.com/125621528/227402726-970703d5-68a8-4190-b77f-2a8b98ed2544.png)

Established in 2012, OH Technologies is a leading provider of Healthcare and Supply & Logistics Automaton Solutions in the region. 
We provide consultation, solutioning, system integration and implementation services of various automation technologies. With 
our current experience and expertise in deploying hospital-wide Pharmacy Automation systems, we are well positioned to assist 
institutions to plan, implement and maintain automation solutions across Healthcare and Supply & Logistics industries.


# Overview
Omni Robot is a mobile robot with built-in high-performance SLAM 2.0 autonomous position and navigation system which allow user to perform 
their task efficiency without external environment adjustment and human programming settings. By implementation of Omni Robot, operational 
efficiency can be enhanced since Omni Robot ensure precision with security innovation.

# Omni Robot Applications

 + Hotel : Meal delivery
  
 + Manufacturing : Pallete delivery
  
 + Hospital : Medicine and samples delivery
 
# Solution Design Flow

![Solution Design Flow](https://user-images.githubusercontent.com/125621528/227409651-3b2c82b8-8db2-4505-be03-a2f6cc28387d.JPG)

# Solution Design Architecture

![Solution Architecture](https://user-images.githubusercontent.com/125621528/227409718-d84c36fe-abd6-4222-8c98-101ab185404a.JPG)
  
# Method of connectivity

|Specifications       | Description                                                            |
|---------------------|------------------------------------------------------------------------|
|4G router to 2.4GWIFI| 4GCPE-M6 (optional)                                                    |
|512AN_HMW Module     | Support dual frequency 2.485G                                          |
|Intel WIFI           | WIFI&BT4.1 802.116/g/n Wireless local area network11ac 5.15GHz-5.825GHz|

# Environmental Requirements

+ Avoid a lot of black marble and black reflective cabinets at the floor height of 30cm

+ Slope angle < 5°

+ Do not travel on the ground with high friction

+ Do not use densely placed thin-legged chairs in the travel area

+ Do not use in an environment above 50°C and below 0°C

+ Do not use on uneven roads

# Instructions

1. Create an application at Sandbox and copy client id and client secret
2. Open postman 
3. Create HTTP request, choose POST and enter this url : https://dev.kone.com/api/v2/oauth2/token
4. Open new tab, choose get and enter this url: https://dev.kone.com/api/v2/application/self/resources
5. Copy any building id
6. Use client id and client secret at Authorization(Basic authentication) to generate token access 
7. Copy token access 
8. Open Websocket request, choose raw and inside this url:wss://dev.kone.com/stream-v2
9. In Params, enter accessToken 
10.In header, enter Sec-WebSocket-Protocol and value 'koneapi'
11. Connect the websocket
12. Send the message

Gantt Chart
<img width="774" alt="image" src="https://user-images.githubusercontent.com/125621528/227426369-f15fbb56-4c05-4f5b-8ef5-4f9673a06204.png">

