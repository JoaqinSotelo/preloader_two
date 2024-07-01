## Descripción

Este proyecto es un preloader simple y elegante implementado completamente con HTML y CSS. Los preloaders son una excelente manera de mejorar la experiencia del usuario al proporcionar una indicación visual de que el contenido se está cargando.

## Características

- 100% HTML y CSS, sin JavaScript adicional.
- Compatible con todos los navegadores modernos.
- Diseño responsivo.
- Fácil de integrar en cualquier proyecto web.

## Vista Previa

Puedes ver una demostración en vivo [aquí](https://codepen.io/JoaqinSotelo/pen/qBGzzQy).

## Uso

### Instrucciones de Integración

1. **HTML:** Añade el siguiente código en el cuerpo (`<body>`) de tu documento HTML.

    ```html
    <div class="preloader">
        <div class="spinner"></div>
    </div>
    ```

2. **CSS:** Añade el siguiente código en tu archivo CSS o en una etiqueta `<style>` dentro del `<head>` de tu HTML.

    ```css
    /* Preloader CSS */
    .preloader {
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        z-index: 9999;
        background-color: #fff;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .spinner {
        border: 16px solid #f3f3f3;
        border-radius: 50%;
        border-top: 16px solid #3498db;
        width: 120px;
        height: 120px;
        -webkit-animation: spin 2s linear infinite;
        animation: spin 2s linear infinite;
    }

    @-webkit-keyframes spin {
        0% { -webkit-transform: rotate(0deg); }
        100% { -webkit-transform: rotate(360deg); }
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }

3. **JavaScript:** Añade el siguiente código JavaScript para ocultar el preloader una vez que la página haya terminado de cargar.

    ```javascript
    window.addEventListener('load', function () {
        document.querySelector('.preloader').style.display = 'none';
        document.querySelector('.content').style.display = 'block';
    });
    ```

### Personalización

Puedes personalizar el preloader ajustando los estilos CSS. Por ejemplo, para cambiar el color del spinner, modifica la propiedad `border-top` en la clase `.spinner`.

```css
.spinner {
    border-top: 16px solid #3498db; /* Cambia este color al que prefieras */
}
