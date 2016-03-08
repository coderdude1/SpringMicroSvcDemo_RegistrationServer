# Overview
This project will setup and run a netflix registration server using spring cloud services. This project can 
be used on any microservices implementation with little change (properties).  It
was written to be used in a demo using the AccountService_Demo and the AccountWebClient_Demo.
 
This is an evolution of a springblog post on microservices with spring.  The original source is
[here](https://spring.io/blog/2015/07/14/microservices-with-spring) and provides a great overview of these
pieces and how they work.

I ended up splitting up the original project that had three tiers (registration server, account micro service, and
the client webservice) into three separate projects.   This allowed me to inject the spring config service.
This requires the use of the bootstrap.yml to set the properties, and each app needs to be set separately.

# Discovery Service
The generic spring term is "DiscoveryService".  Netflix provides an opensource implementation
called "Eureka".  There are other impls, such as consul and others.  

REASEARCH: I think that there is a generic annotation for setting up a registration server, and springboot
 looks on the classpath to find If you use the generic wrapper, it changes it's behavior based on 
finding an impl on the classpath (ie the implementation you add to maven).

This demo will use the netflix "EnableEurekaServer" annotation

# Demo
show the RegistrationServer class

# Interesting URLS

1.  [Ngnix article](https://www.nginx.com/blog/introduction-to-microservices/)
2.  [Configuring It All Out" or "12-Factor App-Style Configuration with Spring"](https://spring.io/blog/2015/01/13/configuring-it-all-out-or-12-factor-app-style-configuration-with-spring)
2.  [Spring Cloud Netflix](http://cloud.spring.io/spring-cloud-netflix/spring-cloud-netflix.html)
3.  [Microservices With Spring](https://spring.io/blog/2015/07/14/microservices-with-spring)
4.  [Microservice Registration and Discovery with Spring Cloud and Netflix's Eureka](https://spring.io/blog/2015/01/20/microservice-registration-and-discovery-with-spring-cloud-and-netflix-s-eureka)
5.  [Spring cloud samples git repo](https://github.com/spring-cloud-samples/)
6.  [Configuring it all git repo](https://github.com/joshlong/configuring-it-all-out/blob/master/cloud-client/pom.xml)
7.  [Original Source Microservices with spring](https://spring.io/blog/2015/07/14/microservices-with-spring)

# Misc
Zuul, consul, Hysterix, load balancing, redundant registration server?