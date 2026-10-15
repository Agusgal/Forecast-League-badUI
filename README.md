# Ministerio del Futuro · Forecast League badUI

**El futuro es incierto. El trámite, obligatorio.**

Una landing jugable, deliberadamente mala, para el proyecto de [Forecast League](https://github.com/Agusgal/Forecast-League). Vive en un repositorio independiente: no reemplaza la aplicación ni modifica sus datos.

## La idea

En lugar de elegir una probabilidad y enviarla y de crear tu usuario normalmente, tenés que solicitar permiso para opinar, armar el porcentaje sumando casilleros, explorar carpetas anidadas, copiar una frase y encontrar el botón de envío escondido. La pregunta es autorreferencial: **¿vas a terminar este trámite?** Llegar al comprobante resuelve el pequeño juego.

La estética es la hoja de un organismo gubernamental ficticio, con el estilo predeterminado del navegador. El humor está en la interacción y en los textos, no en animaciones ni efectos.

## Abrir

Abrí `index.html` directamente en un navegador. No requiere instalar nada, compilar, conectarse a servicios ni ejecutar un servidor.

Opcionalmente, para servirlo por HTTP:

```sh
python3 -m http.server 3001 --bind 127.0.0.1
```

Visitá http://localhost:3001. Ambos archivos se pueden alojar en cualquier hosting estático, incluido GitHub Pages.

## HTML y nada más

- Dos páginas HTML con etiquetas semánticas, enlaces y controles nativos.
- Sin CSS: ni hojas externas, ni etiquetas `style`, ni atributos `style`.
- Sin JavaScript: ni scripts, ni manejadores de eventos, ni URLs `javascript:`.
- Sin dependencias, fuentes externas, imágenes remotas, frameworks o analítica.
- `details` y `summary` permiten abrir ventanillas y carpetas.
- `required` y `pattern` hacen la validación nativa de los campos.
- El formulario navega mediante GET a `comprobante.html`.
- Los casilleros se suman a mano: HTML no coteja su suma con el número escrito.
- El comprobante es estático: no interpreta parámetros ni calcula puntajes.

Las respuestas quedan en la URL y pueden aparecer en el historial y en los registros del servidor si se aloja por HTTP. Usá solamente datos inventados. No existe cuenta, persistencia de aplicación ni conexión con la base de Forecast League.

## Catálogo de decisiones pésimas

| Antipatrón | Implementación |
| --- | --- |
| Fricción antes del valor | Permiso para tener una opinión |
| Interfaz que obliga a pensar en su mecanismo | Porcentaje armado en binario y transcrito a mano |
| Orden impredecible | Casilleros 64, 1, 16, 4, 32, 2, 8 |
| Divulgación progresiva llevada al absurdo | Cuatro carpetas para revelar que no hay consenso |
| Trabajo redundante | Copia literal y tres confirmaciones |
| Jerarquía invertida | Reset visible, envío escondido |
| Falso progreso | Barra estática del 1 %, explícitamente identificada |
| Ayuda circular | Un enlace de ayuda que vuelve a la ayuda |
| Escape burocrático | Atajo legítimo al comprobante en las preguntas frecuentes |

La frustración es intencional, pero no usamos destellos, capturas de teclado ni etiquetas inaccesibles. Hay un final alcanzable, navegación por teclado y una salida. No hay apuestas ni dinero; el organismo y sus declaraciones son ficticios.

## Cómo se ideó

Pedido del usuario: experimentar con una landing badUI de Forecast League, muy creativa, usando solamente HTML, sin CSS ni JavaScript. Se debe recrear la experiencia de llenar trámites para una agencia gubernamental ficticia. Por ejemplo: llenar un sinfín de campos inútiles, interacciones lentas con la UI y comboboxes que no hacen nada. La estética debe ser de una página vieja del gobierno. 



## Comprobar el recorrido

1. Abrir `index.html`, completar alias y motivo y aceptar la declaración ficticia.
2. Para 73 %, marcar 64 + 8 + 1 y transcribir 73.
3. Explorar las carpetas de consenso; copiar `EL FUTURO NO ACEPTA RECLAMOS`.
4. Marcar las tres copias y desplegar «Otras gestiones» para enviar.
5. Ver el comprobante, abrir la explicación de Brier y volver al inicio.
6. Probar que un porcentaje fuera de 1–99 o un sello incorrecto impide el envío.
