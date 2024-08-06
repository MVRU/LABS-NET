# Unidad 3 – Laboratorio 1: Login

## 1. Creación del Formulario de Login

### Objetivo
Construir un login para una aplicación Win Form.

### Pasos

1. **Crear Proyecto en Visual Studio:**
   - Abrir Visual Studio 2005.
   - Ir a Archivo -> Nuevo -> Proyecto.
   - Seleccionar C# -> Windows -> Windows Application.
   - Completar:
     - **Nombre del Proyecto:** Academia
     - **Ubicación:** C:\Proyectos\Unidades\Unidad03
   - Presionar **Aceptar**.

2. **Configurar Formulario:**
   - Editar propiedades del formulario:
     - **(Name):** formLogin
     - **Text:** Ingreso
   - Renombrar `Form1` a `formLogin` en el Explorador de Soluciones.

3. **Agregar Controles:**
   - Arrastrar desde el Cuadro de Herramientas:
     - 3 Labels
     - 2 TextBox
     - 1 Button
     - 1 LinkLabel
   - **Ubicarlos de la siguiente manera:**
     - **Label1:**
       - **Text:** ¡Bienvenido al Sistema! Por favor digite su información de Ingreso
       - **TextAlign:** MiddleCenter
     - **Label2:**
       - **Text:** Nombre de Usuario:
     - **Label3:**
       - **Text:** Contraseña:
     - **LinkLabel1:**
       - **(Name):** lnkOlvidaPass
       - **Text:** Olvidé mi contraseña
     - **TextBox1:**
       - **(Name):** txtUsuario
     - **TextBox2:**
       - **(Name):** txtPass
     - **Button1:**
       - **(Name):** btnIngresar
       - **Text:** Ingresar

4. **Ajustar Propiedades del Formulario:**
   - Agrandar el formulario y reorganizar los controles para que luzca bien.

### 2. Definir Eventos

### Objetivo
Definir eventos del formulario Login.

### Pasos

1. **Evento Click del Botón Ingresar:**
   - Seleccionar `btnIngresar` y abrir la ventana de propiedades.
   - Hacer clic en el ícono de relámpago para ver eventos.
   - Doble clic en el evento `Click` para generar el manejador de eventos.

2. **Agregar Código al Handler:**
   - Modificar el handler `btnIngresar_Click`:
     ```csharp
     private void btnIngresar_Click(object sender, EventArgs e)
     {
         if (this.txtUsuario.Text == "Admin" && this.txtPass.Text == "admin")
         {
             MessageBox.Show("Usted ha ingresado al sistema correctamente.",
                             "Login", MessageBoxButtons.OK, MessageBoxIcon.Information);
         }
         else
         {
             MessageBox.Show("Usuario y/o contraseña incorrectos",
                             "Login", MessageBoxButtons.OK, MessageBoxIcon.Error);
         }
     }
     ```

3. **Evento LinkClicked del LinkLabel:**
   - Seleccionar `lnkOlvidaPass` y agregar handler para el evento `LinkClicked`:
     ```csharp
     private void lnkOlvidaPass_LinkClicked(object sender, LinkLabelLinkClickedEventArgs e)
     {
         MessageBox.Show("Es Ud. un usuario muy descuidado, haga memoria",
                         "Olvidé mi contraseña", MessageBoxButtons.OK, MessageBoxIcon.Exclamation);
     }
     ```

4. **Probar la Aplicación:**
   - Ejecutar la aplicación y verificar funcionamiento.

5. **Ocultar Contraseña:**
   - Seleccionar `txtPass` y en propiedades, establecer `PasswordChar` a `*`.

## 3. Formulario Modal

### Objetivo
Incluir el formLogin en una aplicación con un formulario MDI y convertirlo en un formulario modal.

### Pasos

1. **Agregar Nuevo Formulario Principal:**
   - En el proyecto `Agenda`, agregar un nuevo formulario llamado `formMain`.

2. **Configurar formMain:**
   - Editar propiedades:
     - **Text:** Academia
     - **WindowState:** Maximized
     - **IsMdiContainer:** True

3. **Agregar MenuStrip:**
   - Agregar un `MenuStrip` y cambiar propiedad `(Name)` a `mnsPrincipal`.
   - Agregar ítems `Archivo` y `Salir`, renombrar a `mnuArchivo` y `mnuSalir`.

4. **Evento Click del Menú Salir:**
   - Agregar handler para el evento `Click` del `mnuSalir`:
     ```csharp
     private void mnuSalir_Click(object sender, EventArgs e)
     {
         this.Dispose();
     }
     ```

5. **Mostrar formLogin como Modal:**
   - En `formMain`, agregar handler para el evento `Shown`:
     ```csharp
     private void formMain_Shown(object sender, EventArgs e)
     {
         formLogin appLogin = new formLogin();
         if (appLogin.ShowDialog() != DialogResult.OK)
         {
             this.Dispose();
         }
     }
     ```

6. **Configurar Método Main:**
   - En la clase `Program`, cambiar el formulario de inicio a `formMain`:
     ```csharp
     static void Main()
     {
         Application.EnableVisualStyles();
         Application.SetCompatibleTextRenderingDefault(false);
         Application.Run(new formMain());
     }
     ```

7. **Probar la Aplicación:**
   - Ejecutar y verificar que el `formLogin` sea modal.

8. **Ajustes en formLogin:**
   - Editar propiedades para evitar redimensionado:
     - **MaximizeBox:** False
     - **MinimizeBox:** False
     - **FormBorderStyle:** FixedSingle
     - **StartPosition:** CenterParent

9. **Configurar AcceptButton:**
   - En `formLogin`, establecer `AcceptButton` a `btnIngresar`.

10. **Cerrar Aplicación si Login Falla:**
    - Asegurarse que el `formMain_Shown` cierra la aplicación si el login falla:
      ```csharp
      private void formMain_Shown(object sender, EventArgs e)
      {
          formLogin appLogin = new formLogin();
          if (appLogin.ShowDialog() != DialogResult.OK)
          {
              this.Dispose();
          }
      }
      ```

11. **Probar Nuevamente:**
    - Ejecutar y verificar todos los ajustes.