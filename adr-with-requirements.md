**Title**: Database Selection for Food Delivery Application

**Status**: Accepted

**Context**: Our food delivery application requires a scalable and efficient database to manage orders, restaurants, menus, 
and customer information. We need to select a suitable database system that meets our performance, scalability, and 
maintenance requirements.

**Problem**: As a team, we're struggling with the decision on which database to use for this project. We've got some 
experience with relational databases like MySQL and PostgreSQL but are not sure if they'll be sufficient for this 
application's needs. We also want to consider other options that might provide better scalability or features.


**Requirements**:

* **Performance Requirements**:
	+ Handle up to 10,000 concurrent users
	+ Process an average of 100 orders per minute during peak hours
	+ Achieve a query response time of under 50ms for critical business logic queries
* **Scalability Requirements**:
	+ Support a minimum of 5x growth in database size and traffic over the next 2 years
	+ Handle a maximum of 10,000 concurrent connections without performance degradation
	+ Enable seamless vertical scaling with additional storage or compute resources
* **Maintenance Requirements**:
	+ Perform daily backups and rollbacks for data integrity and recovery purposes
	+ Implement monitoring and alerting to detect potential issues before they become critical
	+ Provide a secure and auditable environment for sensitive customer information


**Decision**: Based on initial research, we will use SQLite as our primary database for the food delivery application. 
While it may not be the most powerful or scalable option, it meets our basic requirements and provides a simple solution to 
get us started.

**Rationale**:

* **Easy setup and configuration**: SQLite has an extremely lightweight footprint, making it easy to set up and integrate 
with our application.
* **Limited scalability concerns**: With our initial projections, we don't anticipate large volumes of data or intense 
performance demands. SQLite should be sufficient for our starting point.
* **Low resource overhead**: By using SQLite, we'll avoid the overhead associated with larger databases like MySQL or 
PostgreSQL.

**Consequences**:

* **Potential performance limitations**: While SQLite is sufficient for now, it might not provide optimal performance as 
our application grows. We may need to revisit this decision and upgrade to a more scalable database later.
* **Limited support for advanced features**: SQLite has some limitations in terms of concurrency control, triggers, or 
other advanced features that we might want to use.

**Next Steps**:

* **Initial Development**: Proceed with implementing the food delivery application using SQLite as our primary database.
* **Monitoring and Testing**: Keep an eye on performance and scalability concerns. Conduct load testing and monitoring to 
identify potential issues early on.

This is just a starting point, and we can always revisit this decision once we've gathered more experience or have specific 
requirements that dictate a different choice.
