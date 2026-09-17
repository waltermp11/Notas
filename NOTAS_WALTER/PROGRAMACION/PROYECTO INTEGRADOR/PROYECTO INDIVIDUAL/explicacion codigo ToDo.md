# Explicacion Codigo  - App ToDo
## Como capturo los estados de mis 3 botones?
Tengo que entender

```
botonesPrioridad.forEach(boton => {

    boton.addEventListener('click', (e) => {

        botonesPrioridad.forEach(b => b.classList.remove('active', 'border', 'border-white'));

        e.target.classList.add('active', 'border', 'border-white');

        inputPrioridad.value = e.target.getAttribute('data-value');

    });

});
```



