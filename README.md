# springboot-kotlin-webgoat

Simple vulnerable Spring Boot Application written in Kotlin

## Run

```
$ ./gradlew bootRun
```

## Vulnerabilities

```
$ grep -R vulnerability src 
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/CustomRestExceptionHandler.kt:        // vulnerability: Exception Data Leaked in HTTP Response
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/HelloController.kt:    // vulnerability: Sensitive Data Leak
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/HelloController.kt:    // vulnerability: XSS
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/HelloController.kt:      // vulnerability: Remote Code Execution
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/HelloController.kt:      // vulnerability: Directory Traversal
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/HelloController.kt:    // vulnerability: Open Redirect
src/main/kotlin/ai/qwiet/springbootkotlinwebgoat/HelloController.kt:    // vulnerability: XSS
```

## Examples of HTTP endpoints querying

```
$ curl localhost:8080
Greetings from Spring Boot
```
