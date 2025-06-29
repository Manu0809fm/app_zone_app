# 🎮 App S10 - Registro de Juegos Favoritos

Una aplicación Android desarrollada en **Kotlin** que permite a los usuarios registrar, editar, eliminar y buscar sus juegos favoritos. Utiliza **Firebase Authentication** para el login y **Firebase Realtime Database** para almacenar la información de cada usuario de forma segura y privada.

---

## 🛠️ Funcionalidades

✅ Autenticación de usuarios (login/logout)

✅ Registrar nuevos juegos con:

- Título  
- Género  
- Plataforma  
- Descripción  
- Año de lanzamiento  
- Calificación  
- Estado (completado o no)

✅ Ver la lista de juegos registrados

✅ Editar y eliminar juegos existentes

✅ Filtrar juegos por género

✅ Buscar juegos por título

✅ Datos sincronizados en tiempo real con Firebase

✅ Cada usuario solo ve sus propios juegos (seguridad garantizada)

---

## 🔧 Tecnologías Usadas

- **Kotlin** + Android SDK  
- **Firebase Realtime Database**  
- **Firebase Authentication**  
- **RecyclerView + Adapter**  
- **Material Design UI**  
- **ConstraintLayout y ScrollView**  

---

## 📸 Capturas de pantalla

![image](https://github.com/user-attachments/assets/f57c9348-873a-4e73-9b6f-23e108e63713)
![image](https://github.com/user-attachments/assets/7f64f317-b041-44ba-8d88-9f226bf908f5)
![image](https://github.com/user-attachments/assets/6473c733-a741-4bfa-815f-b88f690aa686)
![image](https://github.com/user-attachments/assets/b277ff11-22da-4d52-bea7-4558495e2b93)
![image](https://github.com/user-attachments/assets/18fe5783-aeae-4638-883c-cf615ddaade3)


---

## 🔐 Configuración de Firebase

1. Crea un proyecto en [Firebase Console](https://console.firebase.google.com/)
2. Agrega tu app Android (usa el paquete `com.example.app_s10`)
3. Descarga el archivo `google-services.json` y colócalo en: app/ > google-services.json
4. Habilita **Authentication** > "Correo y contraseña"
5. En **Realtime Database** > pestaña **Reglas**, coloca lo siguiente:

```json
{
"rules": {
 "games": {
   "$uid": {
     ".read": "$uid === auth.uid",
     ".write": "$uid === auth.uid"
   }
 }
}
}
📁 Estructura del Proyecto
com.example.app_s10/
├── MainActivity.kt
├── LoginActivity.kt
├── AddGameActivity.kt
├── EditGameActivity.kt
├── GamesListActivity.kt
├── GameAdapter.kt
├── Game.kt
└── res/
    ├── layout/
    │   ├── activity_main.xml
    │   ├── activity_login.xml
    │   ├── activity_add_game.xml
    │   ├── activity_edit_game.xml
    │   ├── activity_games_list.xml
    │   └── item_game.xml
    └── values/
        ├── strings.xml
        └── colors.xml
🚀 Cómo Ejecutar
Abre el proyecto en Android Studio

Asegúrate de tener el google-services.json en la carpeta app/

Conecta un dispositivo o inicia un emulador

Haz clic en Run ▶️

📝 Licencia
Este proyecto es de libre uso para fines educativos.
🙌 Créditos
Desarrollado por: Manuel Flores
