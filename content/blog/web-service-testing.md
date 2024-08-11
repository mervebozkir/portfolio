---
title: "Web Service Testing"
dateString: Dec 2020
draft: false
tags: ["Software Testing", "Webservice Testing"]
weight: 103
cover:
    image: "/blog/web-service-testing/ws-testing.png"
---

# What is a Web Service?

The most basic definition of a web service is the standard protocols (HTTP or HTTPS) used for communication between systems. This communication is mostly centered around XML and JSON.

Briefly, XML (Extensible Markup Language) is a language that enables the creation of easily readable documents, known in Turkish as Genişletilebilir İşaretleme Dili.

JSON (JavaScript Object Notation), which translates to JavaScript Nesne Notasyonu in Turkish, is a more flexible language compared to XML. It is also one of the languages used for data communication.

Applications and systems written in different programming languages and running on various platforms communicate through JSON or XML, making them independent of any operating system or programming language.

Web services can be examined under the SOAP and REST architectures. Let's briefly touch on these concepts.

![](/blog/web-service-testing/soap-and-rest.png)

**SOAP:** Standing for Simple Object Access Protocol, SOAP is a service protocol that primarily uses the HTTP protocol for communication. It communicates exclusively through XML and is not flexible in this regard.

Although it only supports communication through XML, security controls are easier within SOAP, making it more frequently used when such controls are necessary.

**REST:** Standing for Representational State Transfer, REST is an architecture that also uses the HTTP protocol for communication. However, unlike SOAP, it does not mandate the use of XML. It allows communication using JSON, HTML, or even plain text. This flexibility makes it more preferred.

The amount of data transferred within REST is smaller, making it ideal for applications requiring high performance.

# Web Service Testing

Web service tests hold a significant place among test types and are conducted to check the functionality, performance, and reliability of an application or system. To ensure systems work successfully and data flow is correctly provided, it is necessary to test the web services that supply data to the user interface.

The general working principle of web service tests is the same. The client sends a request, and the server returns an appropriate response based on the received request. It is crucial to ensure the correctness of the fields in the sent request; otherwise, an incorrect response will be returned, leading to a misinterpretation of the test.

Web service tests are similar to unit tests in some aspects but differ in the following way: the development of web service tests is done in a way that supports all versions of the application. Thus, even if a new version of the application is released, regression testing can be performed for both the current and all previous versions. This situation prevents an increase in test time during the development of new parts of the product and ensures usability in older versions of the product without needing changes.

There are many tools available for conducting web service testing. The most common ones are SoapUI, Postman, and JMeter. Web service tests can be performed manually with SoapUI, while Postman and JMeter are more commonly used for automating web service tests.

In this article, I briefly introduced web services and discussed the purposes of web service testing. See you in future articles :)

![](/blog/web-service-testing/ws-testing2.png)

*SOURCES*

- https://www.tutorialspoint.com/webservices/what_are_web_services.htm
- https://www.guru99.com/webservice-testing-beginner-guide.html

[Medium](https://mervebozkir.medium.com/web-servi%CC%87s-ve-web-servi%CC%87s-testi%CC%87-8e0057a5c1b7)