# Timer Plus (web / APK)

Aplicación de temporizadores, cronómetro y entrenamientos por intervalos, inspirada en Timer Plus de DigitAlchemy. Es una página web de un solo archivo (`www/index.html`) empaquetada como APK de Android con Capacitor.

## Funciones

- **Temporizador:** varios a la vez, con nombre, tiempo en h:min:s, barra de progreso, alarma y aviso visual al terminar.
- **Cronómetro:** minutos, segundos y milésimas, con vueltas, mejor y peor vuelta.
- **Entrenar:** Tabata, EMOM, AMRAP, AFAP, HIIT, Circuito, Boxeo y Personalizado.
  - Más de 25 plantillas incluidas.
  - Todos los campos son editables (escribiendo o con los botones − y +).
  - Pasos propios en el modo Personalizado y plantillas propias guardables.
- **Ajustes:** tema (sistema, claro, oscuro), color de acento, sonidos, volumen, repetición de la alarma, cuenta atrás, vibración, notificaciones y pantalla encendida.
- Los datos se guardan en el navegador (`localStorage`).

## Cómo obtener el APK

No hace falta instalar Android Studio.

1. Crea un repositorio en GitHub y sube todo el contenido de esta carpeta, incluida la carpeta oculta `.github`.
2. Abre la pestaña **Actions**. El flujo **Build APK** se ejecuta con cada subida y tarda unos 5 minutos.
3. Cuando termine, descarga el artefacto `timer-plus-apk` de la ejecución. Contiene `app-debug.apk`.
4. Cópialo al móvil e instálalo permitiendo instalar desde orígenes desconocidos.

Es un APK de depuración: sirve para instalar en tu móvil, no para publicar en Google Play.

## Estructura

```
www/index.html                  La aplicación completa (HTML, CSS y JS)
capacitor.config.json           Configuración de Capacitor (nombre e id de la app)
package.json                    Dependencias de Capacitor
.github/workflows/build-apk.yml Flujo que compila el APK en GitHub
CHANGELOG.md                    Historial de cambios
```

## Cómo registrar un cambio

1. Sustituye `www/index.html` (o los archivos que cambien) en el repositorio con **Add file → Upload files**.
2. Escribe en el mensaje de la subida qué has cambiado.
3. Añade una entrada nueva al principio de `CHANGELOG.md`.

## Limitaciones conocidas

- Las notificaciones del navegador pueden no funcionar dentro del APK.
- Con el móvil bloqueado, la alarma no es tan fiable como en una app nativa.
- No incluye widget de pantalla de inicio.
