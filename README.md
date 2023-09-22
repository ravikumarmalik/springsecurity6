# Spring Security along with JWT,OAUTH2



## Topics covered in the course

* Spring Security framework details and it features
* How to adapt security for a Java web application using Spring Security
* Password Management in Spring Security with PasswordEncoders
* Deep dive about encoding, encryption and hashing
* What is CSRF, CORS and how to address them
* What is Authentication and Authorization. How they are different from each other.
* Securing endpoint URLs inside web applications using Ant, MVC & Regex Matchers
* Filters in Spring Security and how to write own custom filters
* Deep dive about JWT (JSON Web Tokens) and the role of them inside Authentication & Authorization
* Deep dive about OAUTH2 and various grant type flows inside OAUTH2.
* Deep dive about OpenID Connect & how it is related to OAUTH2
* Applying authorization rules using roles, authorities inside a web application using Spring Security
* Method level security in web/non-web applications
* Social Login integrations into web applications
* Set up of Authorization Server using KeyCloak 

## Pre-requisite for the course
- Good understanding on Java and Spring concepts
- Basic understanding on SpringBoot & REST services is a bonus but not mandatory
- Interest to learn and explore about Spring Security

# Important Links

- Spring website to generate projects - https://start.spring.io/
- Spring Website - https://spring.io/
- Spring Projects website - https://spring.io/projects
- Spring Boot properties - https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html
- AWS website - https://aws.amazon.com/
- SQLECTRON website - https://sqlectron.github.io
- Free MySQL DB website - https://www.freemysqlhosting.net
- OAuth2 Website - https://oauth.net/2/
- OAuth2 playground - https://www.oauth.com/playground/
- KeyCloak website - https://www.keycloak.org
- KeyCloak Download page - https://www.keycloak.org/downloads
- KeyCloak setup - https://www.keycloak.org/getting-started/getting-started-zip
- KeyCloak guides - https://www.keycloak.org/guides
- KeyCloak Well known APIs - http://localhost:8180/realms/eazybankdev/.well-known/openid-configuration
- Angular Keycloak library - https://www.npmjs.com/package/keycloak-angular
- Keycloak official documentation - https://www.keycloak.org/documentation
- Keycloak Admin REST APIs - https://www.keycloak.org/docs-api/19.0.2/rest-api/index.html








# =======================SPRING SECURITY======================================

# What is spring security ?
Spring Security is a powerful and highly customizable security framework for building Java-based applications. It is a part of the larger Spring Framework, which provides comprehensive infrastructure support for developing Java applications. Spring Security focuses specifically on addressing security concerns within your application, making it easier to implement features like authentication, authorization, and protection against common security vulnerabilities.

Key features and components of Spring Security include:

# Authentication: 
Spring Security provides a wide range of authentication mechanisms, including username/password, OAuth, OpenID, and more. It can integrate with various data sources for user credential validation, such as databases, LDAP servers, and custom implementations.

# Authorization:
It allows you to control access to specific resources or actions within your application based on user roles and permissions. You can configure fine-grained access control rules through expressions or annotations.

# Security Filters: 
Spring Security uses a series of filters to intercept incoming HTTP requests and apply security checks. These filters handle tasks such as authentication, session management, CSRF protection, and more.

# Session Management: You can configure and manage user sessions, including handling session fixation attacks, tracking active sessions, and specifying session timeout policies.

# Cross-Site Request Forgery (CSRF) Protection:
Spring Security provides built-in CSRF protection to prevent common web application security vulnerabilities related to cross-site request forgery.

# Remember-Me Authentication: 
This feature allows users to opt for persistent login sessions, so they don't need to re-enter their credentials each time they visit your site.

Integration with Other Security Standards: Spring Security integrates seamlessly with other security standards and protocols, such as OAuth 2.0, OpenID Connect, SAML, and more, making it suitable for building secure, identity-aware applications.

