### Need of Spring MVC
1. Earlier Servelt was used to build and run an application which had following drawbacks
     1.1 Requires more manual coding and configuration.
     1.2 requires servlet mapping through web.xml
Then Spring MVC came into picture and reduced development effort by auto configuration, a rich set of libraries, Inversion of control etc

### Need of Spring 
1. Even though spring MVC solved many issues, it still had it's drawbacks
  1.1 In spring, No need to take care of dependency version compatibility. Let's say our pom has below dependencies

      <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <version>1.18.30</version>
        </dependency>
      <dependency>
            <groupId>jakarta.persistence</groupId>
            <artifactId>jakarta.persistence-api</artifactId>
            <version>3.1.0</version>
      </dependency>

   In spring mvc, if we change the version of lombok from 1.18.30 to something else, this could create trouble as persistence dependency might not be compatible with the new version.
   In spring, we dont have to take care of version compatibility so our pom looks like this
    <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
        </dependency>
      <dependency>
            <groupId>jakarta.persistence</groupId>
            <artifactId>jakarta.persistence-api</artifactId>
      </dependency>

2. In traditional spring MVC applications, we need to build a war of our applicarion and deploy it in external server but in spring boot server is embedded

