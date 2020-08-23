# spring cloud microservices

### Limits Service


### Spring Cloud Config Server
- Server that fetch config from local git repo
- http://localhost:8888/limits-service/dev
- http://localhost:8888/limits-service/qa
- ... (many other environment)

### Currency Exchange Service
- http://localhost:8000/currency-exchange/from/AUD/to/INR
- http://localhost:8001/currency-exchange/from/AUD/to/INR
- ... (many other ports)

### Currency Conversion Service
- http://localhost:8100/currency-converter-feign/from/USD/to/INR/quantity/1000

### Git Local Config Repo
- Host config for multiple microservices and their different environment.
- Git init and commit the changes to make the config effective.

### Netflix Eureka naming server
- http://localhost:8761/

### Netflix Zuul api gateway server
- http://localhost:8765/currency-exchange-service/currency-exchange/from/AUD/to/INR
- http://localhost:8765/currency-conversion-service/currency-converter-feign/from/USD/to/INR/quantity/1000 (check the Zuul filtering log, this will trigger the first api as well)

### Spring Cloud Sleuth
- Generate global UUID for tracing. UUID is shown in logging for each server with Sleuth enabled.

### Spring Cloud Zipkin
- Install and launch Zipkin (https://zipkin.io/pages/quickstart and then http://127.0.0.1:9411/zipkin/)

### RabbitMQ
- Install and launch RabbitMQ (https://www.rabbitmq.com/install-homebrew.html and then /usr/local/sbin/rabbitmq-server)
