# Stock Pal 
<p align="center">
  <img src="https://github.com/mrkwapo/StockPal-MS/blob/master/stock%20pal%20architecture.jpg">
</p>

## Synopsis
Stock Pal is a Microservices Architecture design concept. This application provides regular users with historic, current and predicted stock data. 

## Design Architecture Concept
API Gateway design pattern. The API Gateway is the single point of entry for any microservice call when users fetch historic, current and predicted data. Machine Learning is used to make predications of future stock prices. Only admins have the ability to persist historic Big Data from a csv file to the database. The Big Data feature is multi-threaded to optimize performance in terms of speed and time complexity.

## Construction
The architecture has multiple servers and seperate databases. Registered users, including admin, are authenticated and authorized through the gateway in conjunction with the auth microservice. Guest users can only search for current and historic stock records in which requests are also sent through the API Gateway.

## Architecture Technology and Languages used 
* Zuul (API Gateway)
* Eureka (Discovery Server) 
* PostgreSQL
* Spring Batch & TaskExecutor (Dependencies used for optimizing Big Data persistence)
* Spring Boot
* Spring Security (Authorization and Authentication)
* JDBC (Database Driver)
* Java (Primary Language)
* Python (Secondary Language used for Data Preprocessing, API Consumption and Machine Learning Model)
* Flask (for Python API Development)

## Links to each Microservice:

[API Gateway MS](https://bit.ly/2NgiICN)

[Auth MS](https://bit.ly/3hxvvP1)

[Eureka Discovery Server](https://bit.ly/2YJruyn)

[Persist Big Data MS](https://bit.ly/2YJqDh9)

[Current Data MS](https://bit.ly/30U4Oyd)

[Machine Learning - Stock Prediction MS](https://bit.ly/2UToo9Y)
