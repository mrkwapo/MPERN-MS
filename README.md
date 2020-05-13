# Stock Pal Microservice
![Stock Pal Architecture](https://github.com/mrkwapo/StockPal-MS/blob/master/Stock%20Pal%20architecture%20.jpg?raw=true "Stock Pal Architecture")
## Synopsis
Stock Pal is a Microservices Architecture design concept. This application provides regular users with stock current and historic stock data. 

Design Architecture Concept
Aggregator design pattern. Users make a get request to the search aggregator microservice that will fetch both current and historic data for the user. Only admins have the ability to persist data from a csv file. 

## Construction
The architecture has multiple servers and seperate databases. All users including admin are authenticated and authorized through the gateway in conjunction with the auth microservice. Regular users can only search for current and historic stock records in which requests are sent through the Gateway API.

## Architecture Technology and Languages used 
* Zuul (API Gateway)
* Eureka (Discovery Server) 
* Postgresql (Databases used)
* Spring Batch (Dependency used for persisting big data to DB)
* Spring Boot (Framework)
* Spring Security (Auth)
* JDBC (Database Driver)
* BCrypt (Password Encoder)
* Java (Primary Language)
* Python (Data Preprocessing)



## Links
Below are the links to each microservice.

[API Gateway MS](https://github.com/mrkwapo/spring-batch-microservice)

[Auth MS](https://github.com/mrkwapo/auth-microservice-register-login-logout)

[Eureka Discovery Server](https://github.com/mrkwapo/eureka-server-microservice)

[Historic Big Data Batch Job MS](https://github.com/mrkwapo/spring-batch-microservice)

[Current Data MS](https://github.com/mrkwapo/search-current-data-microservice)
