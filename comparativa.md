# Comparativa metodológica: Identificación y preservación de evidencias

| | RFC 3227 (IETF) | NIST SP 800-86 | ENFSI (Best Practice Guide) |
|---|---|---|---|
|
| **Concepto de "Identificar"** | Identificar en que estado se encuentra el equipo en ese instante y ver que datos volátiles se pueden extraer sin modificar el sistema (§2.1, §3). | Reconocer que la información no está solamente en el equipo sospechoso, sino que puede estar distribuida por toda la infraestructura de la empresa (§3.1.1). | Evaluar la escena, reconocer dispositivos físicos, lógicos y el perímetro y documentar visualmente el entorno (§8.2, §9.2). |
| **Fuentes de evidencia que contempla** | Registros/caché de CPU, memoria principal (RAM), estado de red, procesos activos, disco, medios extraíbles (§2.1). | Dispositivos de usuario, servidores, equipos de red (switches, cortafuegos), periféricos, servicios cloud y logs (§3.1.1). | Hardware de escritorio, portátiles, móviles, consolas, medios de almacenamiento, cámaras y servicios remotos (§8.2, §9.1). |
| **Criterio de prioridad / orden de actuación** | **Orden estricto de volatilidad**: de más volátil a menos volátil (§2.1). | **Volatilidad funcional e impacto operativo**: Se basa en el riesgo de sobreescritura o caducidad, primero lo más probable a que se sobreescriba y luego lo que menos (§3.1.1). | **Preservación de la escena física y orden de volatilidad contextual**, prioriza aislar los dispositivos, evitando borrados en remoto y proteger la escena para garantizar que las pruebas son válidas en un procedimiento judicial (§8.2, §9.2). |

---

### Coincidencias
Las tres normas prohíben acciones que puedan destruir datos o alterar metadatos. También coninciden en la importancia de guardar los datos volátiles de la memoria y documentar cada paso desde el primer momento.

### Diferencias
La diferencia principal es que la RFC 3227 tiene un enfoque mas individual mientras que la NIST tiene una visión corporativa, como los servidores y red de una empresa.  
Por último la ENFSI tiene una visión pericial, con elementos como la cadena de custodia, el control de la escena física y la recolección de pruebas periféricas.