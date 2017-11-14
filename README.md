# HelloHibernateSpringMVCSecurity

Now we need to extend our SpringMVC so that it can protect our resources from unauthorized access. We use SpringSecurity for this purpose. 
In most cases we use a database to persist our user details (username, password, and authorities) but for testing purpose we can use InMemory user.

Often, after users login successfully, there is a session created on server and send back to the client and be stored as a cookie. Subsequent requests from that client will be accompanioned by that cookie, thus they are allowed to access a resource. 

For restful webservices, most of requests are stateless, meaning that it is not aware of any no pre-authentication. The approach in such a case is to send again username/password in the header (as in BasicAuthentication protocol). There is a better way, however, often used in token based request, is to send in the header a token which contains the status of the resquest (user details, authorization, time to expires etc).

This example shows how we can use in memory users to test Spring Security
