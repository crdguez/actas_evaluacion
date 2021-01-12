# Actas de evaluación

 **Notebook** que genera las actas de evaluación a partir de los **informes actilla** extraídos del **Sigad**. En la siguiente documentación el símbolo # representa 1, 2 o 3, según la evaluación que queramos analizar.

## Instrucciones

El *notebook* genera varios documentos:

* **acta_#ev.md**: documento detallado en markdown 
* **acta_#ev.pdf**: documento detallado en pdf a partir del markdown *acta_#ev.md*
* **acta_#ev.docx**: documento detallado en formato docx a partir del markdown *acta_#ev.md*
* **resumen_#ev.md**: documento resumen en markdown
* **resumen_#ev.pdf**: documento detallado en pdf a partir del markdown *resumen_#ev.md*

Para generar todo, se necesitan los siguientes ficheros:

* **est_evaluacion.ipynb**: Notebook a ejecutar para generar las actas. Necesita los siguientes ficheros:
    - **importado#.csv**: Fichero con los resultados en *csv* extraídos del **SIGAD**
    - **alumnos_observaciones#.csv**: Fichero en *csv* con las observaciones a los alumnos que queramos que aparezcan en el acta. Existe un parámetro en el código
    - **template_acta.latex**: Plantilla *latex* que utiliza *pandoc* para dar formato a los ficheros acta en *pdf*
    - **portada.jpeg**: Imagen para la portada de las actas

Para ello el *notebook* tiene varios parámetros modificables (basta buscar en el código y reemplazar el valor de la variable). Los más importantes son:

* *evaluaciones_a_incluir*: Indicar la evaluación para la que vamos a obtener el acta
* *inicio_nombre_fichero*: Por defecto es *importado*. Por tanto para la primera evaluación, por defecto, buscará el fichero *importado1.csv*. 
* *observaciones*: Si la variable vale *True* busca el fichero *alumnos_observaciones#.csv* para añadir observaciones a las actas. Si es *False* no incluye observacioens

