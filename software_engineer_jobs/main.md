# Software Engineer Jobs

* Front end development
  * Responsibility: develop web app or mobile app for end-clients.
  * Programming languages: HTML, CSS, Javascript (Coffeescript, Typescript)
  * Popular frameworks: React, Vue, Angular1, Angular2, Polymer, Ember, etc.
* Back end development
  * Responsibility: develop server interface and domain logic to serve requests
    from front end.
  * Programming languages: Java, C++, Python, etc.
  * Popular libraries: Jetty/Jersey/Jackson
* Development operations (DevOps)
  * [WIP]

# Example

### UI
![google search](/software_engineer_jobs/google_search_demo.gif)

*Disclamer: Above is the official Google search site. The later sections are not
real design/code for this demo, but are just showing example implementation.*

### Architect

### Frontend code

### Backend code
```Java
package com.example;

import javax.ws.rs.GET;
import javax.ws.rs.Path;
import javax.ws.rs.Produces;

@Path("")
public class MyResource {
    @GET
    @Produces("text/plain")
    public String getIt() {
        return "Got it!";
    }
}
```
