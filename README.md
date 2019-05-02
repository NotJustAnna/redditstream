# RedditStream
ProjectReactor-based Reddit crawler in Java 11.

Licensed under the [MIT License](https://github.com/notjustanna/redditstream/blob/master/LICENSE).

### Installation

![Latest Version](https://api.bintray.com/packages/notjustanna/maven/redditstream/images/download.svg)

Using in Gradle:

```gradle
repositories {
  jcenter()
}

dependencies {
  compile 'net.notjustanna.libs:redditstream:LATEST' // replace LATEST with the version above
}
```

Using in Maven:

```xml
<repositories>
  <repository>
    <id>central</id>
    <name>bintray</name>
    <url>http://jcenter.bintray.com</url>
  </repository>
</repositories>

<dependencies>
  <dependency>
    <groupId>net.notjustanna.libs</groupId>
    <artifactId>redditstream</artifactId>
    <version>LATEST</version> <!-- replace LATEST with the version above -->
  </dependency>
</dependencies>
```

### Usage

The starting point of the library is the ``RedditStream`` class.

Use the ``RedditStream#stream`` method to create a stream which returns a ProjectReactor's [``Flux``](https://projectreactor.io/docs/core/release/api/index.html?reactor/core/publisher/Flux.html)

```java
for (Post post : new RedditStream().stream().toIterable()) {
    System.out.println("NEW POST: " + post.getPermalink());
}
```

### Support




