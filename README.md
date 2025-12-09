# Prueba-LMGSI-
Raquel González Carrillo 
# Ejercicio 1
## Ejercicio 1a
¿Por qué NO se centra el texto del <h1> en este caso? Explícalo con tus palabras. (por qué visual y estructuralmente no aparece centrado entre el borde izquierdo y el menú)
(Primero hay que mencionar que el fichero de css no esta vinculado con el html, por lo que no va a funcionar) No funciona porque .site-header esta usando flex (display: flex) y flexbox cambia totalmente el orden de los elementos. Al quitarlo, h1 se alinea al centro. 
## Ejericio 1b 
1. Solución con flexbox
   Debido a que en un contenedor flex un margen automático en el eje principal absorbe el espacio sobrante. Si damos margin: 0 auto; a h1, este quedare centrado y el nav se sitúa a la derecha.
   ## CSS NECESARIO
   
.site-header {
  display: flex;
  align-items: center;
}

.site-header h1 {
  margin:0 auto;
}
   
3. Solución CSS Grid
   Para poder colocar h1 en el centro vamos hacer tres columnas iguales  grid-template-columns: 1fr 1fr 1fr; y situar al h1 en la columna central.

   ## CSS NECESARIO
.site-header {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  align-items: center;
}

.site-header h1 {
  grid-column: 2;      
  justify-self: center; 
  margin: 0;
}
## Ejercicio 1C
## CSS NECESARIO
.site-header {
  display: flex;
  flex-direction: column;
  align-items: center; 
         
}

.site-header h1,
.site-header .main-nav {
  margin: 0;
}
## Explicación 
De esta manera los agregamos dentro del header. 
## Ejericio 1D
.site-header {
  display: flex;
  flex-direction: column;
  align-items: center; 
  gap: 30px;    
  background-color: rgb(226, 43, 43);      
  border-bottom: 10px solid rgb(0, 0, 0) ;   
  padding: 20px;
    
}

.site-header h1,
.site-header .main-nav {
  margin: 0;
}
De esta manera podemos agregar un fondo en el header sin tener que afectar al resto del body, asi mismo, incluimos este border-bottom, para ponerlo especificamente en la parte inferior del header para así poder separarla del resto de información 
# Ejercicio 2
## Ejercicio 2a 

Cambio del HTML
<header class="site-header">
<button class="header">☰</button>

  <h1>Mi Sitio Web</h1>

  <nav class="main-nav">
      ...
  </nav>
</header>

## Ejercio 2b
Cambio en el CSS

.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between; 
  height: 50px; 
  padding: 0 20px;
}

.menu-btn {
  font-size: 24px;
  cursor: pointer;
}


.site-header h1 {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  margin: 0;
}

Agregamos el translateX(-50%) y el left 50% para que este perfectamente en el centro.

# Ejercicio 3 
## Ejericio 3A
Se añadio en la carpeta del repositorio



