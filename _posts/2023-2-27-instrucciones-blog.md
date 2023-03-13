---
layout: post
title: "Comandos de consola para el blog"
---

Este blog es un sitio estático creado con Jekyll y alojado en Github Pages. Hacerlo fue sencillo, pero un poco tedioso. Hay que saber usar comandos básicos en la consola para generar la página localmente, hacer cambios con Git y después subirla al repositorio de Github. Algunos pasos y comandos básicos para hacerlo son:

1. Asegurarse de estar en el directorio del blog local con `cd`
2. Después de cada cambio hecho en los archivos del blog hay que ejecutar `exec bundle jekyll serve` para generar la página localmente. Esto hace que los posts escritos en formato Markdown se rendericen en HTML. Si esto no se hace no se despliegan los cambios depsués.
3. Usar comandos de Git para vincular los archivos locales con el repositorio en GH. Se usa `git add .` para añadir todos los cambios hechos en la carpeta. Se usa `git commit -m "comentario"` para realizar los cambios. Finalmente se usa `git push github gh-pages` o `git push origin gh-pages` para realizar los cambios en el repositorio remoto en Github que hace de servidor.

_Notas_: Hay algunos conflictos con diferentes versiones de software que se utiliza para hacer funcionar el blog. Esto hace que salten varias "deprecaciones". Aún así funciona. Según la teoría, el comando de `exec bundle jekyll serve` solo debería usarse la primera vez que se genera la página y después usar solo `jekyll serve`. En la práctica esto no me funciona por alguna razón que no entiendo. También. La primera vez que hice el blog en mi vieja laptop el comando de git que usaba para hacer `push` contenía el campo `origin`, pero ahora esto no funciona porque ya no se reconoce esta laptop como el origen. Ahora hay que reemplazar `origin` por `github` y hacer una verificación de identidad.