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
* Spring container
  * The core of the Spring framework
  * Used for creating objects and configuring them
* Dependency injection
  * Spring container injects objects into other objects or dependencies
  * Allows for loose coupling of components
  * Move responsibility of managing components into the container
* Component annotation `@Component`
  * Marks a class for dependency injection
* Auotowired annotation `@Autowired`
  * Allows Spring to resolve and inject collaborating beans into a bean
*  Bean annotation `@Bean`
   *  Specifies that a method returns a bean to be managed by Spring Context
*  Configuration annotation `@Configuration`
   *  Used for Spring annotation based configuration
   *  Indicates that a class delcares one or more `@Bean` methods and may be processed by the Spring container to generate bean definitions and service requests for those beans at runtime
*  Qualifier annotation `@Qualifier`
   *  Eliminates issue of which beans needs to be injected
*  Primary annotation `@Primary`
   *  Defines preference when when multiple beans of the same type are present
   *  The bean associated with `@Primary` will be used unless otherwisde indicated
*  Constructor injection (Lombok)
   *  Explicity pass component dependencies to a constructor
   *  No need to create test-specific configuration component
   *  Provides a consistent design
   *  Simplified unit tests
   *  Allows freedom to use final keywords
   *  Generate constructor for all class fields using `@AllArgsConstructor`
   *  Generate constructor for all final class fields using `@RequiredArgsConstructor`
   *  Generate empty constructor using `@NoArgsCOnstructor`