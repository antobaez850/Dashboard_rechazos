# 📊 Dashboard Rechazos

### 📌 Objetivo general del proyecto

El presente tablero tiene como finalidad centralizar y estandarizar el monitoreo de las transacciones aprobadas y rechazadas, permitiendo al equipo de Payment y Operaciones disponer de información actualizada, estructurada y accionable para la detección temprana de problemas, la evaluación de la performance de cobro por comercio y la reducción del impacto operativo y económico generado por los rechazos.


<b>Principales indicadores a mejorar:</b>

• Aumento del % de Aprobación.

• Reducir el costo de rechazo.


<b>Objetivos específicos:</b>

• Medir y monitorear el porcentaje de aprobación de débitos automáticos por comercio, rubro, canal y banco emisor en forma mensual.

• Identificar y clasificar los motivos de rechazo más frecuentes (falta de fondos, cuenta bloqueada, cuenta inexistente, límite excedido, entre otros) para orientar acciones correctivas.

• Cuantificar el impacto económico de los rechazos a través del costo operativo asociado, por comercio y por período.

• Evaluar la efectividad de los reintentos de cobro, determinando si los intentos posteriores al primero mejoran la tasa de aprobación.

• Detectar patrones sistémicos vinculados a bancos emisores específicos, canales de cobro o tipos de cuenta que presenten tasas de rechazo anómalas.
<hr/>

### ⚙️ Detalle de la implementación

<table>
  <tr>
    <th>Nombre</th>
    <th>Detalle</th>
  </tr>
  <tr>
    <td>Fuente Principal</td>
    <td>Base en Excel, periodo contemplado desde Enero 2025-Mayo 2025</td>
  </tr>
  <tr>
    <td>Dashboard en Tableau</td>
    <td>(https://public.tableau.com/app/profile/antonella.baez/viz/Dashboard_rechazos/Portada)</td>
  </tr>
  <tr>
    <td>Indicadores</td>
    <td>Cantidad: Transacciones totales, Aprobadas, Rechazadas.
      
Monto: Total transaccionado, Costo Rechazo.

Calculados:
- %Aprobación:  transacciones aprobadas / transacciones totales.
- %Rechazos:  rechazos / transacciones totales
- Costo prom. Rechazo: Costo de rechazo / cantidad de rechazos</td>
  </tr>
    <tr>
    <td>Dimensiones</td>
    <td>	
Año-Mes, Comercio, Rubro, Motivo Rechazo, Canal, Banco Emisor, Tipo Cuenta.</td>
  </tr>
  <tr>
</table>
<hr/>

### 🧠 Iniciativas

Luego de analizar la información del tablero llegamos a la conclusión que en los últimos dos meses se incrementaron la cantidad de rechazos y por consecuencia aumento el costo por rechazo. 

<b>El mayor % de rechazos proviene de Débitos directo y el motivo Falta de fondos.</b>

En base a este resultado se plantean 3 iniciativas:

• En los casos que el usuario tenga tarjeta de crédito, sugerir o darles un beneficio para que migren la suscripción a Tarjeta de Crédito.

• Estimación próxima fecha de cobro, para enviar una notificación y que el usuario deposite plata en la cuenta.(Para esto se hizo todo un análisis y query para entender como era el comportamiento de estimación de cobro)

• Detectar si era un usuario inactivo o que la tarjeta estaba vencida para cortar el token y que deje de intentar.

### ✅ Impacto

La iniciativa con mas impacto fue la de estimación ya que enviábamos una notificación al usuario 3 días antes que el proximo cobro para que puedan depositar plata.

💪 Resultado logrado: Aumentar un %30 la tasa de aprobación, antes era del 40% y paso a % 70 y reducir costo de rechazo.



