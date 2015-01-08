# PlayGround
It's a playground for github study.

```java
interface GitHub {
  @GET @Path("/repos/{owner}/{repo}/contributors")
  List<Contributor> contributors(@PathParam("owner") String owner, @PathParam("repo") String repo);
}
...
GitHub github = Feign.builder().contract(new JAXRSModule.JAXRSContract()).target(GitHub.class, "https://api.github.com");
```
