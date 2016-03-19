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


