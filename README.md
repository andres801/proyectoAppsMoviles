# Proyecto final apps moviles
## Muestra de documentación

## AuthActivity.kt

Esta es la actividad que originalmente era la principal, la main, fue renombrada para hacer alusión a que es es la que lleva a cabo los procesos de solicitar la autenticación, y desde luego es la primera que se ejecuta al iniciar la aplicación

Comenzando con las dependencias ocupamos las 2 de firebase, la primera es la de las analíticas de Firebase y la segunda la autenticación, después ya comienza la clase AuthActivity

```kotlin
package com.example.firebaselogin
import android.content.Intent
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import androidx.appcompat.app.AlertDialog
import com.google.firebase.analytics.FirebaseAnalytics
import com.google.firebase.auth.FirebaseAuth
import kotlinx.android.synthetic.main.activity_auth.*

class AuthActivity : AppCompatActivity() {
```


La primera función que se ocupa es la de onCreate, lo que hace es crear las instancias de firebase analytic

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_auth)

        val analytics:FirebaseAnalytics = FirebaseAnalytics.getInstance(this)
        val bundle = Bundle()
        bundle.putString("message","Integración de Firebase completa")
        analytics.logEvent("InitScreen",bundle)

        //Setup
        setup()
    }
```


## colors.xml

En este archivo xml personalicé algunos colores para asignarlos a los distintos elementos de acuerdo a la siguiente paleta de colores de forma que determinados botones y el fondo adopten un colores relacionados entre sí

![Paleta azul](https://user-images.githubusercontent.com/58822692/172968016-db6d2d6b-1757-4bed-8c9e-6fcdd1fab197.png)


```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="purple_200">#FFBB86FC</color>
    <color name="purple_500">#FF6200EE</color>
    <color name="purple_700">#FF3700B3</color>
    <color name="teal_200">#FF03DAC5</color>
    <color name="teal_700">#FF018786</color>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="botónLogIn">#023e8a</color>
    <color name="botónLogOut">#0096c7</color>
    <color name="botónSignUp">#0096c7</color>
    <color name="fondo">#caf0f8</color>
</resources>
```
