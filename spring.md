# Spring framework

* Java Bean
  * Classes which encapsulate many objects into a single object (the bean)
  * Reusable software components
* Spring Bean
  * Objects which form the backbone of an application
  * An object which is instantiated, assembled, and managed by a Spring IoC container
* Bean Scopes
  * Control scope of object created from particular bean definition
  * Control managed through configuration rather than at class level
* Spring Context
  * Also known as Spring IoC containers
  * Responsible for instantiating, configuring, and assembling beans
  * Reads configuration metadata from XML, Java annotations, and/or Java code in configuration files
* Factory method
  * Hides complex creation logic using a single method call
  * Creates an instance method which returns the desired bean
  * Makes use of classes which act as factories to create objects
  * Favours method invocation instead of making direct constructor calls to create objects
* Inversion of Control (IoC)
  * Also known as Dependency Injection
  * Object dependencies are defined through constructor arguments, arguments to a factory method, or properties set on onject instance after constructed or returned from the factory method
  * IoC container injects dependencies when creating a bean
  * It is the inverse of the bean controlling the instantiation or location of its dependencies
* Spring container
  * The core of the Spring framework
  * Used for creating objects and configuring them
* Dependency injection
  * Spring container injects objects into other objects or dependencies
  * Allows for loose coupling of components
  * Move responsibility of managing components into the container
* Component annotation `@Component`
  * Marks a class for dependency injection
  * Responsible for some operations
* Service annotation `@Service`
  * Denotes that the class provides some services
  * Used for business logic
* Repository annotation `@Respository`
  * Indicates that a class deals with CRUD operations
  * Usually used with DAO implementations dealing with database tables
* DAO Design Pattern
  * Data Access Object
  * Used to separate the data persistence logic in a separate layer
  * Allows service to remain separate from low-level operations to access databases
* Controller annotation `@Controller`
  * Mostly used with web applications or REST web services
  * Specifies that the class is a front controller and responsible to handler user requests and return the appropriate response
* RESTful Web Service
  * Respresentational State Transfer
  * Software architectural style
  * Easy to build and consume
  * Defines a set of constraints for how the architecture of web services should behave
* Auotowired annotation `@Autowired`
  * Allows Spring to resolve and inject collaborating beans into a bean
*  Bean annotation `@Bean`
   *  Specifies that a method returns a bean to be managed by Spring Context
*  Configuration annotation `@Configuration`
   *  Used for Spring annotation based configuration
   *  Indicates that a class delcares one or more `@Bean` methods and may be processed by the Spring container to generate bean definitions and service requests for those beans at runtime
*  Qualifier annotation `@Qualifier`
   *  Eliminates issue of which beans needs to be injected
   *  Solves autowire conflicts when there are multiple beans of the same type
*  Primary annotation `@Primary`
   *  Defines preference when when multiple beans of the same type are present
   *  The bean associated with `@Primary` will be used unless otherwisde indicated
*  Lombok
   *  Java library providing a wide range of useful annoations
*  Constructor injection (Lombok)
   *  Explicity pass component dependencies to a constructor
   *  No need to create test-specific configuration component
   *  Provides a consistent design
   *  Simplified unit tests
   *  Allows freedom to use final keywords
   *  Generate constructor for all class fields using `@AllArgsConstructor`
   *  Generate constructor for all final class fields using `@RequiredArgsConstructor`
   *  Generate empty constructor using `@NoArgsCOnstructor`
*  Retry annotation `@Retry`
   *  Used to automatically re-invoke a failed operation
   *  Helpful when errors may be transient (momentary network glitch)
*  Facade pattern
   *  Software design pattern use in object oriented programming
   *  An object which serves as a front facing ionterface masking more complex underlying or structural code
*  SLF4J annotation `@SLF4J`
   *  Logging facade for different logging frameworks such as Log4j
   *  Allows for different logging frameworks to co-exist
*  gRPC
   *  RPC (Remote Procedure Call) framework
   *  Helps eliminate boilerplate code and connect polyglot services and and across data centers
* RPC
  * Software communication protocol
  * Allows services to communicate together without having to understand any network details
  * Used to call other processes on remote systems like a local system
* Protocol Buffers
  * Binary format to serliase data between different services
  * Used to store data and function contracts in the form of a proto file
*  Polyglot Services
   *  Micro service architecture consisting of multuple programming languages and technologies
*  RestController annotation `@RestController`
   *  Simplifies creation of RESTful web services
   *  Combines `@Controller` and `@ResponseBody`
*  ResponseBody annotation `@ResponseBody`
   *  Maps HTTPRequest body to a transfer or domain object
   *  Enables automatic deserialisation of the inbound HttpRequestBody onto a Java object
*  RequestMapping annotation `@RequestMapping`
   *  Maps HTTP requests to handler methods of MVC and REST controllers
*  GetMapping annotation `@GetMapping`
   *  Maps HTTP GET requests to their respective controller methods
*  PreAutorize annoation `@PreAuthorize`
   *  Checks a given expression before entering the method
*  PostAuthorize annotation `@PostAuthorize`
   *  Checks a given expression after the execution of a method and could alter the result
*  hasAuthorithy
   *  Checks if current principal has the specified role
*  Getter and Setter annotations `@Getter` & `@Setter`
   *  Used by Lombok to generate default getter/setter methods for fields