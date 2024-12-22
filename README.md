# Lista de Radios Españolas para Euro Truck Simulator 2

[![Check Links](https://github.com/juan-miii/ets2-spain-radio/actions/workflows/link-check.yml/badge.svg)](https://github.com/juan-miii/ets2-spain-radio/actions/workflows/link-check.yml)

Este repositorio contiene una lista de radios españolas organizada alfabéticamente en el formato `live_streams.sii`, compatible con **Euro Truck Simulator 2** y **American Truck Simulator**. 

Se ha intentado priorizar el uso de enlaces HTTPS por motivos de seguridad, excepto en casos donde solo se dispone de enlaces HTTP. Además, las columnas están organizadas para facilitar la visualización del contenido.

---

## Contenido del Repositorio

- **Lista completa de radios españolas**:
  - Emisoras clasificadas por nombre, género, idioma y bitrate.
  - Preparada para ser integrada directamente en el juego.

- **Formato del objeto radio dentro de la lista**:
  - `RADIO_URL`: Enlace al stream de la emisora.
  - `RADIO_NAME`: Nombre de la emisora (informativo).
  - `GENRE`: Género musical o contenido (informativo).
  - `LANGUAGE`: Idioma de la emisora (informativo).
  - `BITRATE`: Calidad del stream en kbps (kilobits por segundo).
  - `FAVOURITE`: Si es favorita, como binario (0 no, 1 sí). Esto se puede configurar desde dentro del juego. Con la asignación de teclas correcta permite navegar entre radios favoritas directamente.

*Los datos marcados como informativos sólo contribuyen a cómo se muestra la radio dentro del juego.*

---

## Cómo incluir nuevas emisoras

Si quieres contribuir al proyecto, para que más gente tenga acceso a nuevas emisoras, o para arreglar cualquier link roto o caido, te recomiendo que incorpores los cambios a este repositorio mediante un Pull Request. Si quieres mantener tu lista independiente, configurada a tu gusto, sugiero hacer fork del repositorio y modificarla ahí. De esta forma, siempre tendrás acceso a actualizaciones que se hagan sobre la lista.

### Pasos para añadir emisoras:
1. **Obtener la información de la emisora**:
   - Usa [StreamURL.link](https://streamurl.link/) para encontrar emisoras funcionales con enlaces HTTPS, nombre, bitrate e idioma. Cualquier otro servicio también es válido, siempre y cuando se incluya un link válido y el bitrate. SCS (la desarrolladora de los juegos) considera válidos aquellos servicios que ofrezcan emisión en formato MP3.
2. **Probar el enlace**:
   - Antes de añadir la emisora, asegúrate de que el enlace funciona correctamente en un navegador o reproductor multimedia.
3. **Editar el archivo**:
   - Abre el archivo `live_streams.sii` en un editor de texto.
   - Añade una nueva línea con el siguiente formato:
     ```plaintext
     stream_data[X]: "RADIO_URL|RADIO_NAME|GENRE|LANGUAGE|BITRATE|0"
     ```

### Ejemplo de entrada válida:
```plaintext
stream_data[]: "https://dispatcher.rndfnk.com/crtve/rne1/main/mp3/high|Radio Nacional|Nacional|ES|128"
stream_data[]: "http://playerservices.streamtheworld.com/api/livestream-redirect/CADENADIALAAC_SC|Cadena Dial|Pop|ES|128"
```

Actualmente, las entradas están formateadas con espacios, como se puede ver en el archivo, para facilitar la lectura humana. El juego permite que estén escritas de este modo.

---

## Ubicación del Archivo y Modificaciones

El archivo `live_streams.sii` original se encuentra en:
```
ruta\a\Euro Truck Simulator 2\live_streams.sii
```

### Pasos para reemplazar o modificar:
1. **Hacer una copia de seguridad**:
   - Antes de realizar cualquier cambio, guarda una copia del archivo original en otro directorio.
2. **Editar el archivo o sustituyelo por este**:
   - Usa un editor de texto como Notepad++ o Visual Studio Code para modificar el orginal, cambiando las entradas, o reemplazalo por el de este repositorio teniendo en cuenta el siguiente paso.
3. **Conservar el nombre original**:
   - Por compatibilidad, mantén el nombre de la lista `live_stream_def : ESTE_NOMBRE` tal cual para prevenir erroresal cargarlo en el juego. Si la lista tiene la sintaxis correcta y se muestra un mensaje de error en el juego redirigiéndote al README, seguramente tenga que ver con este fallo.
4. **Probar los cambios**:
   - Guarda los cambios y abre el juego. Verifica que las emisoras añadidas aparecen y funcionan correctamente.

---

## Recomendaciones para Contribuciones

Este repositorio es **colaborativo**. Si deseas contribuir:
1. Realiza un fork del repositorio y añade tus cambios.
2. Prueba que los enlaces funcionan antes de crear un Pull Request.

Si prefieres una lista personalizada, puedes usar este repositorio como base y adaptarlo a tus preferencias.

---

## Notas legales

Este proyecto sigue las indicaciones de SCS Software. El archivo `live_streams.sii` y el software Euro Truck Simulator 2 son propiedad de SCS Software. Este proyecto es de uso personal y no comercial. Consulta la licencia completa proporcionada por SCS Software para más información.
