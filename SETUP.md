# Nuestras finanzas: puesta en marcha

La app guarda los datos en Firebase (plan gratis) y se abre desde el navegador del teléfono.
Mientras `firebase-config.js` esté vacío, funciona en modo demo dentro de cada navegador.

## 1. Crear el proyecto de Firebase

1. Entra a https://console.firebase.google.com con tu cuenta de Google.
2. Toca **Agregar proyecto**, ponle un nombre (por ejemplo `finanzas-hogar`) y sigue los pasos. No hace falta Google Analytics.
3. **Authentication** → **Comenzar** → en Proveedores, activa **Google** y elige un correo de soporte.
4. **Firestore Database** → **Crear base de datos** → modo de producción → elige una región cercana.
5. En Firestore, pestaña **Reglas**, pega el contenido de `firestore.rules` y toca **Publicar**.

## 2. Conectar la app con tu proyecto

1. En la configuración del proyecto (ícono de engranaje) → **Tus apps** → botón **</>** (Web).
2. Ponle un nombre, no marques hosting, y registra la app.
3. Copia los valores de `firebaseConfig` dentro de `firebase-config.js`.

## 3. Publicar la página (GitHub Pages)

1. Crea un repositorio público en GitHub (por ejemplo `finanzas`). Pages gratis requiere que sea público.
2. Sube todos los archivos de esta carpeta a la raíz del repositorio.
3. En el repositorio: **Settings** → **Pages** → **Deploy from a branch** → rama `main`, carpeta `/ (root)`.
4. Espera un minuto. La dirección será `https://TU_USUARIO.github.io/finanzas/`.
5. En Firebase: **Authentication** → **Settings** → **Authorized domains** → agrega `TU_USUARIO.github.io`.

## 4. Instalarla en el teléfono

1. Abre la dirección en **Safari** del iPhone (o Chrome en Android).
2. Entra con tu cuenta de Google y crea el hogar.
3. En **Ajustes** de la app aparece el **código de su hogar**. Cópialo y pásaselo a tu esposa.
4. Ella abre la misma dirección, entra con su cuenta y pega el código en **Unirme**.
5. Toca **Compartir** → **Añadir a pantalla de inicio**. Listo: ícono propio, pantalla completa y sin entrar a claude.ai.

## Notas

- Las reglas dejan que solo los dos miembros del hogar lean y escriban sus datos.
- Un hogar nunca pasa de 2 miembros, y nadie puede quitar a otro miembro.
- Si cambias la configuración de Firebase, vuelve a subir `firebase-config.js` a GitHub.
