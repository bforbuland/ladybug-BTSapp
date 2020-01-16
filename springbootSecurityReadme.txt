





*****Back-End*****

File location: /ladybug-app/src/main/java/spring/ladybug/ladybugapp/config/SecurityConfig.java

line16:	1.requests matched against /css/** and /index are fully accessible

line17:	2.requests matched against /user/** require a user to be authenticated and must be associated to the USER role

line20:	3.form-based authentication is enabled with a custom login page and failure url

line24:	The name of the configureGlobal method is not important. However, it is important to only configure AuthenticationManagerBuilder in a class annotated with either @EnableWebSecurity, @EnableGlobalMethodSecurity, or @EnableGlobalAuthentication. Doing otherwise has unpredictable results.


File location: /ladybug-app/pom.xml
line80:1.We are using Thymeleaf for our view template engine and need to add an additional dependency for the Thymeleaf - Spring Security integration module. 






*****Front-End*****

File Location: ./springbootSecurityFrontEndConfig

	1.Displays the Thymeleaf fragment (DOM Node) if the current user has been authenticated.
	2.Displays the name of the currently authenticated principal.
	3.Displays the authorities of the currently authenticated principal.
	4.The logout form.


Note: Thymeleaf will automatically add the CSRF token to our logout form. If we were not using Thymleaf or Spring MVCs taglib we could also manually add the CSRF token using <input type="hidden" name="${_csrf.parameterName}" value="${_csrf.token}"/>.
