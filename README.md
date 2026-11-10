# Painani

Planeación de rutas de última milla para oxígeno medicinal en la Ciudad de México.

**Página:** https://USUARIO.github.io/painani/ (reemplaza `USUARIO` por tu usuario de GitHub)

## ¿Qué es Painani?

Painani es una prueba académica del Posgrado en Ingeniería en Sistemas de la UNAM (Programación Dinámica, semestre 2027-1). Propone cuántas unidades despachar para surtir oxígeno medicinal y qué ruta sigue cada una, para que quien asigna los tanques no tenga que calcularlo a mano durante una emergencia. La meta del proyecto es que cada pedido se atienda en menos de 24 horas.

Este repositorio contiene la landing page con la que se invita a distribuidoras de gases medicinales e instituciones de salud pública a probar un piloto sin costo.

## Cómo funciona el modelo

1. **Entrada:** un archivo CSV con ubicaciones de demanda y de centros de distribución, demanda por punto y matriz de distancias.
2. **Partición del territorio:** un árbol de expansión mínima (MST) agrupa los puntos de demanda y asigna cada grupo a una unidad.
3. **Ruteo por etapas:** programación dinámica ordena las visitas y el regreso de cada unidad.
4. **Salida:** un reporte con la secuencia de visitas y la distancia recorrida por unidad.

El modelo está en etapa piloto y se valida con datos sintéticos. No sustituye la validación operativa en una operación real.

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `index.html` | Landing page. Un solo archivo con HTML y CSS; solo carga tipografías de Google Fonts. |
| `README.md` | Este documento. |

## Publicar en GitHub Pages

1. Crea un repositorio público llamado `painani`.
2. Sube `index.html` y `README.md` a la rama `main`.
3. Ve a **Settings → Pages**.
4. En **Source** elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
5. En uno o dos minutos la página queda en `https://USUARIO.github.io/painani/`.

## Medir visitas por mes y por canal

GitHub Pages no entrega estadísticas de visitas. Para obtenerlas, añade una herramienta de analítica.

1. Elige una (por ejemplo Plausible, GoatCounter o Google Analytics) y copia su código de seguimiento.
2. Pega el código dentro de `<head>` en `index.html`, antes de `</head>`, y sube el cambio.
3. Revisa en su panel las visitas por mes y las fuentes de tráfico.

Para separar los canales, usa un enlace distinto en cada uno con parámetros UTM, que Plausible y Google Analytics leen de forma nativa. Para otras herramientas, revisa su documentación sobre campañas.

| Canal | Enlace |
|---|---|
| Correo frío | `https://USUARIO.github.io/painani/?utm_source=correo&utm_medium=email&utm_campaign=piloto` |
| LinkedIn | `https://USUARIO.github.io/painani/?utm_source=linkedin&utm_medium=social&utm_campaign=piloto` |
| Código QR | `https://USUARIO.github.io/painani/?utm_source=qr&utm_medium=impreso&utm_campaign=piloto` |
| WhatsApp | `https://USUARIO.github.io/painani/?utm_source=whatsapp&utm_medium=mensaje&utm_campaign=piloto` |
| Contactos académicos | `https://USUARIO.github.io/painani/?utm_source=academico&utm_medium=referido&utm_campaign=piloto` |

Algunas herramientas usan cookies. Si las activas, considera añadir un aviso de privacidad a la página.

## Equipo

- Alejandro Ruiz Mendoza: alejandro.ruiz@ingenieria.unam.edu
- Yahir Solares Tenorio: yahirsolares@ciencias.unam.mx

## Licencia

Por definir. Si quieres que otras personas reutilicen la página, añade un archivo `LICENSE` (por ejemplo, MIT).
