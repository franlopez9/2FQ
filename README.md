# 🫓 2FQ — Too Fast & Quick

Sistema ágil para **tomar órdenes en plancha** y llevar el **control financiero diario** de una pupusería desde celular, tablet o computadora.

👉 **Probala aquí:** https://franlopez9.github.io/2FQ/

> 🚧 **Estado: Alpha.** Actualmente la app gestiona pedidos en tiempo real, subcuentas y control de caja/gastos. *No procesa cobros con tarjeta directamente: registra el método con el que pagó el cliente y muestra tu QR bancario.*

---

## ✨ ¿Qué hace hoy?

- **Tablero de Plancha (Activas):** Vista principal con contador en vivo de órdenes en preparación vs. órdenes completadas en el turno.
- **Órdenes por modalidad y cliente:** Soporte para *Comer aquí* (mesas configurables + barra), *Para llevar* y *Delivery*, con registro de cliente desde el inicio.
- **Catálogo completo salvadoreño:** Más de 40 especialidades organizadas por categoría (*Clásicas, Hierbas y Veg., Carnes, Mariscos, Gourmet, Dulces y Bebidas*) con selector independiente de **Maíz** o **Arroz**.
- **Subcuentas por comensal (Unir o separar cuentas):** Permite separar pedidos por amigo dentro de una misma mesa y, al cobrar, liquidar individualmente, unir varios amigos en un solo pago o dividir en partes iguales.
- **Cobros y QR Bancario:** Registro de pagos en *Efectivo, Wompi/POS, Transferencia* (mostrando tu QR y número de cuenta en pantalla) o *Fiado*.
- **Control de Gastos y Arqueo:** Registro por categoría (*quesillo, masa, carnes, verduras, gas, luz/agua, alquiler, desechables, personal*) y cierre de caja por día, semana o mes.
- **Libreta de Clientes y Fiados:** Historial de saldos pendientes con recordatorio directo por WhatsApp.
- **Configuración visual sin tocar código:** Asistente inicial paso a paso y menú de ajustes (`⚙️`) para personalizar nombre, logo, mesas, precios, sencillo inicial y QR bancario.

---

## 🚀 Próximamente

- 📦 **Modo Offline instalable (PWA):** `manifest.json` y *Service Worker* para operar 100% sin internet y bloquear tablets en Modo Kiosco.
- ☁️ **Respaldo en la nube:** Sincronización multi-dispositivo (plancha + caja).
- 💳 **Integración directa con pasarela de pago.**

---

## 📱 Cómo usarla

1. Abrí el enlace desde el navegador de tu tablet, celular o computadora: `https://franlopez9.github.io/2FQ/`
2. En el menú del navegador, elegí **"Agregar a pantalla de inicio"** para usarla a pantalla completa como app.
3. Completá la configuración inicial de tu pupusería en menos de un minuto (menú, mesas y QR).

> ⚠️ **Nota sobre los datos:** Por ahora toda la información se guarda localmente en el navegador de ese dispositivo (`localStorage`). Si borrás los datos de navegación o cambiás de equipo, los registros se reinician.

---

## 🛠️ Personalización avanzada (Opcional)

Todos los precios, mesas, logo y catálogo se configuran directamente desde el botón **⚙️** dentro de la app.  
Si querés modificar el catálogo base por defecto para nuevas instalaciones, editá el arreglo `MENU_INICIAL` dentro de `index.html`:

```javascript
{ id: 'revuelta', cat: 'clasicas', nombre: 'Revuelta', desc: 'Chicharrón, frijol y queso', emoji: '🫓', precioMaiz: 1.00, precioArroz: 1.25, esPupusa: true, activo: true }
