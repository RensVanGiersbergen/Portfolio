# What can I do to improve the security of my API?
<br>
<div align="center">
    <img src="https://19yw4b240vb03ws8qm25h366-wpengine.netdna-ssl.com/wp-content/uploads/10-API-Security-Best-Practices.png" width="800">
</div>

## Table of contents

## What is an API?
API stands for _"Application programmable interface"._ An API is nothing more then software running on a server. Software can "talk to" API's to request numerous things of an API. Most common methods in an API are Get, Post, Put and Delete. The get method requests data from the API. The post sends data to an API. The put method sends new data to the API to replace old data. And the delete method request the API to delete data. These requests go to endpoints. Endpoints are the code that allows two applications to talk with each other. The requests from an application using our API all come down to an endpoint. The API will then return a status code of the request (if it succeeded or not) and maybe data that was requested (if it was a get request).

## Why is security important in API's?
API security consist of the following according to [Fortinet](https://www.fortinet.com/resources/cyberglossary/api-security#:~:text=Application%20programming%20interface%20(API)%20security,the%20sensitive%20data%20they%20transfer.):
_"Application programming interface (API) security refers to the practice of preventing or mitigating attacks on APIs. APIs work as the backend framework for mobile and web applications. Therefore, it is critical to protect the sensitive data they transfer."_
<br>
<br>
API's are getting more and more common in the daily life of a software developer. It allows developers to use external systems to make their lifes easier. The amount of publicly accessible API's also keeps on rising. These API's have to be very secure and make sure no one can apply any harm. The data transferred between applications is very crucial and sensitive. For example, youtube's public API. Youtube needs to make sure that attackers can't steal data of youtube's users or do anything weird with their application.

The thing with public API's is that everybody can use them (maybe not everyone, but certainly every software engineers). This is as said above very dangerous, because not everybody has good intentions of using your API. The potential risk of getting attacked are increasing. According to [a research from Salt](https://salt.security/api-security-trends?) (experts in API security), the amount of API attack increased by an extraordinary 681% over the last 12 months.

## What are common ways of attacking an API?
I will start this section with a famous quote. “If you know the enemy and know yourself, you need not fear the result of a hundred battles. If you know yourself but not the enemy, for every victory gained you will also suffer a defeat. If you know neither the enemy nor yourself, you will succumb in every battle.” - Sun Tzu (The art of war). What this means is that you need to understand the attacker to succeed in improving the security of your API.

The most common ways of attacking are:
- [Injection](#injection)
- [DoS/DDos](#dosddos)
- [Authentication Hijacking](#authentication-hijacking)
- [Data Exposure](#data-exposure)
- [Parameter Tampering](#parameter-tampering)
- [Man in the Middle](#man-in-the-middle)
- [Unencrypted Communications](#unencrypted-communications)

### Injection
This mainly consists of SQL-injecting and Cross-site scripting (XSS). With SQL-injection the attacker tries to change the query that goes to the database to try and expose vulnerable data or for example add an acccount with the highest possible authorization to try and get certain permissions. Cross-site scripting focusses on trying to inject malicious scripts. Since the end user's browser has no way of knowing that the script is malicious since it came from a trusted source.

### DoS/DDoS
DoS (Denial of Service) attacks are very common. They are used to shut down applications, which doesn't mean that attackers get to steal or modify data. But they will commonly ask for money to stop the service or will DoS something for money. When getting DoS'ed your system gets a lot of traffic and can't handle all of it, which causes it to stop working properly.

DDoS (Distributed Denial of Service) is the same as a DoS attack the difference is that these attacks are harder to stop and track. While DoS is a single system, DDoS consists of many systems preforming DoS attacks at the same time, from all around the world. This makes it way harder to stop, since all over the world systems are attacking. And for that same reason it's very difficult to track where a DoS attack is coming from.

### Authentication Hijacking
Attackers will try to bypass the authentication systems in an application to gain access to things they shouldn't have access to.

### Data Exposure
Data exposure is crucial is much sensitive data is being exchanged. Data like this that isn't encrypted. Data exposure is a big concern for API's using the HTTP protocol since an attacker can craft malicious requests, control message mapping, and even manipulate the responses generated by the backend system.

### Parameter Tampering
Parameter tampering, whe've all tried it in our semester 2 projects, updating for example the name in the url. The attacker tries to modify data that would be send to the server like username, price, quantity etc.

### Man in the middle
Man in the middle (MitM) is an attack where the attacker tries to get between two applications communicating and to intercept their exchanging data. Either to steal the data or to exchange it.

### Unencrypted communications
Encrypted communication is a must have for secure API's. Without this the attacker gets free reign over the API and data that passes through it.

## What are common ways to improve security in API's?

Starting where we left off. A must-have is encrypted communication. Use TLS (HTTPS) for your API. This is the most important. Now we will discuss the other less but still very important improvements:
- [Hash passwords](#hash-passwords)
- [Using OAuth](#using-oauth)
- [Use API keys](#use-api-keys)
- [Leave authorization to logic](#leave-authorization-to-logic)

## Hash passwords
This is pretty straight forward, hashing passwords makes sure no sensitive data is directly exposed. If in any case the passwords do get leaked. It is encrypted and cannot easily be restored. 

## Using OAuth
Using external authentication leaves you with a lot less work. Which is a very big benefit, but not only that. External authentication is way more secure and you can trust the big companies that allow third-party authentication (Google, Microsoft Azure or AWS). As a developer you know you can rely on them. Doing less security yourself and leaving it to these guys makes sure authentication is done very secure.

## Use API keys
Make use of API keys in your API. This is a code that is used to identify and authenticate, users and applications. Make sure you let your clients give the API in the request header so it is not directly visible in the url for max security.

## Leave authorization to logic
If implementing authorization be sure to never preform any authorization in the endpoints. Leave it to the logic layer since that's also what it should be user for.

## Conclusion:
Next time when i'll be making an API, which is probably faster then I think. I will make sure to always use HTTPS (TLS). Secondly, I will leave authentication to an external authentication third-party. These guys are professionals and are way ahead of authentication, and users trust these big well-known companies. Third of all, I will be using API keys in my API that should be send in the header of a request. This makes it way more secure to use my API.

## Sources:
- [Fortinet](https://www.fortinet.com/resources/cyberglossary/api-security)
- [Mulesoft](https://www.mulesoft.com/resources/api/what-is-an-api)
- [Oracle](https://docs.oracle.com/en/cloud/saas/enterprise-performance-management-common/prest/rest_api_methods.html)
- [Salt](https://salt.security/api-security-trends?)
- [Reblaze](https://www.reblaze.com/wiki/api-security/what-is-an-api-attack/)
- [Owasp](https://owasp.org/www-community/attacks/xss/)
- [Paloalto](https://www.paloaltonetworks.com/cyberpedia/what-is-a-denial-of-service-attack-dos)
- [Stackoverflow blog](https://stackoverflow.blog/2021/10/06/best-practices-for-authentication-and-authorization-for-rest-apis/)
- [restfulapi.net](https://restfulapi.net/security-essentials/)
