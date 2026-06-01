Étape 1 : Reconstruction de l'APK modifié

<img width="1332" height="617" alt="image" src="https://github.com/user-attachments/assets/e9359911-17fe-44ce-a5db-e7a7b7e2680c" />


Étape 2 : Signature de l'APK

<img width="1477" height="294" alt="image" src="https://github.com/user-attachments/assets/e161810a-44f9-4182-96a7-3669c3a51e29" />


apksigner.bat sign --ks test.keystore --ks-key-alias test --ks-pass pass:password --key-pass pass:password snake_patched.apk
Signature de l'APK

Étape 3 : Installation de l'APK

<img width="1287" height="127" alt="image" src="https://github.com/user-attachments/assets/5be515a0-8913-4483-807b-bf0e18fadda3" />


Étape 4 : Copie de la charge utile (Payload)

<img width="1245" height="305" alt="image" src="https://github.com/user-attachments/assets/3e9816de-8e0b-44bc-8f10-653c3421e3b4" />


Étape 5 : Autorisations et exécution


Étape 6 : Extraction du drapeau
La commande de filtrage logcat sensible à la casse permet d'extraire la ligne contenant le drapeau généré par la bibliothèque native après désérialisation réussie.

<img width="763" height="107" alt="image" src="https://github.com/user-attachments/assets/8002cc94-f8e5-4738-ae77-57273a3943f9" />


adb logcat -d | Select-String -CaseSensitive "PWNSEC{"
Extraction du drapeau

Le drapeau extrait est : PWNSEC{W3'r3_N0t_T00l5_0f_The_g0v3rnm3n7_0R_4ny0n3_3ls3}
