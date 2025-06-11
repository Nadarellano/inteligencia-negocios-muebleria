# 📊 Inteligencia de Negocios – Caso Muebles Aconcagua  
**Optimización del análisis de ventas mediante integración de datos y visualización interactiva**


Este proyecto simula una solución de Business Intelligence para la empresa ficticia **Muebles Aconcagua**, desarrollada como parte de una formación en análisis de datos e inteligencia de negocios.

---

## Fuentes de Datos
Este proyecto utiliza datos simulados y generados con fines educativos. Todos los datos han sido diseñados exclusivamente para este proyecto de análisis y visualización y no corresponden a información real de personas ni empresas.

---

## Estructura del Proyecto

🔹 Base de datos modelo relacional `.bak` y archivo de texto `.txt`  
🔹 Carga ETL automatizada con **IDE Visual Studio** y **SQL Server Integration Services Projects (SSIS)**  
🔹 Modelo dimensional tipo estrella `.bak`  
🔹 Dashboard interactivo desarrollado con **Power BI**  

---

## Herramientas Utilizadas

- SQL Server Management Studio (SSMS)
- SQL Server Integration Services Projects (SSIS)
- IDE Visual Studio
- Power BI Desktop

---

## Preguntas de Negocio

- ¿Qué productos fueron los más comprados por solteros en Viña del Mar durante 2015?
- ¿Cómo evolucionaron las ventas por sucursal a lo largo del año?
- ¿Qué categoría de productos aportó más al ingreso total?
- ¿Cuál fue el desempeño individual de cada vendedor en enero de 2015?

---

## 📈 Resultados

El dashboard desarrollado permite obtener insights relevantes para la toma de decisiones, como:
- Identificar productos más vendidos por región
- Medir el desempeño comercial por categoría y vendedor
- Detectar patrones de compra según perfil de cliente

---

## 📁 Estructura del Repositorio
  
| Carpeta          | Contenido                                                                    |
|------------------|---------------------------------------------------------------------------   |
| `backup/`        | BD relacional inicial `.bak` y archivo de texto con estado civil clientes    |
| `dashboard/`     | Archivo `.pbix` con el dashboard final desarrollado en Power BI Desktop.     |
| `datawarehouse/` | Datos procesados (modelo dimensional) `.bak` para análisis y visualización.  |
| `docs/`          | Informe técnico completo y resumen profesional del proyecto.                 |
| `etl/`           | Flujo de trabajo ETL `.dtsx` desarrollado en SQL Server Integration Services |

---

## Cómo Usar Este Proyecto

1. **Restaurar la base de datos original:**
   - Usar el archivo `.bak` desde `/backup/` en SQL Server Management Studio.

2. **Cargar el modelo dimensional:**
   - Restaurar la BD desde `/datawarehouse/`.

3. **Revisar el flujo ETL:**
   - Abrir el archivo `.dtsx` desde `/etl/` en Visual Studio con SSDT.

4. **Explorar el dashboard:**
   - Abrir `dashboard.pbix` desde Power BI Desktop y conectar con el modelo restaurado.

---

## 🧩 ETL con Integration Services (SSIS)
El archivo Package.dtsx contiene el flujo de trabajo ETL desarrollado en SQL Server Integration Services (SSIS) para el proyecto de análisis de ventas de Muebles Aconcagua.

¿Qué hace este paquete?
- Carga datos desde múltiples fuentes: archivos planos y una base de datos relacional (.bak).
- Transforma y limpia datos: ajusta columnas, tipos y relaciones.
- Carga a un modelo estrella: con tablas dimensiones (DIM_PRODUCTO, DIM_CLIENTE, etc.) y la tabla de hechos (FACT_VENTA).

¿Cómo abrir el archivo .dtsx?
- Abre Microsoft Visual Studio con el componente SQL Server Data Tools (SSDT) instalado.
- Crea un proyecto nuevo de tipo Integration Services Project o abre uno existente.
- Agrega el archivo Package.dtsx al proyecto.
- Visualiza el flujo de control y los flujos de datos desde la vista de diseño.

### Carga Histórica de Clientes
Para evitar conflictos y pérdida de información en futuras ejecuciones del proceso ETL, se implementó una carga histórica en la dimensión de clientes. Esto significa que, cuando un registro de cliente cambia (por ejemplo, cambia su comuna o estado civil), el sistema no lo sobrescribe, sino que crea una nueva versión del registro.

---

## Documentos
- [PDF Resumen del Proyecto](docs/Resumen_Técnico_Inteligencia_de_Negocio.pdf)
- [PDF Detallado del Proyecto](docs/Informe_Completo_Inteligencia_de_Negocio.pdf)
- [Ver presentación en LinkedIn](https://www.linkedin.com/posts/activity-7325630377660706816-_4m3?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAScY54Bz1v1B1JB3pZedXQTIUvQ5jjX7XU)
