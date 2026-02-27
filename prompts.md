Prompts usados:
1: Crea la estructura HTML semántica para un componente visual de 400px x 300px.
El componente tiene 4 esquinas, y en cada una hay un cuadrado y un círculo.

Requisitos:
- Usa <main> como contenedor de la página
- Usa un <div class="componente"> para el contenedor principal
- Crea 4 <div class="esquina"> dentro del componente, uno por esquina,
  con clases BEM: esquina--sup-izq, esquina--sup-der, esquina--inf-izq, esquina--inf-der
- Dentro de cada esquina coloca un <div class="cuadrado"> y un <div class="circulo">
- No agregues CSS todavía

2:Agrega los estilos base al HTML anterior siguiendo estas especificaciones:
En un archivo styles.css

**Reset:**
- Aplica box-sizing: border-box con el selector universal (*)
- Elimina margin y padding del body

**Colores con variables CSS en :root:**
- --color-fondo: #12219A
- --color-cyan: #70CCDB
- --color-rosado: #DB5EAD

**Contenedor .componente:**
- width: 400px y height: 300px
- background-color: var(--color-fondo)

**Figuras (usa las variables, no valores directos):**
- .cuadrado: width: 70px, height: 70px, background-color: var(--color-cyan)
- .circulo: width: 70px, height: 70px, background-color: var(--color-rosado),
  border-radius: 50%

Usa selectores de clase para mantener baja la especificidad.

3:Centra el contenedor .componente en el medio del viewport usando Flexbox.

Aplica al body:
- display: flex
- justify-content: center  (centra en el eje principal horizontal)
- align-items: center      (centra en el eje cruzado vertical)
- min-height: 100vh        (ocupa toda la altura de la pantalla)
- background-color: var(--color-fondo)  (mismo azul que el contenedor)
- margin: 0

El fondo de la página y el contenedor no deben ser el mismo color (#12219A).
el fondo de la pagina es blanco

4:Posiciona los pares de figuras en las 4 esquinas del contenedor
replicando exactamente este orden:

- esquina--sup-izq: [cuadrado] [círculo]
- esquina--sup-der: [círculo]  [cuadrado]
- esquina--inf-izq: [círculo]  [cuadrado]
- esquina--inf-der: [cuadrado] [círculo]

En .componente aplica:
- display: flex
- flex-wrap: wrap
- justify-content: space-between
- align-content: space-between
- padding: 10px

En cada .esquina aplica:
- display: flex
- align-items: center
- gap: 8px

Para invertir el orden visual sin tocar el HTML usa flex-direction: row-reverse
en .esquina--sup-der y .esquina--inf-izq

Agrega en .cuadrado:hover y .circulo:hover:
- transform: scale(1.1)
- transition: transform 0.2s ease

5: Ahora por ultimo modifica las figuras para que queden de 50px y esten en las esquinas del contenedor, pasame el styles.css finalizado con la ultima modificacion realizada.