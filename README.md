# Migrate_XML_Project_Into_Compose


First of all add a dependencies and needed to build.gradle.kts (:app):


android {
```
//Add buildFeatures code snippet
buildFeatures {
    compose = true
}
```
}



In similar file add below dependencies inside the dependencies block:

dependencies {
```
  //compose
    implementation("androidx.compose.material:material:1.3.0-rc01")
    implementation("androidx.compose.compiler:compiler:1.3.2")
    implementation("androidx.compose.ui:ui-tooling-preview:1.3.0-rc01")
    implementation("androidx.activity:activity-compose:1.6.0")
    debugImplementation("androidx.compose.ui:ui-tooling:1.3.0-rc01")
}
```

And then Syn Now the project.


After that, 

Add below code snippet to your activity_main file:
```
 <androidx.compose.ui.platform.ComposeView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:id="@+id/composeView"/>
```

Later open MainActivity file

Add below code above of MainActivity file:
```
   private val composeView: ComposeView by lazy {
        findViewById(R.id.composeView)
    }
```

With using compose property we can write setContent to set compose Ui to our composeView id:
```
  composeView.setContent {
        //Adding an example composable text compose of inside
            Text(
                text = "Compose view with a place holder",
                modifier = Modifier
                    .fillMaxWidth()
                    .wrapContentHeight()
                    .background(Color.Yellow)
                    .padding(20.dp),
                textAlign = TextAlign.Center,
                fontWeight = FontWeight.Bold,
                fontSize = 20.sp

            )
        }

```

Congratulations! You migrate compose into XML project.

