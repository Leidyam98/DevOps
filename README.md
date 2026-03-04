
**A05:2025 - Injection**

**Descripción de cada vulnerabilidad**
Esta categoría abarca vulnerabilidades que se presentan cuando una aplicación permite que datos no confiables lleguen a un intérprete (como una base de datos, navegador, sistema operativo o motor de búsqueda) y estos se procesen como instrucciones en lugar de simples datos.

**Métodos de explotación**:
- **SQL Injection**: alterar consultas a bases de datos.
- **Cross-Site Scripting (XSS)**: inyectar código malicioso en páginas web.
- **Command Injection: ejecutar** comandos en el sistema operativo.

Paso 1 – Contexto del sistema Un módulo de búsqueda arma consultas dinámicas para filtrar registros.
Paso 2 – Acción general del atacante El atacante introduce un valor diseñado para cambiar el significado de la consulta en vez de solo “buscar”.
Paso 3 – Resultado o impacto La aplicación devuelve información que no debería o ejecuta operaciones no previstas, afectando datos y confidencialidad.

[](https://media.licdn.com/dms/image/v2/D4E12AQEow10bwC4owg/article-inline_image-shrink_1500_2232/B4EZwfVL.CHsAU-/0/1770052175407?e=1774483200&v=beta&t=V8-LW0STE7d8efWUmwJc9EjT_H_ed_AlxNTB2vPDMgk)

### Ejemplo ataque real

**Vulnerabilidad de inyección SQL en MOVEit Transfer**
En mayo de 2023, Progress reveló una vulnerabilidad crítica de inyección SQL en MOVEit Transfer, identificada como ![CVE-2023-34362](https://www.indusface.com/blog/moveit-zero-day-indusface-coverage/) . Esta falla permitía el acceso no autorizado a bases de datos, lo que hacía vulnerables los datos confidenciales. Atacantes asociados con el grupo de ransomware Clop la explotaron como un ataque de día cero antes de que se corrigiera la vulnerabilidad.

Impacto : Se comprometieron bases de datos y se robó información confidencial. La disponibilidad de código de prueba de concepto (PoC) aumentó la probabilidad de mayor explotación por parte de otros actores maliciosos que atacaban sistemas sin parches.

**Mejores prácticas de prevención y mitigación**:

- Validación estricta de entradas (listas blancas, sanitización).
- Uso de consultas parametrizadas (prepared statements).
- Escapado adecuado de datos antes de enviarlos a intérpretes.
- Principio de menor privilegio en bases de datos y sistemas.
- Frameworks seguros que separen datos de comandos.

**A06:2025 - Insecure Design**
**Descripción de cada vulnerabilidad**
El diseño inseguro comprende vulnerabilidades que surgen debido a controles de seguridad mal planteados o inexistentes desde la etapa de diseño. Aunque un diseño adecuado puede verse afectado por errores durante la implementación, un diseño deficiente no puede corregirse únicamente con una ejecución técnica impecable, ya que los controles necesarios nunca fueron considerados. Una causa común es la falta de un análisis de riesgos que permita establecer el nivel de protección requerido para el sistema o software.

**Métodos de explotación**:
Paso 1 – Contexto del sistema
Un sistema ofrece un beneficio comercial bajo ciertas condiciones (por ejemplo, reservas o descuentos).

Paso 2 – Acción general del atacante
El atacante explota un vacío en el diseño del flujo para forzar un comportamiento no previsto (sin romper técnicamente nada).

Paso 3 – Resultado o impacto
El negocio pierde dinero o sufre abuso operativo porque el sistema nunca diseñó defensas para ese escenario.

[](<img width="1536" height="291" alt="image" src="https://github.com/user-attachments/assets/8278eb84-76e4-4f0b-9fe4-310cd207f96f" />
)

<image src="img width="1536" height="291" alt="image" src="https://github.com/user-attachments/assets/8278eb84-76e4-4f0b-9fe4-310cd207f96f" alt="Descripción de la imagen">
**Mejores prácticas de prevención y mitigación**:

**A07:2025 - Authentication Failures**

https://www.indusface.com/learning/injection-attacks/

**Descripción de cada vulnerabilidad**

**Métodos de explotación**:

**Mejores prácticas de prevención y mitigación**:

Injection - https://www.indusface.com/learning/injection-attacks/
