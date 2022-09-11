# RabbitMq

It's a message-oriented middleware, that implement [AMQP](https://www.amqp.org/)

## Docker compose installation

This is an example made for myself, using the following [guide](https://x-team.com/blog/set-up-rabbitmq-with-docker-compose/) [Note: This is only for test the image]

```yaml
version: "3.2"
services:
  rabbitmq:
    image: rabbitmq:3-management-alpine
    container_name: 'rabbitmq'
    user: "1000"
    ports:
        - 5672:5672
        - 15672:15672
    volumes:
        - ./rabbitmq/data/:/var/lib/rabbitmq/
        - ./rabbitmq/log/:/var/log/rabbitmq
    networks:
        - rabbitmq_go_net

networks:
  rabbitmq_go_net:
    driver: bridge
```