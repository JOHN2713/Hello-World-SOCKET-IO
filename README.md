# Socket.IO Visual - Comunicación Cliente-Servidor

Este proyecto implementa un servidor Socket.IO en Python utilizando Flask y Eventlet. Incluye un cliente web visual que permite enviar y recibir mensajes en tiempo real desde un navegador.

## Características

- Comunicación bidireccional entre el cliente y el servidor
- Interfaz web para enviar mensajes al servidor y ver las respuestas en tiempo real
- Dockerización completa para un despliegue fácil y portátil

## Requisitos

- **Docker** instalado en tu sistema
- **Docker Compose** (opcional para una gestión más fácil)

## Estructura del Proyecto

```
.
├── Dockerfile              # Archivo para construir la imagen Docker
├── requirements.txt        # Dependencias del servidor
├── socketio_server.py      # Código del servidor Socket.IO
├── index.html              # Interfaz web del cliente
└── README.md               # Documentación del proyecto
```

## Configuración

### 1. Construir la Imagen Docker

Desde el directorio raíz del proyecto, ejecuta:

```bash
docker build -t socketio-visual .
```

### 2. Ejecutar el Contenedor

Ejecuta el contenedor con el siguiente comando:

```bash
docker run -p 5000:5000 --name socketio-visual-container socketio-visual
```

### 3. Probar la Aplicación

1. Abre tu navegador y visita http://localhost:5000
2. Escribe un mensaje en la interfaz web y presiona "Enviar"
3. Observa la respuesta del servidor en tiempo real

## Uso de Docker Compose (Opcional)

Si prefieres usar Docker Compose:

1. Asegúrate de tener un archivo `docker-compose.yml` en el directorio raíz
2. Ejecuta el siguiente comando para levantar el servicio:

```bash
docker-compose up
```

3. La aplicación estará disponible en http://localhost:5000

## Personalización

Puedes personalizar el archivo `index.html` para:
- Cambiar el diseño
- Agregar funcionalidades adicionales

## Reinicio del Servidor

Para reiniciar el servidor, detén y elimina el contenedor anterior:

```bash
docker stop socketio-visual-container
docker rm socketio-visual-container
```

## Tecnologías Utilizadas

- **Python**
  - Flask
  - Flask-SocketIO
  - Eventlet
- **Socket.IO** (comunicación en tiempo real)
- **Docker** (contenedores)
- **HTML y JavaScript** (interfaz web)
