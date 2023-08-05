# Migrate_XML_Project_Into_Compose


First of all add a dependencies and needed to build.gradle.kts (:app)

```
android {

//Add this code
**
buildFeatures {
    compose = true
}
**
}
```


In similar file add below dependencies.
```
dependencies {

  **//compose
    implementation("androidx.compose.material:material:1.3.0-rc01")
    implementation("androidx.compose.compiler:compiler:1.3.2")
    implementation("androidx.compose.ui:ui-tooling-preview:1.3.0-rc01")
    implementation("androidx.activity:activity-compose:1.6.0")
    debugImplementation("androidx.compose.ui:ui-tooling:1.3.0-rc01")**
}
```
