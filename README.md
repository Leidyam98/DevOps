
**A05:2025 - Injection**

**Descripción de cada vulnerabilidad**
Esta categoría abarca vulnerabilidades que se presentan cuando una aplicación permite que datos no confiables lleguen a un intérprete (como una base de datos, navegador, sistema operativo o motor de búsqueda) y estos se procesen como instrucciones en lugar de simples datos.

**Métodos de explotación**:
- SQL Injection: alterar consultas a bases de datos.
- Cross-Site Scripting (XSS): inyectar código malicioso en páginas web.
- Command Injection: ejecutar comandos en el sistema operativo.

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

### Ejemplo ataque real

El sitio web de comercio electrónico de una cadena minorista no cuenta con protección contra bots administrados por revendedores que compran tarjetas de video de alta gama para revenderlas en sitios web de subastas. Esto genera una mala publicidad para los fabricantes de tarjetas de video y los propietarios de las cadenas minoristas, además de generar una mala relación con los aficionados que no pueden obtener estas tarjetas a ningún precio. Un diseño antibots cuidadoso y reglas de lógica de dominio, como las compras realizadas a los pocos segundos de estar disponibles, podrían identificar compras no auténticas y rechazar dichas transacciones.

**Mejores prácticas de prevención y mitigación**:

- Adoptar un SDLC seguro con apoyo de especialistas en AppSec e incorporación de controles de seguridad y privacidad desde el diseño.

- Aplicar diseño seguro y modelado de amenazas, especialmente en componentes críticos, fomentando una mentalidad de seguridad en el equipo.

- Integrar seguridad en todo el desarrollo, incluyendo requisitos en historias de usuario, validaciones en frontend/backend y pruebas basadas en casos de uso y abuso.

- Implementar arquitectura segmentada y aislada, separando capas del sistema y asegurando un aislamiento sólido entre inquilinos.

**A07:2025 - Authentication Failures**

**Descripción de cada vulnerabilidad**

Estas fallas ocurren cuando las aplicaciones permiten a los atacantes comprometer contraseñas, claves, tokens de sesión o explotar fallas de implementación para suplantar la identidad de los usuarios. Desde el robo de credenciales y los ataques de fuerza bruta hasta el secuestro de sesiones y mecanismos de recuperación de contraseñas débiles, estas vulnerabilidades permiten el acceso no autorizado que evade todos los demás controles de seguridad.

![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*yWn8ahHQAmk2ebdwRoIq3Q.png)

**Métodos de explotación**:

Paso 1 – Contexto del sistema
Una aplicación usa solo contraseña y permite intentos repetidos de login.

Paso 2 – Acción general del atacante
El atacante prueba credenciales reutilizadas filtradas en incidentes anteriores, de forma automatizada.

Paso 3 – Resultado o impacto
Consigue acceso a cuentas reales, toma control de perfiles y opera como el usuario legítimo.

![](https://kajabi-storefronts-production.kajabi-cdn.com/kajabi-storefronts-production/file-uploads/blogs/2147492532/images/5a0c670-e521-5cad-4fcf-c51f0203b430_ChatGPT_Image_1_feb_2026_03_04_47_a.m..png)

### Ejemplo ataque real

**El desastre de la API del USPS (2018)**

En noviembre de 2018, el Servicio Postal de Estados Unidos expuso información sobre aproximadamente 60 millones de usuarios debido a una lógica empresarial defectuosa y una autorización deficiente. La API se diseñó para permitir que los usuarios autenticados solicitaran sus propios datos, pero carecía de controles para verificar que solo pudieran acceder a su propia información. Esto no se debió a un error de codificación, sino a una falla de diseño fundamental en la gestión de la autorización por parte de la API.

**Mejores prácticas de prevención y mitigación**:

- Fortalecer la autenticación mediante MFA, claves de acceso (passkeys) y autenticación adaptativa basada en riesgos para prevenir robo de credenciales y phishing.

- Proteger contra ataques automatizados implementando detección avanzada de bots, limitación de intentos, bloqueo de cuentas y monitoreo continuo de anomalías.

- Aplicar buenas prácticas en contraseñas y sesiones, incluyendo políticas alineadas a estándares (NIST), uso de gestores de contraseñas y gestión segura de sesiones.

- Asegurar recuperación y monitoreo de credenciales, reforzando flujos de restablecimiento, verificando filtraciones y utilizando soluciones de autenticación confiables y probadas.

Injection - https://www.indusface.com/learning/injection-attacks/
