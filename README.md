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
![SlowSubscriber](/static/Screenshot8.jpg)
    - my total number of queue is 20, this is due to the intentional delay introduced into the subscriber set at 1 second, despite seemingly brief delay, the rapid influx of messages in short amount of time results in the significant spike in delay

2. Running atleast three subscribers

- cargo run 4 times
![threesubscriber](/static/Screenshot6.jpg)

- cargo run 10 times
![ThreeSubscriber3](/static/Screenshot10.jpg)

- the 3 terminal
![threeSubscriber2](/static/Screenshot9.jpg)

from my observation it seems that the delay has reduced down a bit, i also did some test with different amount of queues. It seems like the delay decreases more rapidly compared to the previous scenario, this is because the message broker's distribution of messages among multiple subscriber. As a result, the delay diminishes more swiftly than in the previous setup.

