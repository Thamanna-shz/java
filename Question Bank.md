1.  With a neat sketch explain the processes involved in the life cycle of an EJB (10 Marks) Dec 2019,Dec 2018
* The client locates the bean’s home using the JNDI(Java Naming and Directory Interface) services in the application server.
* The JNDI service returns a reference to the client’s Home interface.
* The client uses its Home interface to call home.create(). In response to this call, the Home object creates an EJBObject. A new instance of the code in the bean class is also instantiated by the newInstance() method.
* The new instance of the bean class is given a session context. This instantiation is now called a Session Bean.
* The Home object gives the client’s Remote interface a reference to the EJBObject in the container.
* The client’s Remote interface can now invoke methods on the EJBObject in the container. This EJBObject then passes these method calls to the Session Bean
* The session bean returns a resultset to the EJBObject, which in turn returns it to the client’s Remote interface.

![EJB Life Cycle](/img/1.png)

2. With a neat sketch explain CORBA Architecture (10 Marks) Dec 2018, Dec 2019

* CORBA relies on the protocol Internet InterORB Protocol (IIOP) for communications between objects. 
* The center of the CORBA architecture lies in the Object Request Broker (ORB).
* The ORB is a distributed programming service that enables CORBA objects to locate and communicate with one another.
* CORBA objects have interfaces that expose sets of methods to clients. 
* To request access to an objects method, a CORBA client acquires an object reference to a CORBA server object. 
* Then the client makes method calls on the object reference as if the CORBA object were local to the client.
* The ORB finds the CORBA object and prepares it to receive requests, to communicate requests to it, and then to communicate replies back to the client.

![CORBA](/img/2.png)

3. What are Message Driven Beans?

* The Message-Driven Bean (MDB) is a stateless component that is invoked by a container as a result of the arrival of a JMS message
* A MDB acts as a message consumer, it receives messages from a JMS Topic and performs business logic based on the message contents
* Message-Driven Bean Container Services
    * MDB life cycle management
    * Exception handling
    * Threading and concurrency
    * Message acknowledgment
    * Security






