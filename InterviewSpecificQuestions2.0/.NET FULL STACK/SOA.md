## Technical

1. What is SOA?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

SOA is an architecture for building applications using reusable, interoperable services which have well-defined business functionalities and can be orchestrated to achieve a specific functionality by utilizing them together.

</blockquote>

</details>

---

2. What are ends, contracts, addresses, and bindings?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The service can be made available to clients from different ends. All these services must be exposed through one of these ends.

The end will consist of the following:

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

