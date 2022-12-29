# O365
  
Conectar con Outlook mediante O365.  

*Read this in other languages: [English](README.md), [Portugues](README_pr.md), [Español](README_es.md).*

## Como instalar este módulo
  
__Descarga__ e __instala__ el contenido en la carpeta 'modules' en la ruta de Rocketbot.  

## Como usar este modulo

Antes de usar este modulo, es necesario registrar tu aplicación en el portal de Azure App Registrations. 

1. Inicie sesión en Azure Portal y busque el servicio Azure Active Directory.
2. Alli, en el menu en el lateral izquierdo, ingrese a "Registración de Aplicaiones".
3. Seleccione "Nuevo registro".
4. En “Tipos de cuenta compatibles” soportados elija:
    a. "Cuentas en cualquier directorio organizativo (cualquier directorio de Azure AD: multiinquilino) y cuentas de Microsoft personales (como Skype o Xbox)" para este caso utilizar  ID Inquilino = common
    b. "Solo cuentas de este directorio organizativo (solo esta cuenta: inquilino único) para este caso utilizar ID Inquilino especifica de la aplicación.
5. Establezca la uri de redirección (Web) como: https://login.microsoftonline.com/common/oauth2/nativeclient y haga click en "Registrar".
6. Copie el ID de la aplicación (cliente). Necesitará este valor.
7. Dentro de "Certificados y secretos", genere un nuevo secreto de cliente. Establezca la caducidad (preferiblemente 24 meses). Copie el VALOR del secreto de cliente creado (NO el ID de Secreto). El mismo se ocultará al cabo de unos minutos.
8. Dentro de "Permisos de API", haga click en "Agregar un permiso", seleccione "Microsoft Graph", luego "Permisos delegados", busque y seleccione "Mail.ReadWrite" y "User.Read", y por ultimo "Agregar permisos".
9. En Rocketbot Studio, insertar el comando "Conectar a O365", ingresar los datos solicitados (ID de cliente, valor del secreto y tenant) y ejecutar el comando.
10. En la consola de Rocketbot se generara una url (Ejemplo: https://login.microsoftonline.com/common/oauth2/v2.0/authorize?response_type=code&client_id=82f8efcd-6a0d-4532-a62e-3e2aecb4d19f&redirect_uri=https%3A%2F%2Flogin.microsoftonline.com%2Fcommon%2Foauth2%2Fnativeclient&scope=Mail.ReadWrite+User.Read.All&state=3LvNFBfX0qej9Q0rsixmSWjCGJyi0M&access_type=offline ), copiarla y pegarla en su navegador.
11. Aceptar el otorgamiento de permisos y devolvera una pantalla sin contenido. Copiar la URL (Ejemplo: https://login.microsoftonline.com/common/oauth2/nativeclient?code=M.R3_SN1.5dcda10b-6567-ce05-3a5b-f67145c62684&state=3LvNFBfX0qej9Q0rsixmSWjCGJyi0M) y pegarla en la consola de Rocketbot debajo de "Paste the authenticated url here:".
12. Presionar "enter" y si la operación fue exitosa vera en la consola: "Authentication Flow Completed. Oauth Access Token Stored. You can now use the API." y se habra creado un archivo con sus credenciales, en la carpeta raiz de Rocketbot, llamado o365_token.txt o o365_token_{session}.txt.


## Overview


1. Conectar a O365  
Conectar a una insancia de la aplicación de O365

2. Listar todos los emails  
Listar todos los emails, se puede especificar un filtro

3. Listar emails no leidos  
Listar todos los emails no leidos de tu casilla de correo

4. Leer email por ID  
Leer un email utilizando su ID

5. Enviar Email  
Envia un email

6. Responder Email  
Responder un email utilizando su ID

7. Reenviar Email  
Reenviar un email utilizando su ID

8. Descargar adjuntos  
Descarga los archivos adjuntos de un correo

9. Marcar como no leido  
Marcar un email como no leido

10. Listar carpetas del correo  
Lista todas las carpetas del correo

11. Mover email  
Mover un email de una carpeta a otra

12. Crear carpeta  
Crea una nueva carpeta en el correo electrónico.

13. Obtener grupos  
Obtener lista de Grupos a los que pertenece la cuenta

14. Obtener grupo  
Obtener Grupo por su ID

15. Obtener sitio  
Obtener el sitio del Grupo

16. Obtener listas  
Obtener las listas del Sitio

17. Crear Lista  
Crear una nueva lista

18. Obtener items de lista  
Obtener los items de una Lista utilizando su nombre

19. Obtener Item  
Obtener un Item, utilizando su ID, de una Lista

20. Crear Item  
Crear un Item dentro de una Lista

21. Borrar Item  
Borrar un Item, usando su ID, de una Lista

22. Actalizar Item  
Actualizar datos de un Item usando si ID  




----
### OS

- windows
- mac
- linux
- docker

### Dependencies
- [**bs4**](https://pypi.org/project/bs4/)
- [**O365**](https://pypi.org/project/O365/)
### License
  
![MIT](https://camo.githubusercontent.com/107590fac8cbd65071396bb4d04040f76cde5bde/687474703a2f2f696d672e736869656c64732e696f2f3a6c6963656e73652d6d69742d626c75652e7376673f7374796c653d666c61742d737175617265)  
[MIT](http://opensource.org/licenses/mit-license.ph)