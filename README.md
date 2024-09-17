### Sistema de Pedidos de Farmacia - README
## Descripción del Proyecto
Este proyecto es una interfaz gráfica de usuario (GUI) en Java para gestionar el sistema de pedidos de una farmacia. La aplicación permite a los usuarios ingresar datos sobre los medicamentos, elegir un distribuidor, seleccionar la sucursal de entrega y confirmar o cancelar los pedidos. Utiliza Swing para la creación de la interfaz de usuario y está estructurado para facilitar la interacción con diferentes componentes de la farmacia, como tipos de medicamentos, distribuidores y sucursales.

# Funcionalidades
Ingreso de Datos del Medicamento:
El usuario puede ingresar el nombre del medicamento y la cantidad deseada.
El tipo de medicamento se selecciona desde un menú desplegable con categorías como Analgésico, Antibiótico, etc.

# Selección del Distribuidor:

Tres distribuidores principales están disponibles: Cofarma, Empsephar y Cemefar.
Se usa un grupo de botones de radio para asegurarse de que el usuario elija solo uno.

# Selección de la Sucursal:

El usuario puede elegir una o ambas sucursales donde se entregará el pedido, marcando las opciones Principal y/o Secundaria.

# Validación de Datos:

Se valida que todos los campos obligatorios sean completados correctamente antes de permitir que el pedido sea confirmado.
Se validan específicamente:
- Nombre del medicamento (no vacío, solo caracteres alfanuméricos).
- Cantidad (solo números y debe ser mayor que 0).
- Distribuidor seleccionado.
- Al menos una sucursal seleccionada.

# Resumen del Pedido:

Al confirmar, se muestra una ventana resumen que detalla el pedido, incluyendo:
- Nombre, tipo y cantidad del medicamento.
- Distribuidor seleccionado.
- Sucursal de entrega.
- El usuario puede enviar o cancelar el pedido desde esta ventana.

# Botones de Acción:

- Confirmar: Valida los datos ingresados y muestra el resumen del pedido.
- Borrar: Limpia todos los campos del formulario para comenzar un nuevo pedido.

# Estructura del Código
El código está dividido en dos clases principales:

1. PedidoFarmaciaGUI
Esta clase es la que contiene toda la interfaz gráfica y los elementos interactivos. Sus principales componentes son:

- Componentes de la GUI: Se definen etiquetas (JLabel), campos de texto (JTextField), botones (JButton), cajas de verificación (JCheckBox) y botones de radio (JRadioButton), organizados en paneles (JPanel).
- Métodos de Acción: Se manejan las acciones del usuario como:
. btnConfirmarActionPerformed(): Valida los datos ingresados y genera un resumen del pedido.
. btnBorrarActionPerformed(): Limpia todos los campos del formulario.
. mostrarResumen(): Muestra una ventana con los detalles del pedido y permite enviar o cancelar.
. borrarFormulario(): Restablece los campos del formulario a su estado inicial.
  
- Validaciones: Se implementan las validaciones para asegurar la coherencia de los datos ingresados antes de permitir confirmar el pedido.

2. SistemaPedidosFarmacia
Esta clase contiene el método principal (main) que inicia la aplicación creando una instancia de PedidoFarmaciaGUI y la hace visible en la pantalla.

# Componentes Utilizados
- JFrame: Para la ventana principal y el resumen del pedido.
- JLabel: Para las etiquetas descriptivas de cada campo.
- JTextField: Para el ingreso del nombre y la cantidad del medicamento.
- JComboBox: Para la selección del tipo de medicamento.
- JRadioButton: Para elegir el distribuidor, agrupados con ButtonGroup para asegurarse de que solo uno esté seleccionado.
- JCheckBox: Para la selección de las sucursales de entrega.
- JButton: Para las acciones de confirmar, borrar, enviar o cancelar el pedido.
- JOptionPane: Para mostrar mensajes de validación y errores.

# Instalación y Uso
- Requisitos Previos
. JDK (Java Development Kit): Asegúrate de tener instalado Java SE Development Kit 8 o superior.
. NetBeans o IDE Compatible: Es recomendable utilizar NetBeans u otro IDE como Eclipse para compilar y ejecutar el código, ya que facilita la manipulación del entorno gráfico (Swing).

- Pasos para Ejecutar
  1. Clona o descarga el repositorio.
  2. Copila el proyecto en tu IDE (NetBeans o Eclipse).
  3. Ejecuta la clase SistemaPedidosFarmacia para iniciar la aplicación.

- Interacción con la Aplicación
  1. Llenar el formulario:

. Ingresar el nombre y la cantidad del medicamento.
. Seleccionar el tipo de medicamento y el distribuidor.
. Elegir una o ambas sucursales para la entrega.

  2. Confirmar o borrar:
- Al hacer clic en Confirmar, se validarán los datos y, si todo es correcto, se mostrará un resumen del pedido.
- En el resumen, el pedido puede ser enviado o cancelado.
  
  3. Nuevo pedido:
- Se puede comenzar un nuevo pedido haciendo clic en el botón Borrar para restablecer el formulario.

# Mejoras Futuras
1. Integración con Bases de Datos: Incorporar una base de datos para guardar los pedidos realizados.
2. Manejo de usuarios: Implementar un sistema de autenticación para empleados o administradores.
3. Optimización de la interfaz: Mejorar la disposición de los componentes utilizando un GridLayout o GroupLayout para una mejor experiencia de usuario.
4. Funcionalidad de exportación: Permitir la exportación de los pedidos en formato PDF o CSV.
5 Envío de notificaciones: Integrar un sistema de notificación para avisar cuando los pedidos sean confirmados o rechazados.
