# nodejs-microservices-1

eureka-curl-payload.json

{
    "instance": {
        "hostName": "localhost",
        "app": "MY-SERVICE",
        "vipAddress": "my-service",
        "instanceId": "unique-instance-id",
        "ipAddr": "0.0.0.0",
        "status": "UP",
        "port": {
            "$": 8585,
            "@enabled": true
        },
        "dataCenterInfo": {
            "@class": "com.netflix.appinfo.InstanceInfo$DefaultDataCenterInfo",
            "name": "MyOwn"
        }
    }
}

curl -i --request POST --header "Content-Type: application/json" --data @eureka-curl-payload.json http://localhost:8761/eureka/apps/my-service

https://www.twilio.com/blog/eureka-zuul-service-discovery-dynamic-routing-javascript-microservices-node-js
https://thenewstack.io/implementing-service-discovery-of-microservices-with-consul/
https://www.tutorialspoint.com/consul/consul_introduction.htm
