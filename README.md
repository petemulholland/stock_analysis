# Stock Analysis

So I intend to attempt to develop a stock picking application.
I want to start from micro services, using Python.

Services:
* stock picker, to see what's worth attempting to analyse based on some basic analysis
* stock quotes, to retrieve stcok prices for a period of time from some source (maybe yahoo, I intend to look at the chapter in Core Python)

I intend to start from "Python Microservices Development" using flask for the first couple of services, I may want to look at asynchronous python web servers later.

* other services will analyse the stock chart to make recommendations, 
TODO: find the book I was looking at for fitting curves to charts

* I'll need a front end at some point, I'm thinking react, maybe D3.js or something for drawing charts.

TODOS:
* I want to try deploying this on a cluster fo Raspberry Pi 2s, I'll need more than my 4 Rpis for a UAt env & prod env.
* I want to do docker properly, and deploy container
** I need to look into docker swarms on RPi: https://www.raspberrypi.org/blog/docker-comes-to-raspberry-pi/


TODO: complete list of todos, there's a whole bunch more stuff I want to make note of here
