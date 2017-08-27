# Stock Analysis

So I intend to attempt to develop a stock picking application.
* I want to start from micro services, using Python.
* I want to do docker correctly and deploy containers to a cluster of RPis at home.
* I want SemVer versioning of all services with auto updating.
* I want PEP 8 enforcement
* I want service monitoring with observable metrics
* I want to do Python logging correctly
* I want CI/CD

## The services:
I'll need 2 services first, 1 to pick stocks that are worth getting prices for, and the second to get the price history for the stock picked by the first. I intend to try fitting some curves to stock charts, so i'll need price history.

* Stock picker, to see what's worth attempting to analyse based on some basic analysis.
  So I'll probably start by excluding penny stocks, then do some basic check like PE ratio or something
* Stock quotes, to retrieve stock prices for a period of time from some source (maybe yahoo, I intend to look at the chapter in ```Core Python```)

I intend to start from ```Python Microservices Development``` using flask for the first couple of services, I may want to look at asynchronous python web servers later.

* other services will perform some analysis on the stock to make recommendations, 
**TODO:** find the book I was looking at for fitting curves to charts

* I'll need a front end at some point, I'm thinking react, maybe D3.js or something for drawing charts.

## TODOS:
- [ ] I want to try deploying this on a cluster of Raspberry Pi 2s, I'll need more than my 4 Rpis for a UAT env & prod env, but there's no rush, i'll need to get something going first
- [ ] I want to do docker properly, and deploy containers
  - [ ] I need to look into docker swarms on RPi: https://www.raspberrypi.org/blog/docker-comes-to-raspberry-pi/
  - [ ] Look up Codefresh: ``` a docker native CI/CD platform```
  - [ ] Look into Habitat from Chef for service Choreography
  - [ ] look into docker-gc for cleaning up images/volumes
- [ ] I'll need observable metrics for all services
  - do I get that with a few lines to plug in prometheus - need to follow up on Observables talk at http://shipitcon.com/speakers/ 2017
- [ ] I'll want all services logging to a central location - need to look into the logging tutorials to do this right
- [ ] Can I do Pep 8 precommit hooks? if i create a precommit hook on github, does it come down to the local clone?
- [ ] can I use chef to reimage the sds for the rpis? or to update the images on the rpis?
- [ ] I want semvers on each service with updates on good builds
