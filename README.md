
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

![](https://media.licdn.com/dms/image/v2/D4E12AQEow10bwC4owg/article-inline_image-shrink_1500_2232/B4EZwfVL.CHsAU-/0/1770052175407?e=1774483200&v=beta&t=V8-LW0STE7d8efWUmwJc9EjT_H_ed_AlxNTB2vPDMgk)

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

![](https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/file-uploads/blogs/2147492532/images/162cabe-0b28-1408-4362-db8b47f2be84_ChatGPT_Image_1_feb_2026_02_57_39_a.m..png)

**Mejores prácticas de prevención y mitigación**:

**A07:2025 - Authentication Failures**

**Descripción de cada vulnerabilidad**

Estas fallas ocurren cuando las aplicaciones permiten a los atacantes comprometer contraseñas, claves, tokens de sesión o explotar fallas de implementación para suplantar la identidad de los usuarios. Desde el robo de credenciales y los ataques de fuerza bruta hasta el secuestro de sesiones y mecanismos de recuperación de contraseñas débiles, estas vulnerabilidades permiten el acceso no autorizado que evade todos los demás controles de seguridad.

**Métodos de explotación**:
Paso 1 – Contexto del sistema
Una aplicación usa solo contraseña y permite intentos repetidos de login.

Paso 2 – Acción general del atacante
El atacante prueba credenciales reutilizadas filtradas en incidentes anteriores, de forma automatizada.

Paso 3 – Resultado o impacto
Consigue acceso a cuentas reales, toma control de perfiles y opera como el usuario legítimo.

![](https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/file-uploads/blogs/2147492532/images/5a0c670-e521-5cad-4fcf-c51f0203b430_ChatGPT_Image_1_feb_2026_03_04_47_a.m..png)


**Mejores prácticas de prevención y mitigación**:
- Fortalecer la autenticación mediante MFA, claves de acceso (passkeys) y autenticación adaptativa basada en riesgos para prevenir robo de credenciales y phishing.

- Proteger contra ataques automatizados implementando detección avanzada de bots, limitación de intentos, bloqueo de cuentas y monitoreo continuo de anomalías.

- Aplicar buenas prácticas en contraseñas y sesiones, incluyendo políticas alineadas a estándares (NIST), uso de gestores de contraseñas y gestión segura de sesiones.

- Asegurar recuperación y monitoreo de credenciales, reforzando flujos de restablecimiento, verificando filtraciones y utilizando soluciones de autenticación confiables y probadas.

Injection - https://www.indusface.com/learning/injection-attacks/
