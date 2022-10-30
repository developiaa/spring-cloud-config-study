# 프로젝트 빌드
`mvn clean compile package`

# Docker 이미지 빌드
`docker build -t developiaa/config-service:1.0 .`

# Docker 이미지 업로드
`docker push developiaa/config-service:1.0`

# Docker 실행
`docker run -d -p 8888:8888 --network ecommerce-network -e "spring.rabbitmq.host=rabbitmq_docker" -e "spring.profiles.active=default" --name config-service developiaa/config-service:1.0`

# Kafka docker 실행
`docker-compose -f docker-compose-single-broker.yml up -d`

# Zipkin docker 실행
`docker run -d -p 9411:9411 --network ecommerce-network --name zipkin openzipkin/zipkin `
