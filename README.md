# Aplicaciones: descargas oficiales

Repositorio público de APK, novedades y manifiestos de actualización de las aplicaciones de Akira. El código de cada aplicación se mantiene en su repositorio de desarrollo.

## Aplicaciones

| Aplicación | Descargas y novedades | Manifiesto de actualización |
|---|---|---|
| Cuadre | [Ver versiones de Cuadre](https://github.com/akiradev990515/aplicaciones-descargas/releases?q=cuadre-v) | `apps/cuadre/actualizacion.json` |

Cuadre ya está disponible para descargar. Su manifiesto indica la versión comercial vigente y el enlace de descarga correspondiente.

## Descargar e instalar

1. Abre las versiones de la aplicación que necesitas.
2. Selecciona una publicación estable de esa aplicación y descarga su archivo `.apk`.
3. Abre la APK desde Android y confirma la instalación. Si Android lo solicita, concede permiso al navegador para instalar el archivo.
4. Para actualizar, instala sobre la versión anterior conservando la aplicación. Las actualizaciones deben mantener su identificador y certificado de firma.

Cada publicación incluye novedades y una suma SHA-256 para verificar el archivo descargado. Cuadre incluye su propia gestión de licencias; descargar una APK no concede una licencia.

## Organización de versiones

- Cuadre utiliza etiquetas `cuadre-vX.Y.Z`.
- Otras aplicaciones usarán su propio identificador, por ejemplo `otra-app-vX.Y.Z`.
- Cada aplicación consulta `apps/IDENTIFICADOR/actualizacion.json` en la rama `main`.
- La última publicación general del repositorio puede pertenecer a cualquier aplicación. Para actualizar, utiliza el manifiesto de la aplicación correspondiente.

Las APK y los manifiestos de cada versión se guardan en GitHub Releases. En `main` solo se conservan el catálogo, la documentación y el manifiesto vigente de cada aplicación. Una versión se publica completa antes de actualizar su manifiesto vigente.

## Incorporar otra aplicación

1. Elige un identificador único y estable.
2. Añádela a `catalogo.json` y crea `apps/IDENTIFICADOR/README.md`.
3. Publica sus APK con etiquetas propias y un certificado de firma constante.
4. Configura su actualizador para consultar exclusivamente su manifiesto.
5. Actualiza únicamente su archivo, conservando los manifiestos de las demás aplicaciones.

Las credenciales de publicación se guardan en los secretos de los flujos de desarrollo. Los clientes descargan sin token.
