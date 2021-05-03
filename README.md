# Gabo
## Patron builder para la construcción de elementos del dom



## Caracteristicas
JS Puro
## Uso

En cualquier navegador o entorno para ejecutar JS

Crea un objecto Gabo y decoralo con las etiquetas que quieras.

```sh
var td_aux = new Gabo("td").setId(0).setClass("center").build();
```

## Como aportar al codigo

Lastimosamente no estan todas las attributes definidos. Si alguien desea, puede agregar y enriquecerlo de la siguente forma:
En el constructor:
```sh
...
  constructor(tag) {
        this.newAtributte = null;
 }
 ...
```
Luego agregar el set:
```sh
...
 setnewAtributte(newAtributte) {
    this.newAtributte = newAtributte;
    return this;
 }
 ...
```

Por último modificar el set parameter:
```sh
...
setParameters(element) {
    if (this.newAtributte != null) {
        element.setAttribute("newAtributte", this.newAtributte);
    }
...          
}
```