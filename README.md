git add README.md
git commit -m "docs: añadir explicacion sobre commits pequeños al README"
exit



	
cat << 'EOF' >> README.md
git add README.md
git commit -m "docs: añadir explicacion sobre commits pequeños al README"
exit
q

q
q

## Reflexión de Seguridad
1. **¿Por qué .env.example puede publicarse?**
   Porque únicamente sirve de plantilla e indica qué nombres de variables de entorno necesita la aplicación, sin exponer credenciales ni claves reales.
2. **¿Por qué .env debe ignorarse?**
   Porque almacena contraseñas, secretos y tokens reales que comprometerían la seguridad del proyecto si se hicieran públicos.
3. **¿Qué habría que hacer si una contraseña o un token reales se hubieran publicado en GitHub?**
   Se debe revocar e invalidar la credencial inmediatamente en el servicio correspondiente, generar una nueva y purgar el historial de Git para eliminar el dato sensible.
4. **¿Bastaría con eliminar el archivo en un commit posterior? Justificar la respuesta.**
   No, porque Git conserva todos los archivos en su historial, por lo que el token seguiría siendo visible al consultar commits pasados.

## Conflicto Resuelto
Se produjo un conflicto en `index.html` al modificar la misma línea de la presentación en las ramas `main` y `feature/nuevo-eslogan`. Se resolvió evaluando ambas propuestas, redactando una versión final combinada, eliminando los marcadores de control de Git y confirmando el commit de resolución.

## Instrucciones de Apertura
Para visualizar la página web, clona el repositorio localmente y abre el archivo `index.html` en un navegador.

## Instrucciones de Apertura
Para visualizar la página web, clona el repositorio localmente en tu ordenador y abre el archivo `index.html` con cualquier navegador web.

## Sincronización Remota: Fetch vs Pull
1. **¿Qué hizo git fetch?**  
   Descargó el historial y las referencias del servidor remoto sin alterar el directorio de trabajo local ni tus archivos.
2. **¿Qué hizo git pull?**  
   Realiza un `git fetch` seguido de un `git merge` automáticamente para traer e integrar los cambios de golpe.
3. **¿Por qué fetch permite revisar antes de integrar?**  
   Porque al no modificar los archivos de trabajo locales, te permite ejecutar un `git diff` para examinar qué ha cambiado antes de decidir si fusionas.
4. **¿Qué relación existe entre pull, fetch y la integración posterior?**  
   `git pull` es la combinación directa de descargar la información (`fetch`) e integrar o fusionar los datos (`merge`).

## Forks y Colaboración
1. **¿Qué es un fork en GitHub?**  
   Es una copia completa e independiente de un repositorio ajeno alojada en tu propia cuenta de GitHub.
2. **¿En qué se diferencia un fork de una rama?**  
   El fork genera un repositorio nuevo en otra cuenta de usuario; la rama es una línea paralela de trabajo dentro del mismo repositorio.
3. **¿En qué cuenta se almacena un fork?**  
   En la cuenta personal del usuario que hace la copia.
4. **¿Cuándo resulta útil trabajar mediante un fork?**  
   Cuando quieres contribuir a un proyecto en el que no tienes permisos directos de escritura.
5. **¿Qué relación existe entre el repositorio original y el fork?**  
   El fork mantiene un enlace histórico con el original, permitiendo sincronizar cambios y enviar propuestas.
6. **¿Qué es el repositorio upstream?**  
   Es el alias que se le da al repositorio central u original del cual proviene tu fork.
7. **¿Qué diferencia existe entre origin y upstream?**  
   `origin` apunta a tu fork personal; `upstream` apunta al repositorio original del autor del proyecto.
8. **¿Cómo se propone que un cambio del fork llegue al repositorio original?**  
   Mediante la creación de una Pull Request (PR) hacia la rama principal del repositorio original.
9. **¿Quién decide si se acepta la propuesta?**  
   Los mantenedores o administradores del repositorio original.
10. **¿Puede seguir evolucionando el repositorio original mientras existe el fork?**  
    Sí, por ello es necesario sincronizar periódicamente tu fork trayendo las novedades de `upstream`.
