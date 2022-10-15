# Sobre el codi de les activitats.
Per accedir als elements de la interfície se referencien amb una variable:
- textViewFails: per al nombre de intents fallits.
- editTextUsername: per al nom d'usuari.
- editTextPassword: per a la clau.
- btLogin: perl al botó d'accés .

Exemple amb part del codi:
```
val textViewFails=findViewById<TextView>(R.id.textViewAttemptsCounter) 
val editTextUsername=findViewById<EditText>(R.id.editTextTextUsername) 
val editTextPassword=findViewById<EditText>(R.id.editTextTextPassword) 
val btLogin=findViewById<Button>(R.id.btLogin)
```

Per a realitzar la navegacio entre una activitat i altra he fet us d'un *intent*.
```
val intentScreen= Intent(baseContext,MainScreen::class.java)
intentScreen.putExtra("usuari",goodUser) // amb aquesta linia li pasem el nom d'usuari a la nova activitat
startActivity(intentScreen)
```

# Sobre el fitxer *Manifest*.
Hi han dos activitats:
1 MainActivity
2 MainScreen
```
        <activity
            android:name=".MainScreen"
            android:exported="false">
            <meta-data
                android:name="android.app.lib_name"
                android:value="" />
        </activity>
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
            <meta-data
                android:name="android.app.lib_name"
                android:value="" />
        </activity>
 ```
La principal diferencia entre elles es que en la MainActivity hi ha un apartat "intent-filter" que no apareix en MainScreen.
El intent-filter serveix per a indicar el tipus de "intents" implícites que accepta la app.

L'atribut *android:exported* serveix per a indicar si els components d'altres aplicacions poden iniciar l'activitat.
- Si el seu valor es *true* qualsevol app pot accedir a l'activitat.
- Si el valor es *false* l'activitat sols se pot iniciar amb components de la mateixa aplicacio, aplicacions amb el mateix ID d'usuari o components del sistema amb privilegis.
Quan no hi han filtres de intents (intent-filter) el valor predeterminat es *false*.

# Sobre les traduccions realitzades.
En la carpeta de recursos de tipus String s'han creat dos fitxers mes anomenats; strings.xml(ca-rES) i strings.xml(es-rES)
En la carpeta *res* del projecte s'han creat 2 carpetes anomenades; values-es-rES i values-ca-rES. Aquestes carpetes contenen els fitxers *strings.xml* on esta inclosa la tracuccio al espanyol i al català de la APP.

strings.xml (es-rES):
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="app_name">LoginApp</string>
    <string name="FailedAttempts">Intentos fallidos:</string>
    <string name="UserName">Nombre de usuario</string>
    <string name="Login">Acceso</string>
    <string name="Password">Clave</string>
    <string name="Welcome">Bienvenido</string>
</resources>
```

strings.xml (ca-rES):
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="app_name">LoginApp</string>
    <string name="FailedAttempts">Intents fallits:</string>
    <string name="UserName">Nom d\'usuari</string>
    <string name="Login">Accés</string>
    <string name="Password">Clau</string>
    <string name="Welcome">Benvingut</string>
</resources>
```
