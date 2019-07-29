#Gradle Global Repository Settings

To specify a global repository for all projects (i.e a company repository) put the following code in `~/.gradle/init.gradle`

```groovy
allprojects {
    repositories {
        mavenLocal()
        maven { url "https://your-url.net" }
        maven { url "https://your-url.net" }
    }
}
```

