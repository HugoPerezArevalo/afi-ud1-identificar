# Comparativa metodológica: Identificación y preservación de evidencias

| | RFC 3227 (IETF) | NIST SP 800-86 | ENFSI (Best Practice Guide) |
|---|---|---|---|
| **Concepto de "Identificar"** | Identificar en qué estado se encuentra el equipo en ese instante y ver qué datos volátiles se pueden extraer sin modificar el sistema (§2.1, §3). | Reconocer que la información no está solamente en el equipo sospechoso, sino que puede estar distribuida por toda la infraestructura de la empresa (§3.1.1). | Evaluar la escena, reconocer dispositivos físicos, lógicos y el perímetro, y documentar visualmente el entorno (§8.2, §9.2). |
| **Fuentes de evidencia que contempla** | Registros/caché de CPU, memoria principal (RAM), estado de red, procesos activos, disco, medios extraíbles (§2.1). | Dispositivos de usuario, servidores, equipos de red (switches, cortafuegos), periféricos, servicios cloud y logs (§3.1.1). | Hardware de escritorio, portátiles, móviles, consolas, medios de almacenamiento, cámaras y servicios remotos (§8.2, §9.1). |
| **Criterio de prioridad / orden de actuación** | **Orden estricto de volatilidad**: de más volátil a menos volátil (§2.1). | **Volatilidad funcional e impacto operativo**: se basa en el riesgo de sobrescritura o caducidad; primero lo más probable a que se sobrescriba y luego lo que menos (§3.1.1). | **Preservación de la escena física y orden de volatilidad contextual**: prioriza aislar los dispositivos evitando borrados en remoto y proteger la escena para garantizar la validez en un procedimiento judicial (§8.2, §9.2). |

---

### Coincidencias
Las tres normas prohíben acciones precipitadas que puedan destruir datos o alterar metadatos (principio de mínima alteración). También coinciden en la importancia crítica de salvaguardar los datos volátiles de la memoria antes de apagar el sistema y en la obligatoriedad de documentar cada paso desde el primer instante.

### Diferencias
La diferencia principal radica en el alcance y la perspectiva:
- La **RFC 3227** tiene un enfoque técnico e individual, centrado exclusivamente en el sistema anfitrión encendido frente al analista.
- La **NIST SP 800-86** aporta una visión corporativa y de red, considerando la infraestructura completa (servidores, proxys, cortafuegos y nube).
- La **ENFSI** adopta un prisma pericial y procesal, priorizando la legalidad, la cadena de custodia, el control del entorno físico, los testimonios y los dispositivos del entorno (como el CCTV).

Estas diferencias son determinantes en la práctica: si solo aplicáramos la RFC 3227 nos centraríamos en la RAM del portátil y se nos escaparían los logs rotativos del cortafuegos o las grabaciones de la cámara de seguridad. Del mismo modo, si aplicáramos únicamente la NIST podríamos olvidar aislar las comunicaciones de un dispositivo móvil frente a un borrado remoto antes de analizarlo.