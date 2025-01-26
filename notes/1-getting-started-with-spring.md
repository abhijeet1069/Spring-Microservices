# Spring

At its core, Spring offers a container, often referred to as the Spring application context, that creates and manages
application components.

## Benefits of Spring platform

Examples of how you, as an application developer, can benefit from the Spring platform:

- Make a Java method execute in a database transaction without having to deal with transaction APIs.
- Make a local Java method an HTTP endpoint without having to deal with the Servlet API.
- Make a local Java method a message handler without having to deal with the JMS API.
- Make a local Java method a management operation without having to deal with the JMX API.

## Spring MVC

The controller is responsible for handling user input, processing it, and determining what response to send back.

- Annotation-Based Controllers : Spring uses annotations like @Controller and @RestController to define controllers.
- Request Mapping : The @RequestMapping (or its shortcuts like @GetMapping, @PostMapping, etc.) maps URLs to specific
                    handler methods.
- Parameter Binding: Automatically maps request parameters to method arguments using annotations like @RequestParam,
                     @PathVariable, and @RequestBody.

The view is responsible for presenting data to the user. It takes the model data and renders it in a suitable format,
such as HTML, JSON, XML, etc.

- View Resolver : Spring uses a ViewResolver to map logical view names (e.g., "hello") to actual view files
                (e.g., hello.html or hello.jsp).
- Template Engines: Popular engines like Thymeleaf, JSP, and FreeMarker are used to render views.

## Taco-Cloud

- devtools
- thymeleaf
- web
