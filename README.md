docker-apollomq
==============

This project builds a [docker](http://docker.io/) container for running Apache (ActiveMQ) Apollo message broker. STOMP, AMQP, MQTT, Openwire, SSL, and WebSockets are supported.

## Build

Once you have [installed docker](https://www.docker.io/gettingstarted/#h_installation) you should be able to create the containers via the following:

```
git clone https://github.com/pires/docker-apollomq.git
cd docker-apollomq
docker build -t apollomq:1.7 .
```

## Run

Non-secure ports:

```
docker run --name amq1 -p=61613:61613 -p=61613:61623 -p=61680:61680 -d -t apollomq:1.7
```

Secure ports:

```
docker run --name amq1 -p=61614:61614 -p=61624:61624 -p=61681:61681 -d -t apollomq:1.7
```

## Test

Credentials:
```
login: admin
passcode: password
```

Connect as you see fit.