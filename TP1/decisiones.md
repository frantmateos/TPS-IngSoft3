#Paso 1. 
Forkeamos el repo 

![fork](image.png)

Clones el repo con SSH(mayor seguridad)

![SSH](image-1.png)


Creamos la rama secundaria

![branches](image-3.png)


Usamos el repositorio y hacemos dos cambios separados con sus respectivos commits 

![commit](image-2.png)

Lo que hicimos fue movernos a nuestra rama que creamos para poder trabajar en nuestra tarea( creamos la función despedir) e hicimos dos commits, uno para cada momento que se hizo un cambio. El primero fue cuando se agregó el comentario y el segundo cuando agregamos la función despedir. Estos commits son para la rama TASk-1 donde estamos trabajando

Solucion de error 

![error](image-4.png)

Supongamos que encontramos un error en producción, en este caso la función ErrorFuncion nunca fue definida. Entonces para arreglar este error que debemos solucionar de manera inmediata, sacamos una rama de main para obtener la misma version que tiene el error y solucionamos el error en esa rama

![](image-5.png)

Entonces lo que hicimos fue trabajar en esa rama para solucionar el error, ahora para poder aplicar esos cambios en producción para que no falle mas podriamos hacer con un merge. Eso sería pasarse a la rama “main” y hacer un “git merge hotFix”. y los cambios de la rama hotFix se pasarían a la rama main. En este caso lo vamos a hacer con PRs para hacer el paso 5 también y para actualizar las rama de development también.

![fix](image-6.png)

Creamos la PR que va directo a main para el cambio(como no tenemos un pipeline que limite los cambio a main directo vamos a poder ver reflejado el cambio) en caso de tener un pipeline que pida que lo cambios se hagan de la rama de staging, deberíamos hacer el cambio a staging y después hacer una  PR de staging a main, pero no es el caso.
Mergeamos

![merge](image-7.png)

Hacemos lo mismo de la PR pero de main a development para que esta tambien quede actualizada 

![](image-8.png)

Agregamos un tag en nuestro main para marcar una instancia importante en producción, por ejemplo la versión inicial funcionado.

![](image-9.png)
