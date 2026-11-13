# TOPTEAM Gym Timer - OTA

Repositorio de actualizaciones de la app **TOPTEAM Gym Timer** para la TV del gimnasio.

- `latest.json`: manifiesto que consulta el agente del PC.
- Releases: APK firmado de cada version.
- No se guarda ninguna keystore en este repositorio.

## Funcionamiento

1. Se publica una release con el APK nuevo y un `versionCode` mayor.
2. Se actualiza `latest.json` con la URL del APK y su SHA-256.
3. El agente del PC descarga la actualizacion, verifica el hash y la instala
   por ADB en la TV.

## Importante

- El APK debe estar firmado siempre con la misma keystore.
- El `versionCode` debe subir en cada version.
- La TV y el PC deben estar en la misma red o tener ruta entre ellos.
- La depuracion ADB de la TV debe estar activada.
