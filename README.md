# Overview
Setup and run a netflix registration server using spring cloud services.  This code is an evolution
from the Microservices with spring blog (link below) on using the eureka netflix server and spring microservices.
The original had the 3 major pieces in one git repository /intellij project.  THis worked ok, but I wanted to
show the integration with spring config server, and that requires modification to the bootstrap.yml, which 
would not have worked in a single
environment.

# Interesting URLS

1.  [Configuring It All Out" or "12-Factor App-Style Configuration with Spring"](https://spring.io/blog/2015/01/13/configuring-it-all-out-or-12-factor-app-style-configuration-with-spring)
2.  [Spring Cloud Netflix](http://cloud.spring.io/spring-cloud-netflix/spring-cloud-netflix.html)
3.  [Microservices With Spring](https://spring.io/blog/2015/07/14/microservices-with-spring)
4.  [Microservice Registration and Discovery with Spring Cloud and Netflix's Eureka](https://spring.io/blog/2015/01/20/microservice-registration-and-discovery-with-spring-cloud-and-netflix-s-eureka)
5.  [Spring cloud samples git repo](https://github.com/spring-cloud-samples/)
6.  [Configuring it all git repo](https://github.com/joshlong/configuring-it-all-out/blob/master/cloud-client/pom.xml)
7.  Original Source [Microservices with spring](https://spring.io/blog/2015/07/14/microservices-with-spring)

# Discovery Service
The generic spring term is "DiscoveryService".  Netflix provides an opensource implementation
called "RegistrationService".  Spring supports the use of both.  There are other impls, such
as consul and others.  SPring provides annotations for the netflix concrete impl, and for a generic
wrapper over all of them.  If you use the generic wrapper, it changes it's behavior based on 
finding an impl on the classpath (ie the implementation you add to maven).

This demo will use the netflix "EnableEurekaServer" annotation

# Demo
show the RegistrationServer class

# Misc
Zuul, consul, Hysterix, load balancing, redundant registration server?