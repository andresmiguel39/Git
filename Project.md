**siempre se debe iniciar en la rama develop 

1. cd C:/Repositorio_XXXX10/XXXX10001_Name_APP

2. git checkout master <nombre rama> (develop - release - master)
---git branch -D <nombre rama> (para borrarla si se necesita) tambien se borra en VSTS

3. git pull origin  - para actualizar repo local desde vsts

4. git checkout -b features/HA_XXXXX203  para crear la rama

5. copio el archivo fuente en la ruta del repositorio

6. git status (debe salir en rojo)

7. git add -A para traer todo tipo de archivo

8. git status (debe salir en verde)

9. git commit -m "instalacion paquete HA_XXXXX203"

10. git push origin <nombre de rama (featuresfeatures/HA_XXXXX203-06145)> - para subir al repositorio de VSTS los cambios

11. luego ir a vsts repos-branches a verificar la creación de la rama 

12. luego ir a repos pull request y dar crear pull request seleccionar la rama develop y en workitems seleccionar la HU XXXZZW5 para la instalacion y dar crear

queda pendiente la aprobación para pasar a complete y luego complete merge

13. luego ir al pipeline BUILDS verificar el estado en CI sube al repo la nueva rama y en CD pasa la rama a artifactory y hace la dif entre los archivos

luego ir al pipleine de RELEASE para verificar ejecucion de la receta de urbancode

si falla, se hace redeploy, si falla se va a repós-buids se busca el APP_CD y se pone de nuevo en cola

PARA ISNTALAR EN CERTIFICACION
12. luego ir a repos pull request y dar crear pull request seleccionar el paquete de origen y la rama releas y en workitems seleccionar la HU XXXZZW5 para la instalacion y dar crear

queda pendiente la aprobación para pasar a complete y luego complete merge

13. luego ir al pipeline BUILDS verificar el estado en CI sube al repo la nueva rama y en CD pasa la rama a artifactory y hace la dif entre los archivos

luego ir al pipleine de RELEASE para ejecutar la receta de urbancode
