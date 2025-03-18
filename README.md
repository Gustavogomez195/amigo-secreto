# Proyecto "Amigo Secreto" 

## Descripción  del proyecto
Este proyecto es un sistema que permite a los usuarios agregar nombres a una lista de amigos y luego sortear al azar un "Amigo Secreto". Fue desarrollado en **JavaScript** y manipula el **DOM** para actualizar dinámicamente la lista de participantes y mostrar el resultado del sorteo.  

El objetivo de este desafío es mejorar las habilidades en lógica de programación y la manipulación de arreglos en JavaScript.  

---

## Describe Funcionalidades  
✅ Permite agregar nombres a una lista de amigos.  
✅ Evita agregar nombres duplicados.  
✅ Muestra la lista actualizada en pantalla.  
✅ Sortea un amigo secreto al azar.  
✅ Muestra el resultado en la interfaz.  

---

## Listando Archivos principales  
- `index.html` → Contiene la estructura HTML de la aplicación.  
- `app.js` → Implementa la lógica de agregar amigos y realizar el sorteo.  
- `style.css` → Contiene los estilos de la interfaz (opcional).  

---

## Instalación y ejecución del código
1. Descarga o clona este repositorio.  
2. Abre el archivo **`index.html`** en cualquier navegador.  
3. Escribe un nombre en el campo de texto y presiona "Añadir".  
4. Cuando hayas agregado todos los nombres, presiona "Sortear amigo".  
5. El resultado aparecerá en pantalla.  

---

## Código principal y funciones

### `agregarAmigo()`  
Esta función:  
- Obtiene el nombre ingresado en el campo de texto.  
- Valida que el campo no esté vacío.  
- Evita nombres repetidos en la lista.  
- Agrega el nombre al arreglo y actualiza la lista en pantalla.  

```javascript
function agregarAmigo(){
 
    let nombreDeAmigo = document.getElementById("amigo").value;
    
    if (nombreDeAmigo === "") {
        alert("Por favor, ingresa un nombre válido.");
        return;
    }

     // Validar si el nombre ya está en la lista
     if (amigos.includes(nombreDeAmigo)) {
        alert("Este nombre ya ha sido ingresado. No puedes agregarlo nuevamente.");
        amigo.value = "";
        return;
    }
    
    amigos.push(nombreDeAmigo);
 
    // Limpiar el input después de agregar
    amigo.value = "";
    
    // Actualizar la lista en la pantalla
    mostrarAmigos();

    return;
}
