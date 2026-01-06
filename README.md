# tsm-app---kg-locked-mdm-app
explicacion acerca de la app tsm y privilegios de tener una app con perfil administrador

bueno que tal 
esta investigación es para usos educativo
la aplicación usadas fueron
adb.exe
apk editor studio.exe
y la app de tsm

las herramientas de bypass mdm utilizan el perfil de administrador para administrar el dispositivo
y asi poder ingresar acciones administrativas (acceso muchas funcionas)

mi enfoque:

- bloquear el factory reset para evitar que un usuario lo formatee (use tedstdpc para saber como funcionaba un pefil administrador)

para ello debemos habilitar el profile owner
# Para Device Owner (máximos privilegios, requiere dispositivo recién factory reset)
adb shell dpm set-device-owner com.tsm.amdm.knox/.Hubris

el dispositivo no puede ya tener otro perfil owner o cuenta google
debe estar recién formateado

al estar instalado 
para ejecutar el disabled factory reset
adb shell am start -n com.tsm.amdm.knox/.DisableFactoryReset

para habilitarlo
adb shell am start -n com.tsm.amdm.knox/.EnableFactoryReset


ya lo único que tienen que hacer para ejecutar la app de tsm luego de la instalación y poner de perfil administrador
adb shell am start -n com.tsm.amdm.knox/.Andromaleus
con eso la inician y les ejecutara sus respectivas funciones



si quieren editar la app háganlo con Android studio
y se iran a las carpetas drawable 
y layout para editarla las xml y poner su logo y marca

ahí les dejo la carpeta de la app
APP SOURCE:
https://www.mediafire.com/file/crfmsi80n9tv58t/TSM+APP.zip/file


