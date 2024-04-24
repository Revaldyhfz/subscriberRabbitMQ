# TUTORIAL 8

## Reflection

1. what is amqp
    - AMQP stands for Advanced Message Queuing Protocol. It is an open standard protocol for message-oriented middleware that enables communication between applications or components in a distributed system.

2. what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for? 
    - The string `guest:guest@localhost:5672` is a part of the URL used to connect to an AMQP (Advanced Message Queuing Protocol) server.

        - `guest:guest`: referes to the username and password used to authenticate with the AMPQ server

        - `localhost:5672`: specifies the hostname and port number of the AMQP server. 

    So, when this URL is used to create a new queue listener (CrosstownBus::new_queue_listener), it tells the listener to connect to an AMQP server running on the local machine, using the username "guest" and password "guest", and communicating over port 5672.

## Preparing Message Broker(RabbitMQ)

1. Simulation Slow Subscriber
![SlowSubscriber](/static/Screenshot5.jpg)

