---
{}
---
   
**What is WCF?**     
**WCF** stands for **Windows Communication Foundation** and is part of .NET 3.0. WCF is Microsoft platform for building distributed and interoperable applications.     
     
     
     
**What is a distributed application?**     
In simple terms a distributed application, is an application where parts of it run on 2 or more computers. **Distributed applications** are also called as **connected systems.**     
     
**Examples:**     
A web application running on one machine and a web service that this application is consuming is running on another machine.     
![Distributed System](https://1.bp.blogspot.com/-LkoamBJfsSQ/UofZ3J6jx1I/AAAAAAAAHck/oAxSs9dSCcA/s1600/Distributed+System.png)     
     
An enterprise web application may have the following tiers, and each tier may be running on a different machine     
1. Presentation tier     
2. Business tier     
3. Data Access tier     
![Connected System](https://2.bp.blogspot.com/-O0N8uAnU0fg/UofdGKhX6yI/AAAAAAAAHdQ/gRiiR5b2YDY/s1600/Connected+System.png)     
     
**Why build distributed applications?**     
There are several reasons for this     
**1.** An enterprise application may need to use the services provided by other enterprises. For example an ecommerce application may be using Paypal service for payments.     
**2.** For better scalability. An enterprise web application may have Presentation tier, Business tier, and Data Access tier, and each tier may be running on a different machine.     
     
**What is an interoperable application?**     
An application that can communicate with any other application that is built on any platform and using any programming language is called as an interoperable application. Web services are interoperable, where as .NET remoting services are not.     
     
Web services can communicate with any application built on any platform, where as a .NET remoting service can be consumed only by a .net application.     
     
**What technology choices did we have before WCF to build distributed applications?**     
Enterprise Services     
Dot Net Remoting     
Web Services     
     
**Why should we use WCF?**     
Let's take this scenario     
**We have 2 clients and we need to implement a service a for them.**      
**1.** The first client is using a Java application to interact with our service, so for interoperability this client wants messages to be in **XML format** and the protocol to be **HTTP.**     
**2.** The second client uses .NET, so for better performance this client wants messages formatted in **binary** over **TCP protocol**.     
     
**Without WCF**     
**1.** To satisfy the first client requirement we end up implementing an ASMX web service, and     
![asp.net web service example](https://2.bp.blogspot.com/-zldxQC3WJ70/UofdjIeTZ4I/AAAAAAAAHdY/F06xA5kLbMM/s1600/asp.net+web+service+example.png)     
     
2. To satisfy the second client requirement we end up implementing a remoting service     
![Dot Net Remoting Example](https://4.bp.blogspot.com/-vZhCr7hVfI4/Uofd8kuyigI/AAAAAAAAHdg/Nzc6OqaWEJ4/s1600/Dot+Net+Remoting+Example.png)     
     
These are 2 different technologies, and have **complete different programming models.** So the developers have to learn different technologies.      
     
So to **unify and bring all these technologies under one roof** Microsoft has come up with a single programming model that is called as **WCF - Windows Communication Foundation.**     
     
**With WCF,**     
You implement one service and we can configure as many end points as want to support all the client needs. To support the above 2 client requirements, we would configure 2 end points. In the endpoint configuration we can specify the protocols and message formats that we want to use.     
![WCF Example](https://4.bp.blogspot.com/-4j1EGHIUjAA/UofeSXiSIwI/AAAAAAAAHdo/zC5juwDP5IA/s1600/WCF+Example.png)