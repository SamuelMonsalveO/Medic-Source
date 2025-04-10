Startup Challenge: Ejemplo Resuelto - "Medic Source"

Nombre del producto

Medic Source – Una página web para el control y gestión de inventario de medicamentos en Clinicas, con alertas de vencimiento, escasez y reportes automatizados.

Product Owner – Requisitos

•	Problema que resuelve: Software web orientado al control de la compra, venta y distribución de medicamentos.

•	Público objetivo: Centros de salud (clínicas, hospitales, ips , eps ).

•	3 funcionalidades clave:

o	Regulación y control de caducidad (es decir indicar en que momento podría estar próximo a vencerse un medicamento o si ya venció).

o	Control de la adquisición y venta de medicamentos (referente a la cantidad de medicamentos que se compran y venden).

o	Control de medicamentos que tiene la institución (cantidad que tiene su stock inventariado).

Analista – Análisis

•	Tareas:

o	Definir estructura de base de datos (medicamento, cantidad, fecha de vencimiento, stock mínimo).

o	Lógica de alertas y notificaciones.

o	Generación de reportes en PDF o Excel.

•	Dificultad estimada:

o	Inventario: media

o	Alertas: alta

o	Reportes: media

•	Restricciones:

o	Acceso con login seguro para cada empresa.

o	Datos deben almacenarse de forma local o en servidor seguro (según la versión).

Diseñador UX/UI – Bocetos y flujo

 

Desarrollador – Implementación

•	Feature implementada: 

o	Nombre: Registro y control de caducidad de medicamentos

o	Objetivo: Prevenir el uso de medicamentos vencidos en instituciones de salud.

•	Pseudocódigo:

Inicio de aplicacio

1.	Conexión a Supabase:

a.	Se carga la URL y clave secreta desde un archivo .env.

b.	Se utiliza la librería @supabase/supabase-js para conectarse a la base de datos.

2.	Inicialización de la App React:

a.	Se renderiza una barra lateral con navegación entre módulos.

b.	Los módulos disponibles son: 

i.	Dashboard

ii.	Hospitals

iii.	Medications

iv.	Patients

v.	Usage

3.	Ruteo y Navegación:

a.	Se usa react-router-dom para controlar rutas.

b.	Ejemplos: 

i.	Ruta / → Carga el componente Dashboard.

ii.	Ruta /hospitals → Muestra listado de hospitales.

iii.	Ruta /medications → Muestra medicamentos disponibles.

iv.	Ruta /patients → Lista de pacientes.

v.	Ruta /usage → Permite visualizar el uso de medicamentos y costos por paciente.

4.	Comportamiento de los Componentes:

a.	Cada módulo: 

i.	Hace fetch de datos desde Supabase.

ii.	Muestra los resultados en tablas o tarjetas.

iii.	Permite crear, editar o eliminar registros mediante formularios.

iv.	Algunos formularios utilizan validación básica con react-hook-form.

5.	Validación del Código y Buenas Prácticas:

a.	Se usa TypeScript para tipado estatíco.

b.	Se ejecuta ESLint para mantener la calidad del código.

c.	Las consultas a Supabase están tipadas para prevenir errores.



QA Tester – Pruebas

•	Caso 1: El medicamento se registra correctamente y aparece en el listado.

•	Caso 2: El medicamento buscado aparece correctamente.

•	Caso 3: Los cambios se guardan y se actualiza ebnel sistema correctamente. 

•	Caso 4: El stock se actualiza correctamente según el movimiento.

•	Errores esperados:

o	No se muestran alertas de medicamentos caducados. 

o	Si hay muchos registros, empieza a bsjar rendimiento o se congela. 

o	Algunas funciones no funcionan bien en algunos navegadores (safari :) ).

o	Usuarios sin rol puede editar o eliminar medicamentos.



DevOps/Mantenimiento – Despliegue

1. Integración con Inteligencia Artificial para Predicción de Consumo

¿Qué hace?

•	Analiza los datos históricos sobre cuántos medicamentos se han usado en hospitales o farmacias.

•	Con esa información, predice cuánto se va a necesitar en el futuro.

2. Interfaz de Reportes en Tiempo Real y Alertas Automatizadas

¿Qué hace?

•	Muestra reportes dinámicos sobre: 

o	Disponibilidad actual de medicamentos.

o	Costos totales por paciente.

o	Uso excesivo de un medicamento.

•	Envía alertas automáticas cuando algo importante ocurre, por ejemplo: 

o	Si se está por agotar un medicamento.

o	Si un paciente está recibiendo dosis muy frecuentes.



DESPLIEGUE DE LA APLICACIÓN

1. Servidor Backend 

2. Frontend

3. Seguridad y Escalabilidad

