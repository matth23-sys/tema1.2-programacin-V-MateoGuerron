# Tema 1.2 - Entorno portable de Dart y Flutter

## Características del equipo

- Procesador: 13th Gen Intel(R) Core(TM) i7-13620H (2.50 GHz)
- Memoria RAM: 16 GB DDR4
- Espacio libre en disco: 512 GB
- Virtualización: Habilitada
- Permisos de administrador: Sí

## Entorno de desarrollo

La instalación portable se realizó en:

`C:\Dev`

Dentro de esta carpeta se configuraron Flutter, VS Code portable, la caché de paquetes y los proyectos realizados durante la práctica.

## Versiones utilizadas

- Flutter: 3.47.8
- Dart: 3.13.7
- Canal Flutter: stable

## Destinos disponibles

Durante la práctica se utilizaron principalmente:

- Consola de Dart
- Google Chrome para aplicaciones Flutter Web

Flutter detectó correctamente Chrome como destino disponible.

## Diagnóstico con Flutter Doctor

El comando `flutter doctor` detectó correctamente Flutter, Chrome, dispositivos conectados y los recursos de red.

Se encontraron advertencias relacionadas con Android SDK y Visual Studio. Estos componentes no fueron necesarios para completar esta práctica, ya que se trabajó con Dart en consola y Flutter en Chrome.

## Problema resuelto durante la práctica

Uno de los problemas revisados fue la configuración del PATH de Flutter.

Para que Windows pueda reconocer el comando `flutter`, no se debe agregar únicamente:

`C:\Dev\flutter`

La ruta correcta es:

`C:\Dev\flutter\bin`

Después de actualizar el PATH fue necesario abrir una terminal nueva para que Windows reconociera correctamente el comando.

## Kit portable

Se creó el archivo `iniciar.bat`, que configura temporalmente las rutas de Flutter y `PUB_CACHE` y abre VS Code portable.

La variable `%~dp0` permite obtener automáticamente la ubicación donde se encuentra el archivo `.bat`, haciendo que el kit pueda funcionar desde su propia carpeta.

## Proyectos realizados

### hola_entorno

Programa desarrollado en Dart que solicita el nombre del usuario y muestra información del sistema y la versión de Dart.

### hola_flutter

Aplicación Flutter ejecutada en Google Chrome. Durante la práctica se modificó el título de la aplicación y el color del tema utilizando Hot Reload.