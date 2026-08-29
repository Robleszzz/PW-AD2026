<h2>1. Comando</h2>
<code>git clone [URL]</code>
<h2>Descripción</h2>
Copia un repositorio remoto completo a la computadora local
<h2>Ejemplo de caso de uso</h2>
Para descargar un proyecto existente desde github</br>
<code>git clone https://github.com/usuario/proyecto.git</code>

<h2>2. Comando</h2>
<code>git status</code>
<h2>Descripción</h2>
Muestra el estado actual de repositorio, incluyendo archivos modificados, nuevos o preparados para confirmación
<h2>Ejemplo de caso de uso</h2>
Si se modifico por ejemplo <code>index.html</code> y se quiere saber qué se cambió, se escribe:</br>
<code>git status</code>

<h2>3. Comando</h2>
<code>git add</code>
<h2>Descripción</h2>
Agrega uno o varios archivos en el area de preparaciòn para incluirlos en el próximo 
<h2>Ejemplo de caso de uso</h2>
Para preparar un archivo en especifico:</br>
<code>git add index.html</code></br>
Tambien se pueden agregar todos los cambios:</br>
<code>git add .</code>

<h2>4. Comando</h2>
<code>git commit -m "mensaje"</code>
<h2>Descripción</h2>
Guarda los cambios preparados en el historial del repositorio con un mensaje descriptivo
<h2>Ejemplo de caso de uso</h2>
Depues de modificar el código: </br>
<code>git add .</code></br>
<code>git commit -m "Agrega pagina principal"</code>

<h2>5. Comando</h2>
<code>git log</code>
<h2>Descripción</h2>
Muestra el historial de commits realizados en el repositorio.
<h2>Ejemplo de caso de uso</h2>
Para revisar los cambios realizados anteriormente:</br>
<code>git log</code></br>
Una version resumida:</br>
<code>git log --oneline</code>

<h2>6. Comando</h2>
<code>git branch</code>
<h2>Descripción</h2>
Muestra las ramas existentes en el repositorio. tambien permite crear y eliminar ramas
<h2>Ejemplo de caso de uso</h2>
Para crear una rama para desarrollar una nueva funcionalidad:</br>
<code>git branch nueva-funcionalidad</code>

<h2>7. Comando</h2>
<code>git switch [rama]</code>
<h2>Descripción</h2>
Nos permite cambiar de una rama a otra
<h2>Ejemplo de caso de uso</h2>
Para cambiar la rama de desarrollo:</br>
<code>git switch desarrollo</code></br>
Tambien se puede crear y cambiar a una nueva rama:</br>
<code>git switch -c nueva-funcionalidad</code>

<h2>8. Comando</h2>
<code>git merge [rama]</code>
<h2>Descripción</h2>
Combina los cambios de una rama con la rama actual
<h2>Ejemplo de caso de uso</h2>
Si se está en <code>main</code> y se quiere incorporar el trabajo de <code>desarrollo</code>:</br>
<code>git switch main</br>
git merge desarrollo</code>

<h2>9. Comando</h2>
<code>git remote -v</code>
<h2>Descripción</h2>
Muestra los repositorios remotos asociados al repositorio local
<h2>Ejemplo de caso de uso</h2>
Para comprobar a qué repositorio remoto está conectado el proyecto:</br>
<code>git remote -v</code>

<h2>10. Comando</h2>
<code>git pull</code>
<h2>Descripción</h2>
Descarga los cambios del repositorio remoto y los integra en la rama local actual
<h2>Ejemplo de caso de uso</h2>
Antes de comenzar, se pueden obtener los cambios más recientes:</br>
<code>git pull origin main</code>

<h2>11. Comando</h2>
<code>git push</code>
<h2>Descripción</h2>
Envia los commits realizados localmente al repositorio remoto
<h2>Ejemplo de caso de uso</h2>
Después de realizar un commit:</br>
<code>git push origin main</code>

<h2>12. Comando</h2>
<code>git fetch</code>
<h2>Descripción</h2>
Descarga información y cambios del repositorio remoto sin incorporarlos automáticamente a la rama local
<h2>Ejemplo de caso de uso</h2>
Para revisar si existen cambios remotos antes de integrarlos:</br>
<code>git fetch origin</code>

<h2>13. Comando</h2>
<code>git diff</code>
<h2>Descripción</h2>
Muestra las diferencias entre los archivos modificados y la última version registrada.
<h2>Ejemplo de caso de uso</h2>
Para revisar qué código se modificó antes de hacer <code>git add</code>:</br>
<code>git diff</code>

<h2>14. Comando</h2>
<code>git restore [archivo]</code>
<h2>Descripción</h2>
Permite descartar modificaciones no confirmadas de un archivo y restaurarlo a su estado anterior
<h2>Ejemplo de caso de uso</h2>
Si se realizaron cambios por error en <code>index.html</code>:</br>
<code>git restore index.html</code></br>
NOTA: Este comando pude eliminar cambios locales no guardados, por lo que debe utilizarse con cuidado

<h2>15. Comando</h2>
<code>git reset [archivo]</code>
<h2>Descripción</h2>
Quita un archivo del área de preparación sin eliminar las modificaciones realizadas en él
<h2>Ejemplo de caso de uso</h2>
Si se agregó un archivo por error al staging:</br>
<code>git add index.html</br>
git reset index.html</code></br>
NOTA: El archivp deja de estar preparado, pero sus modificaciones se conservan

<h2>16. Comando</h2>
<code>git rm [archivo]</code>
<h2>Descripción</h2>
Elimina un archivo del proyecto y registra su eliminación para el próximo commit
<h2>Ejemplo de caso de uso</h2>
Para eliminar un archivo que ya no se necesita:</br>
<code>git rm archivo-obsoleto.txt</br>
git commit -m "Elimina archivo obsoleto"</code>

<h2>17. Comando</h2>
<code>git tag [nombre]</code>
<h2>Descripción</h2>
Crea una etiqueta que permite identificar un commit especifico, normalmente para marcar versiones del proyecto
<h2>Ejemplo de caso de uso</h2>
Para marcar una versión estable:</br>
<code>git tag v1.0.0</code></br>
Después se puede enviar la etiqueta al repositorio remoto</br>
<code>git push origin v1.0.0</code>

<h2>18. Comando</h2>
<code>git stash</code>
<h2>Descripción</h2>
Guarda temporalmente los cambios locales sin necesidad de realizar un commit
<h2>Ejemplo de caso de uso</h2>
Si se está trabajando en una funcionalidad pero se necesita cambiar temporalmente de rama:</br>
<code>git stash</br>
git switch main</code></br>
para recuperar posteriormente los cambios:</br>
<code>git stash pop</code>

<h2>19. Comando</h2>
<code>git config</code>
<h2>Descripción</h2>
Permite configurar diferentes opciones de Git, como el nombre y correo electrónico del usuario
<h2>Ejemplo de caso de uso</h2>
Configura la identidad que aparecerá en los commits></br>
<code>git config --global user.name "Tu Nombre"</br>
git config --global user.email "ejemplo@gmail.com"</code>

<h2>20. Comando</h2>
<code>git checkout [rama]</code>
<h2>Descripción</h2>
Permite cambiar de una rama a otra dentro de un repositorio de Git
<h2>Ejemplo de caso de uso</h2>
Si se tiene una rama llamada <code>Desarrollo</code> y se quiere cambiar a ella:</br>
<code>git checkout desarrollo</code>
