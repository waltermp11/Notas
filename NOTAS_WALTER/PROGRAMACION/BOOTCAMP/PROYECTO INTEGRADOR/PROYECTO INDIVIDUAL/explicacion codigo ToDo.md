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



<mark class="verde">**primera ronda**</mark>
Walter - expongo
sergio - evalua
Andres - moderador


<mark class="verde">**Segunda ronda**</mark>
walter - evalua
Sergio - modera
andres - expone

**Tercera ronda** 
walter- moderador
sergio - expone
andres - evalua
