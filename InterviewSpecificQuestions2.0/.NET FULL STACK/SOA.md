## Technical

1. What is SOA?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

SOA is an architecture for building applications using reusable, interoperable services which have well-defined business functionalities and can be orchestrated to achieve a specific functionality by utilizing them together.

</blockquote>

</details>

---

2. What are endpoints ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The service can be made available to clients from different ends. All these services must be exposed through one of these ends.

The endpoints will consist of the following:

- **Contract**: It is an agreement that is agreed upon between two parties. It defines how clients are expected to communicate. It specifies the different parameters and returns values that are to be used.
- **Address**: This specifies where a user can find a service. There is an address URL that points to the location of services.
- **Binding**: This determines how to access the end. It specifies the process for communication and how it is to be done.

</blockquote>

</details>

---

3. What is the difference between SOA and Web Service?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Service Oriented Architecture, as the name says is an architectural concept which focuses on having different services communicating with each other to carry out a bigger job.

Thus, a web service is a basic building block in an SOA. When multiple services are combined, we have an application that falls under SOA.

The best example would be any big application which uses Amazon Web Services where you have distinct server instances for your business logic, data hosting and load-balancing requests. Each instance provides its own unique service like load balancer distributes load, and business logic transforms user input and processes it with its logic which in turn provides this transformed data to the database instance for storing.

</blockquote>

</details>

---

4. What is a reusable service?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

It is an autonomous, reusable, discoverable, stateless functionality that has the necessary granularity, and can be part of a composite application or a composite service. A reusable service should be identified with a business activity described by the service specifications (design-time contract).

</blockquote>

</details>

---

5. How to achieve loose coupling in SOA? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- To achieve loose coupling, you can use a service interface like WSDL for a SOAP web service. To limit the dependency, we can hide the service implementation from the consumer. 
- Loose coupling can be handled by encapsulating different functionalities in a way which it will limit the impact of changes to the implementation of different service interfaces. 
- We may even have to change the interface and manage versioning without impacting the customers. Also, one can manage multiple security constraints, multiple means of transport, and other specifications.

</blockquote>

</details>

---

6. Can you explain the SOA Principles?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

**Standardized service contract**: Services adhere to a communications agreement, as defined collectively by one or more service-description documents.
**Service loose coupling**: Services maintain a relationship that minimizes dependencies and only requires that they maintain an awareness of each other.
**Service abstraction**: Beyond descriptions in the service contract, services hide logic from the outside world.
**Service reusability**: Logic is divided into services with the intention of promoting reuse.
**Service autonomy**: Services have control over the logic they encapsulate.
**Service statelessness**: Services minimize resource consumption by deferring the management of state information when necessary
**Service discoverability**: Services are supplemented with communicative metadata by which they can be effectively discovered and interpreted.
**Service composability**: Services are effective composition participants, regardless of the size and complexity of the composition.

</blockquote>

</details>

---

7. What is the difference between Monolithic, SOA and Micro services Architecture?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

Monolithic Architecture is similar to a big container wherein all the software components of an application are assembled together and tightly packaged.

A Service-Oriented Architecture is a collection of services which communicate with each other. The communication can involve either simple data passing or it could involve two or more services coordinating some activity.

Microservice Architecture is an architectural style that structures an application as a collection of small autonomous services, modeled around a business domain.
  
</blockquote>

</details>

---

8. What is WSDL File?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
  
WSDL stands for Web Services Description Language. It is the standard format for describing a web service. WSDL was developed jointly by Microsoft and IBM.

Features of WSDL
WSDL is an XML-based protocol for information exchange in decentralized and distributed environments.

WSDL definitions describe how to access a web service and what operations it will perform.

WSDL is a language for describing how to interface with XML-based services.

WSDL is an integral part of Universal Description, Discovery, and Integration (UDDI), an XML-based worldwide business registry.

WSDL is the language that UDDI uses.

WSDL is pronounced as 'wiz-dull' and spelled out as 'W-S-D-L'.  
</blockquote>

</details>

---

9. Explain SOAP Message Structure ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
  
A SOAP message is an ordinary XML document containing the following elements −

Envelope − Defines the start and the end of the message. It is a mandatory element.

Header − Contains any optional attributes of the message used in processing the message, either at an intermediary point or at the ultimate end-point. It is an optional element.

Body − Contains the XML data comprising the message being sent. It is a mandatory element.

Fault − An optional Fault element that provides information about errors that occur while processing the message. 
  
<?xml version = "1.0"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV = "http://www.w3.org/2001/12/soap-envelope" 
   SOAP-ENV:encodingStyle = "http://www.w3.org/2001/12/soap-encoding">

   <SOAP-ENV:Header>
      ...
      ...
   </SOAP-ENV:Header>
   <SOAP-ENV:Body>
      ...
      ...
      <SOAP-ENV:Fault>
         ...
         ...
      </SOAP-ENV:Fault>
      ...
   </SOAP-ENV:Body>
</SOAP_ENV:Envelope>
  
</blockquote>

</details>

---

10. What’s the difference between services and components?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>
  
Services are logical grouping of components to achieve a business functionality. Components are implementation approaches to make a service. The components can be in Java, C#, C++ but the services will be exposed in a general format like Web Services.  
  
</blockquote>

</details>

---




