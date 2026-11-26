# sprint7-final-project
Análisis de Clientes ConnectaTel

Análisis exploratorio y segmentación de clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, con datos registrados hasta 2024.

¿Qué hace el proyecto?

El notebook S7 Version-Estudiante-Project-ConnectaTel.ipynb toma tres datasets, los limpia y construye un perfil estadístico de los clientes. El flujo es:

Carga y exploración de plans.csv, users_latam.csv y usage.csv (estructura, tipos de datos y vista rápida).
Identificación de problemas de calidad: valores nulos, valores centinela (-999 en age, "?" en city) y fechas fuera de rango (registros con año 2026).
Limpieza básica: reemplazo de centinelas, tratamiento de fechas imposibles y verificación de que los nulos en duration y length son MAR (dependen del tipo de registro: llamada o mensaje).
Resumen de uso por usuario: total de mensajes, llamadas y minutos, combinado con la tabla de usuarios.
Visualización de distribuciones (histogramas por plan) y detección de outliers con boxplots y método IQR.
Segmentación de clientes por nivel de uso (Bajo, Medio, Alto) y por edad (Joven, Adulto, Adulto Mayor).
Insight ejecutivo con conclusiones y recomendaciones para el negocio.
¿Por qué es útil?
Convierte datos crudos en un perfil claro de cómo usan el servicio los clientes.
Detecta y documenta problemas de calidad de datos antes de que afecten el análisis.
Identifica usuarios intensivos (outliers), que son tanto una oportunidad de venta como un riesgo de fuga.
Muestra que el nivel de uso es un mejor criterio de segmentación que la edad, lo que ayuda a diseñar planes y ofertas más precisas.
Sirve de base para decisiones de retención y para ajustar la oferta de planes.
Cómo comenzar
Requisitos
Python 3.9 o superior
Librerías: pandas, seaborn, matplotlib, jupyter
bash
pip install pandas seaborn matplotlib jupyter
Datos

El notebook espera encontrar los archivos en la ruta /datasets/:

/datasets/plans.csv: planes disponibles (precio, minutos, mensajes y GB incluidos, costo por extra).
/datasets/users_latam.csv: clientes (edad, ciudad, fecha de registro, plan, fecha de baja).
/datasets/usage.csv: detalle de llamadas y mensajes.

Si ejecutas el proyecto en otro entorno, ajusta las rutas en la celda de carga de datos.

Ejecución
Clona el repositorio:
bash
git clone <URL-DEL-REPOSITORIO>
cd <NOMBRE-DEL-REPOSITORIO>
Abre el notebook:
bash
jupyter notebook "S7 Version-Estudiante-Project-ConnectaTel.ipynb"

También puedes subirlo a Google Colab (File → Upload notebook) y cargar los CSV en la sesión. 3. Ejecuta las celdas en orden, de arriba hacia abajo (Run All). El orden importa, porque cada paso depende de la limpieza anterior.

Resultados principales
Uso: 73.7% de los clientes está en Uso medio, 19.3% en Bajo uso y 7.0% en Alto uso.
Edad: el comportamiento es casi igual en todos los grupos de edad; el nivel de uso es el segmento que realmente diferencia a los clientes.
Outliers: solo en el extremo superior de mensajes, llamadas y minutos; se conservan por ser usuarios intensivos plausibles.

Las cifras exactas pueden variar si cambias el tratamiento de las fechas fuera de rango (marcarlas como nulas o eliminar las filas).

¿Dónde obtener ayuda?
Abre un Issue en este repositorio describiendo el problema, con el mensaje de error y la celda donde ocurre.
Revisa los comentarios y las secciones de insights dentro del notebook, que explican las decisiones tomadas en cada paso.
Documentación de las librerías: pandas, seaborn y matplotlib.
Mantenimiento y contribuciones

Proyecto desarrollado por [JUAN MARTIN SAHAGUN FLORES] como proyecto final del sprint de análisis de datos.

Las contribuciones son bienvenidas: haz un fork, crea una rama con tus cambios y abre un Pull Request con una descripción clara de lo que modificaste.

Contacto: [juanmartinsahagunflores@gmail.com,  juanmartinsahagunflores-max]