# Customization: 
Spring Security is highly customizable. You can configure security settings through XML or Java-based configuration, and it provides hooks for implementing custom authentication providers, access decision strategies, and more.

# Multi-Layered Security: 
You can implement security at multiple layers of your application, including method-level security for business logic, URL-level security for web resources, and data-level security for database records.

# Community and Ecosystem: 
Spring Security has a strong community and is well-documented. It also integrates well with other Spring projects, such as Spring Boot, making it easy to build secure applications quickly.

Overall, Spring Security is a valuable tool for developers who want to ensure the security of their Java applications, whether they are building web applications, RESTful APIs, or other types of software. It simplifies many common security tasks and provides a robust foundation for implementing a wide range of security features.

# How many types of spring security ?

 Spring Security provides several modules and extensions that cater to different use cases and requirements. The main types or modules of Spring Security include:

# Core Spring Security:
This is the foundation of Spring Security and includes essential features like authentication, authorization, and security filters. It provides the basic building blocks for securing applications.

# Spring Security Web:
This module focuses on securing web applications. It includes features such as URL-level security, CSRF protection, session management, and integration with various web frameworks like Spring MVC and Apache Shiro.

# Spring Security OAuth: 
This module adds OAuth 2.0 support to Spring Security, allowing you to implement OAuth 2.0-based authentication and authorization in your applications. It's essential for building secure APIs and enabling third-party authentication.

# Spring Security SAML: 
This module enables Security Assertion Markup Language (SAML) support in Spring Security. SAML is often used for single sign-on (SSO) in enterprise applications.

# Spring Security JWT: 
While not an official module, JSON Web Tokens (JWT) can be integrated with Spring Security to implement stateless authentication in RESTful APIs. JWTs are often used in microservices and distributed systems.

# Spring Security LDAP: 
This module provides support for authenticating and authorizing users against Lightweight Directory Access Protocol (LDAP) servers. It's useful in environments where LDAP is the user directory.

# Spring Security ACL (Access Control Lists): 
This module allows you to implement fine-grained, object-level security by defining access control lists for domain objects. It's suitable for applications that require complex access control rules.

# Spring Security Kerberos: 
This module enables integration with Kerberos authentication, which is commonly used in enterprise environments for single sign-on.

# Spring Security CAS (Central Authentication Service): 
CAS is a single sign-on protocol, and this module allows Spring Security to integrate with CAS servers to provide SSO capabilities.

# Spring Security Test: 
While not a standalone module, Spring Security Test provides utilities and support for testing Spring Security configurations and verifying authentication and authorization behavior in unit and integration tests.

These modules offer different security solutions and can be combined as needed to address specific security requirements in your application. The choice of which module(s) to use depends on your application's architecture, security needs, and integration requirements. Spring Security's modular design allows you to pick and choose the components that best suit your project.


# Advantages 

Spring Security offers several advantages for securing your Java-based applications, whether they are web applications, RESTful APIs, microservices, or other types of software. Here are some of the key advantages of using Spring Security:

# Comprehensive Security Features: 
Spring Security provides a wide range of security features, including authentication, authorization, session management, CSRF protection, and more, allowing you to address various security concerns within your application.

# Customizability:
It is highly customizable and can be tailored to fit the specific security requirements of your application. You can configure security settings through XML or Java-based configuration and implement custom authentication providers, access control strategies, and error handling.

#Modular Design:
Spring Security follows a modular design, making it easy to integrate and configure only the components you need for your project. This modularity helps keep your codebase clean and reduces unnecessary complexity.

# Integration with Other Spring Projects:
Spring Security seamlessly integrates with other Spring projects, such as Spring Framework and Spring Boot. This integration allows for the development of cohesive and well-structured applications.

# Community and Documentation: 
Spring Security benefits from a large and active community, which means you can find extensive documentation, tutorials, and community support to help you implement security best practices.

