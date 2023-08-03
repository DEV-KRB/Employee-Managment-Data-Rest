# Employee-Managment
# A working Spring boot project using Data rest

What has changed?

If dont want to use Dao then add JPA Repository interface and replace dao.
If dont want to use Service and Controller then replace them with Spring Data Rest. Add below dependency
			<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-rest</artifactId>
		</dependency>
		<dependency>
		
	Add Spring Data Rest Properties in application.properties
	spring.data.rest.base-path=/magic-api
	run http://localhost:8080/employees
	GET- http://localhost:8080/magic-api/employees
	POST- http://localhost:8080/magic-api/employees
	PUT- http://localhost:8080/magic-api/employees/13
	DELETE- http://localhost:8080/magic-api/employees/13
	
	Configuration
	It add 's' automatically to the entity. You can also give path for your URL

	@RepositoryRestResource(path="members") annotation at top of Repository interface
	
	Pagination
	# change default page size
	spring.data.rest.default-page-size=3
	
	Sorting
	http://localhost:8080/magic-api/members?sort=age ---default in ascending
	http://localhost:8080/magic-api/members?sort=age ---in descending
