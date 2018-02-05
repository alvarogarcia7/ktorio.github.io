---
title: Features
caption: Extend Application Capabilities
section: Features
permalink: /features/index.html
---

A Ktor application typically consists of a series of features. You can think of features as functionality
that is injected into the request and response pipeline. Usually an application would have a series of features such as `DefaultHeaders` which add headers to every outgoing
response, `Routing` which allows us to define routes to handle requests, etc.

### Features

{% include category-list.html %}

### Installing

A feature is "installed" into the [Application](/application) using the `install` function

```kotlin
fun Application.main() {
    install(DefaultHeaders)
    install(CallLogging)
    install(Routing) {
        get("/") {
            call.respondText("Hello, World!")
        }
    }
}
```
Some common feature such as `Routing` come with helper functions, which are defined as extension functions to `Application`, making the code
somewhat more fluent. For instance, instead of writing

```kotlin
    install(Routing) {
        get("/") {
            call.respondText("Hello, World!")
        }
    }
```

we could simply write

```kotlin
    routing {
        get("/") {
            call.respondText("Hello, World!")
        }
    }
```

### Built-in Features

Ktor comes with a number of ready-made features that can be installed into your application:

> Some features might need adding an extra dependency to your project. See feature pages for more details.

### Custom features

You can develop your own features and reuse them across your Ktor applications.
Refer to [Advanced Features](/advanced/features) for more information.
