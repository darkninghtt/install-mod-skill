---
name: install-mod
title: Install Game Mod
description: Instala mods en juegos siguiendo instrucciones personalizadas. Recibe la ruta del juego, carpeta del mod y pasos de instalación, y ejecuta todo automáticamente.
---

# Install Game Mod

Cuando te pida instalar un mod para un juego, debes seguir este proceso:

## 1. Recibir información del usuario

El usuario te proporcionará:
- **Game path**: Ruta donde está instalado el juego
- **Mod path**: Ruta de la carpeta que contiene los archivos del mod
- **Instructions**: Pasos de instalación específicos (opcional — si no los da, los infieres)

## 2. Explorar las carpetas

- Lee el contenido de `{game_path}` para entender la estructura del juego
- Lee el contenido de `{mod_path}` para ver qué archivos/carpetas trae el mod
- Busca archivos de configuración relevantes en ambas ubicaciones

## 3. Ejecutar la instalación

Sigue estrictamente las instrucciones proporcionadas. Si no hay instrucciones explícitas, aplica la lógica estándar:

- **Copiar archivos del mod al juego**: Si el mod trae carpetas como `models/`, `textures/`, `scripts/`, `plugins/`, etc., cópialas al directorio del juego manteniendo la estructura.
- **Reemplazar archivos existentes**: Si el mod sobrescribe archivos del juego, confirma con el usuario antes de reemplazar.
- **Modificar configuraciones**: Si el mod requiere editar archivos `.ini`, `.cfg`, `.json`, `.toml` u otros de configuración, haz las modificaciones necesarias.
- **Ejecutar parches/instaladores**: Si hay ejecutables o scripts del mod, adviérteselo al usuario y pregúntale si quiere ejecutarlos (nunca ejecutes .exe/.bat/.sh sin permiso explícito).

## 4. Verificar la instalación

- Confirma que los archivos se copiaron correctamente
- Muestra al usuario qué se hizo exactamente (archivos copiados, modificados, etc.)
- Si algo falla (ruta no existe, archivos faltantes, permisos), indícaselo al usuario con el error específico

## 5. Reglas importantes

- **Nunca ejecutes binarios/scripts del mod sin preguntar primero**
- **Siempre haz backup** de cualquier archivo que vayas a reemplazar (renómbralo a `.backup` o cópialo a `{game_path}/.mod-backups/`)
- **Confirma con el usuario** antes de sobrescribir archivos existentes del juego
- Si el mod requiere dependencias (como un mod loader tipo Vortex, Fabric, etc.), indícaselo al usuario
- Trabaja SOLO con archivos directamente — no descargues nada, no uses APIs externas
