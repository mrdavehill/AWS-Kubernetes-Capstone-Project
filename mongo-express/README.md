 docker build . -t mongo-express
 docker tag mongo-express mrdavehill/mongo-express:v1.0
 docker push mrdavehill/mongo-express:v1.0