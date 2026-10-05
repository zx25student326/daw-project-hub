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
