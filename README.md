# Transferencia-de-Playlist
# 🎵 Spotify to YouTube Music Playlist Transfer

Una aplicación web ligera desarrollada en **Python (Flask)** que permite a los usuarios conectar sus cuentas de Spotify y YouTube para migrar automáticamente sus listas de reproducción mediante las APIs oficiales de ambas plataformas.

## 🚀 Características
* 🔐 Autenticación segura mediante protocolo **OAuth 2.0** para ambos servicios.
* 📋 Lectura automatizada de metadatos de canciones (Nombre, Artista, Álbum) desde Spotify.
* 🔍 Algoritmo de emparejamiento inteligente de pistas musicales a través de la API de YouTube Data v3.
* 🛠️ Creación e inserción directa de canciones en la biblioteca del usuario en YouTube Music.

## 🛠️ Requisitos de Instalación

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com
   cd spotify-to-ytmusic
   ```

2. **Crear e iniciar un entorno virtual:**
   ```bash
   python -m venv venv
   # En Windows:
   venv\Scripts\activate
   # En macOS/Linux:
   source venv/bin/activate
   ```

3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

## 🔑 Configuración de las APIs Oficiales

### 1. Portal de Desarrolladores de Spotify
* Dirígete a [Spotify Developer Dashboard](https://spotify.com) y crea una aplicación.
* Obtén tu `Client ID` y `Client Secret`.
* Configura la **Redirect URI** como: `http://localhost:5000/callback/spotify`.

### 2. Google Cloud Console (YouTube Music)
* Ve a [Google Cloud Console](https://google.com) y crea un nuevo proyecto.
* Habilita la **YouTube Data API v3**.
* Crea credenciales de tipo **ID de cliente OAuth 2.0** (Aplicación web).
* Configura la **URI de redireccionamiento autorizada** como: `http://localhost:5000/callback/youtube`.
* Descarga el archivo JSON de credenciales, renombralo como `client_secret.json` y colócalo en la raíz del proyecto.

## 🏃 Interfaz y Ejecución

Modifica las variables de entorno de Spotify dentro de `app.py` con tus credenciales y ejecuta:

```bash
python app.py
```

Abre tu navegador e ingresa a `http://localhost:5000` para iniciar la transferencia de tus playlists de forma gráfica.

## 📄 Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo de licencias para más detalles.
