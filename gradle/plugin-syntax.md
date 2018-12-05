# Gradle Plugin Syntax
Plugins in gradle can be applied using two different syntaxes.  
### Using the `apply` syntax:

~~~groovy
apply plugin: 'com.github.johnrengelman.shadow'
apply plugin: 'java'
apply from: "gradle/project-footer.gradle"
~~~
where `apply plugin:` calls the Plugin.apply() interface, 
while `apply from:` calls the script directly.

### Using the DSL

~~~groovy
plugins {
    id 'java'
    id 'com.jfrog.bintray' version '0.4.1'
}
~~~

