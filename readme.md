#first 
ionic platform add android


#2
instalar plugin con las variables del caso
ionic plugin add https://github.com/BranchMetrics/Cordova-Ionic-PhoneGap-Deferred-Deep-Linking-SDK.git --variable BRANCH_KEY=key_live_akk1wFm09NNq8ohzlZQtLmjixza7zXMB  --variable URI_SCHEME=kykelyn2

#3 dependencias del plugin  branch.io
en esta carpeta
 S:\sportudo\componentes\branchio\kykelyn2\plugins\io.branch.sdk

 corro este comando npm install

 //parece que no ayudo a solucionar el problema de 
 plugins/io.branch.sdk/www/branch.js:28 Uncaught (in promise) Attempt to invoke virtual method 'android.content.Context android.app.Activity.getApplicationContext()' on a null object reference

 #start a branch session


onDeviceReady: function() {
    Branch.initSession();
},
onResume: function() {
    Branch.initSession();
},
initialize: function() {
    document.addEventListener('resume', onResume, false);
    document.addEventListener('deviceready', onDeviceReady, false);
},

ayuda
https://forum.ionicframework.com/t/best-way-to-intercept-events-like-cordova-resume-and-pause-in-ionic/4720/5

http://ionicframework.com/docs/api/service/$ionicPlatform/


////hasta aqui debe de abrir con el custom url 

<a href="kykelyn2:\\">KYKELYN2</a>

-------------------------CUSTOM URL WORKING


#primera prueba con un link generado por marketing
https://bnc.lt/Wwzm/tgDTdTJsSr
resultado: abre el chrome, visita branch por detras y rerdirige a play store (aun no muestra opciones para abrir con la aplicacion)


-----------------------ENABLING APP LINK ON CORDOVA PARA ANDROID

https://dev.branch.io/getting-started/universal-app-links/guide/cordova/

generate signing certificate fingerprint


una prueba primero con un fingerprint y usando otro para generarl el apk a ver que pasa


    <branch-config>
        <android-prefix value="/Wwzm" />
        <host name="bnc.lt" scheme="https" />
    </branch-config>
    justo antes del widget tag
</widget>

no importa que fuera un fingerprint distinto , almenos usando ionic run android funciona, no se si cuando se haga el deploy a play store esto pudiera tener alguna consecuencia y se deberia usaar el mismo firngerprint con que se firmo el apk

--revisaar si se puede jugar con el nombre en vez de 
    <branch-config>
        <android-prefix value="/k2" />
        <host name="kykelyn2.com" scheme="https" />
    </branch-config>

    resta: si funciona cuando abro este enlace, me dice open with y me muestra la app
    https://kykelyn2.com/k2
    que pasa que pierdo el trabajo por detras que me redirige al sitio web y despues al play sotre para descargar, aunque como workaround ahi me podria dirigir al sitio web y ya, si no tengo la app
    




