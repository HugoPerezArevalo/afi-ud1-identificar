# Plan de identificación Almadraba

## 1. Fuentes de evidencia

### Mesa de trabajo de Marta
1. **Portátil corporativo encendido con la pantalla bloqueada:** Contiene la memoria RAM activa con los procesos, conexiones de red y claves de cifrado cargadas en la memoria.

2. **Disco duro externo conectado al Dock:** Almacenamiento donde puede haberse copiado renders o proyectos.

3. **Móvil de empresa:** Historial de llamadas, conversaciones de WhatsApp.

4. **Pendrive de Marta que "no funciona":** Puede que contenga el render y por eso no quiere usarlo.

### Alrededores y otros puestos de la oficina

5. **Pendrive prestado por Javier:** Utilizado por Marta en el periodo de tiempo en el que ocurrió el incidente.

6. **Equipo compartido de la entrada:** Uso común para imprimir/escanear y con una sesión abierta de Outlook.

### Entorno físico y cloud

7. **Servidor de ficheros:** Donde se guardan los archivos de los proyectos.

8. **NAS:** Contiene las últimas 14 copias diarias.

9. **Cortafuegos:** Guarda logs de trafico y conexiones VPN de Marta.

10. **Portal de Microsoft y OneDrive:** En el portal de Microsoft se guardan las claves de recuperación de BitLocker y en OneDrive se almacenan los documentos de los proyectos y sus logs.

11. **Cámara de vigilancia:** Grabaciones de la franja horaria en la que ocurrió el incidente.

12. **Móvil personal de Marta que asoma en el bolso:** Posible conversación o registro de llamadas con Lucía o descarga de datos.

13. **Impresora común:** Contiene logs de escaneos/impresiones y colas de trabajo recientes.

## 2. Prioridad

1. **Memoria RAM del portátil de empresa:** Si el equipo se apaga se pierde toda la información que había almacenada en la Memoria (procesos, conexiones de red o claves de BitLocker).

2. **Aislar el móvil de empresa:** Para que no se borren datos en remoto o elimine chats de WhatsApp.

3. **Logs del cortafuegos:** El técnico nos avisó de que los logs se sobreescriben cada 7 días y están a punto de sobreescribirse.

4. **Grabaciones de la cámara de seguridad:** Para evitar que se sobreescriban las grabaciones y perdamos la grabación del momento del incidente.

5. **Pendrive de Javier:** Para evitar que Javier use el pendrive y sobreescriba el rastro que dejó Marta.

6. **Almacenamiento:** Disco duro externo conectado al dock y disco duro del portátil de empresa, son datos que no se deberían borrar pero se podrían bloquear por BitLocker.

7. **Cola y logs de impresión de la impresora común:** Hay riesgo de que los compañeros sigan usando la imresora y sobreescriban los logs.

8. **Copias de seguridad del NAS:** Hay que sacar la versión del dia 14 y 15 de marzo.

9. **Cloud:** Es los más persistente y lo menos probable a que se pierda.

## 3. Medidas inmediatas

- Mantener el portátil de empresa encendido y conectado al Dock y aislarlo de la red para evitar borrado de datos en remoto.

- Pedir el móvil de empresa a Marta y aislarlo activando el modo avión.

- Asegurarte de que nadie se acerque al puesto de trabajo y nadie toque el disco duro externo.

- Guardar en un sitio seguro el pendrive de Javier previamente usado por Marta.

- Contactar con Bahía Sistemas para que nos faciliten los logs y sesiónes de la VPN.

- Pedir las grabaciones de la cámara de seguridad del dia 14 entre las 18:30 y las 20:00.

- Prohibir temporalmente el uso de la impresora común.

## 4. Límites

- **El móvil personal de Marta:** Estaríamos violando el derecho a la intimidad y al secreto de las comunicaciones.  
Dejaría constancia de que pueden haber más pruebas en el móvil personal de Marta y nos centraríamos en lo que sí podemos investigar.

- **El equipo de la entrada con la sesión abierta de Outlook:** Estaríamos violando nuevamente el derecho a la intimidad del trabajador el cual se ha dejado la sesión abierta.  
En su lugar haría una foto de la pantalla para que conste que está la sesión abierta y bloquear el equipo sin modificar nada y prohibir el acceso temporalmente al equipo.

- **Las grabaciones de la cámara de seguridad:** La cámara de seguridad no es de la empresa sino que es de la comunidad de la empresa.  
Por lo que tendríamos que hacer una petición formal o judicial de las imágenes.

## 5. De dónde sale cada decisión

| Decisión | Punto de la lista | Norma y apartado de referencia |
|---|---|---|
| Mantener el portátil encendido y conectado al Dock (volcado de RAM) | Punto 6 y 16 | **RFC 3227 §2.1** (Orden de volatilidad) y **§3.1** (Procedimiento de recogida). |
| Aislar de la red el portátil de empresa para evitar borrado remoto | Punto 15 | **RFC 3227 §3.1** (Evitar interferencias o accesos remotos no autorizados). |
| Pedir el móvil de empresa y aislarlo activando el modo avión | Punto 5 y 17 | **ENFSI §8.2** (Gestión de dispositivos móviles en la escena). |
| Guardar en un sitio seguro el pendrive de Javier | Punto 14 y 19 | **ENFSI §9.2** (Evaluación de indicios aportados por testigos) y **RFC 3227 §2.1**. |
| Asegurar que nadie toque el disco duro externo del Dock | Punto 4 y 19 | **ENFSI §8.2** (Inspección de periféricos) y **RFC 3227 §2.1** (Almacenamiento no volátil). |
| Contactar con Bahía Sistemas para solicitar logs y sesiones VPN | Punto 9 y 18 | **NIST SP 800-86 §3.1.1** (Fuentes de red y persistencia limitada de logs). |
| Solicitar grabaciones de la cámara de seguridad a la comunidad | Punto 13 y 20 | **ENFSI §8.2** (Preservación de CCTV gestionado por terceros). |
| Prohibir temporalmente el uso de la impresora común | Punto 12 | **NIST SP 800-86 §3.1.1** (Identificación y preservación de dispositivos compartidos). |
| No intervenir el móvil personal de Marta respetando su intimidad | Punto 1 | **ENFSI §9.1** (Marco legal de actuación y límites de autorización). |
| Fotografiar y bloquear el PC común sin alterar la sesión de Outlook | Punto 3 y 6 | **RFC 3227 §3.1** (Fijación fotográfica) y **ENFSI §8.2** (No alterar evidencias ajenas). |