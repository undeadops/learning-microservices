# Learning Micro Services
Playing with Ideas of Multiple Python Flask Micro-Services(I'm open to using Go as well), utilizing MongoDB, consul, NSQ, and several MicroServices

## Idea's built into this project

Purpose of this is to demonstrate service discovery/registration, and multiple "micro" services.

Code is in no way production quality

I'm not a full time developer, just an Ops person with lots of interest in scaleable infrastructure/apps
and infrastructure as code.  I will be using this project and sub projects to test ideas/thoughts on how
service discovery works, monitoring of infrastructure and applications, as well as something to demo to
people to help explain ideas behind those concepts.  I want to keep the code small as possible to remain
easy to explain. Also, in some of the services, I intend on adding bottlenecks. Because this would not
be used in full scale production environments, I need ways of faking scale with those bottlenecks by
writing single threaded blocking services in areas I believe would have bottlenecks in a full scale
environment.  

Pull Requests welcome!


### Service Names and their purpose

 - mongo - MongoDB Data store, want to leverage some data analytics/map reduce functionaly from it.
 - brown - NSQ - Message Queue - Used for Async processing between services
 - vinzclortho - Consul - Service Discovery
 - registrator - registrator - Service Registration - to be run per host
 - inkslinger - Python App - Pulling Data from Twitter Developer API
 - slientbob - Python App - Dealing Messages off NSQ - Dealing to dredd and giles
 - dredd - Python App - Sentiment Analysis REST API currently (may change to background async worker), potentially more
 - giles - Python App - Data Access Layer REST API - Single interface to MongoDB
