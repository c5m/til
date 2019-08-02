#Gradle Global Repository Settings

## Dependencies Repo

To specify a global repository for all projects (i.e a company repository) put the following code in `~/.gradle/init.gradle`

```groovy
allprojects {
    repositories {
        mavenLocal()
        maven { url "https://your-url.net" }
    }
}
```



## Plugin Repo

To specify a global repository for Gradle plugins add this to `~/.gradle/init.gradle` 
(outside the *allprojects* block)

```groovy
settingsEvaluated { settings ->
    settings.pluginManagement {
        repositories {
            maven { url "https://your-url.net" }   
        }
    }
}
```

