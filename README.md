# Stock Pal 
<p align="center">
![Stock Pal Architecture](https://github.com/mrkwapo/StockPal-MS/blob/master/stockpal%20architecture.jpg "Stock Pal Architecture")
  </p>
## Synopsis
Stock Pal is a Microservices Architecture design concept. This application provides regular users with historic, current and predicted stock data. 

## Design Architecture Concept
Aggregator design pattern. Users make a get request to the search aggregator microservice that will fetch both current and historic data. Machine Learning is used to make predications of future stock prices. Only admins have the ability to persist historic Big Data from a csv file to the database. The Big Data feature is multi-threaded to optimize performance in terms of speed.

## Construction
The architecture has multiple servers and seperate databases. Registered users, including admin, are authenticated and authorized through the gateway in conjunction with the auth microservice. Guest users can only search for current and historic stock records in which requests are also sent through the API Gateway.

## Architecture Technology and Languages used 
* Zuul (API Gateway)
* Eureka (Discovery Server) 
* Postgresql (Databases used)
* Spring Batch & TaskExecutor (Dependencies used for optimizing Big Data persistence)
* Spring Boot (Framework)
* Spring Security (Authorization and Authentication)
* JDBC (Database Driver)
* Java (Primary Language)
* Python (used for Data Preprocessing, API Consumption and Machine Learning Model)
* Flask (for Python API Development)

## Links to each Microservice:

[API Gateway MS](https://github.com/mrkwapo/spring-batch-microservice)

[Auth MS](https://github.com/mrkwapo/auth-gateway-ms)

[Eureka Discovery Server](https://github.com/mrkwapo/eureka-server-microservice)

[Persist Big Data MS](https://github.com/mrkwapo/spring-batch-microservice)

[Current Data MS](https://github.com/mrkwapo/current-stock-microservice-python)

[Machine Learning - Stock Prediction MS](https://github.com/mrkwapo/tensorflow-stock-prediction-ml-model)
