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

### Architect (Toy model)
![architecture](/software_engineer_jobs/architecture.png)

### Frontend development (Toy model)
```html
<!DOCTYPE html>
<html>
<body>

<input type="text" id="searchBox"><br>
<button onclick="search()">Google Search</button>
<div id="demo"></div>

<script>
function search() {
  const query = document.getElementById("searchBox").value;
  $.ajax({url: "/search?q=" + query, success: function(result){
      $("#demo").html(result);
  }});
}
</script>

</body>
</html>
```

### Backend development (Toy model)
```java
package com.example;

import javax.ws.rs.GET;
import javax.ws.rs.Path;
import javax.ws.rs.Produces;

@Path("/search")
public class MyResource {
    @GET
    @Produces("text/plain")
    public String getUrl() {
        return "www.google.com";
    }
}
```