# Support for Multiple Authentication Mechanisms:
It supports various authentication mechanisms, including username/password, LDAP, OAuth, OpenID, and more. This flexibility allows you to choose the authentication method that best suits your application's needs.

# Fine-Grained Authorization:
Spring Security enables you to define fine-grained access control rules based on user roles and permissions, making it possible to control who can access specific resources or perform certain actions in your application.

# Protection Against Common Security Vulnerabilities: 
It includes built-in protection against common web security vulnerabilities like Cross-Site Request Forgery (CSRF), Cross-Site Scripting (XSS), and session fixation attacks.

# Session Management: 
You can configure and manage user sessions, including session fixation protection, concurrent session control, and session timeout policies.

# Security Testing Support: 
Spring Security provides utilities for testing security configurations and validating authentication and authorization rules in unit and integration tests, aiding in the development of secure applications.

# Integration with Security Standards:
It integrates seamlessly with various security standards and protocols, such as OAuth 2.0, OpenID Connect, SAML, and more, making it suitable for building secure applications that support single sign-on (SSO) and third-party authentication.

# Scalability: 
Spring Security can be used in large-scale applications and microservices architectures, ensuring that your security measures can grow with your application's demands.

# Legacy System Integration:
It supports integration with legacy authentication and authorization systems, allowing you to secure older applications without a full rewrite.

In summary, Spring Security provides a robust and flexible framework for implementing security measures in Java applications. Its extensive feature set, customizability, and integration capabilities make it a popular choice for developers looking to build secure and maintainable software.



# ====================

# What is Spring Security, and why is it essential in web application development?

Answer: Spring Security is a framework that provides comprehensive security features for Java-based applications. It is crucial in web development to safeguard applications against unauthorized access, data breaches, and other security threats.

# Explain the difference between authentication and authorization in the context of Spring Security.

Answer: Authentication is the process of verifying a user's identity, while authorization is the process of determining whether an authenticated user has permission to perform a specific action or access a particular resource.

# How do you configure Spring Security in a Spring Boot application?

Answer: In a Spring Boot application, you typically include the spring-boot-starter-security dependency and configure security settings in the SecurityConfig class by extending SecurityConfigurerAdapter.

# What is the default authentication mechanism in Spring Security, and how can you change it?

Answer: The default authentication mechanism in Spring Security is username/password-based authentication using a UserDetailsService. You can change it by configuring a different AuthenticationProvider and UserDetailsService implementation.

# What is the purpose of the AuthenticationManager in Spring Security, and how do you configure it?

Answer: The AuthenticationManager is responsible for performing authentication. You can configure it in Spring Security by defining authentication providers and specifying how user credentials are checked.

# How can you enable HTTP Basic and Form-Based authentication in a Spring Security configuration?

Answer: You can enable HTTP Basic authentication by configuring httpBasic(), and Form-Based authentication can be enabled using formLogin() in the security configuration.

# Explain the role of the Spring Security Filter Chain.

Answer: The Spring Security Filter Chain is a series of security filters that process incoming HTTP requests. These filters handle tasks like authentication, authorization, CSRF protection, and more.

# What is CSRF protection in Spring Security, and why is it important?

Answer: CSRF (Cross-Site Request Forgery) protection prevents malicious websites from executing actions on behalf of an authenticated user. Spring Security provides CSRF protection by default.

# How do you configure session management in Spring Security, and what are the options for session fixation protection?

Answer: You can configure session management in Spring Security using sessionManagement(). Session fixation protection options include changing the session ID, invalidating the old session, or allowing only one session per user.

# What is Single Sign-On (SSO), and how can Spring Security be used to implement it?

Answer: SSO allows users to log in once and access multiple applications. Spring Security can implement SSO using protocols like OAuth 2.0, OpenID Connect, or integrating with SSO solutions like CAS or SAML.

These questions and answers should help you assess a candidate's knowledge and understanding of Spring Security during interviews. Depending on the role and the candidate's experience level, you can adjust the complexity of the questions accordingly.
