Este modulo implementa un mencanismo para restablecer la contraseña de
una cuenta Jabber/XMPP empleando el correo electrónico y un navegador web.

Para ello, el usuario previamente debe haber introducido en su vCard
la dirección de correo electronico. El proceso de restablecemiento es el siguiente:

- El usuario acceder a la URL del modulo, introduce su Jid y su email.
- Se validan los datos en busca de errores
- Se envía un email al usuario que contiene una URL con un 'token'.
  Ese token tiene una vida útil de 24 horas, es decir, el usuario no puede
 volver a solicitar otro hasta pasadas 24 horas.
- El usuario hace click en el enlace recibido
- El usuario introduce su nueva clave.

Configuración del módulo:

Hay ciertos parámetros que hay que configurar, estos son relativos al
envío de correos (SMTP). Estos parámetros se deben añadir al fichero
prosody.cfg.lua

Parámetros:

smtp_server:	[String]  El servidor SMTP que se quiere utiliza
smtp_port:	[String]  El puerto de conexión al SMTP
smtp_ssl:	[Boolean] Usar SSL? (No STARTTLS)
smtp_user:	[String]  Usuario para la autentificación SMTP (SMTP_AUTH)
smtp_pass:	[String]  Contraseña de la auth SMTP (SMTP_AUTH)
smtp_address:	[String]  Direccion de origen de los mensajes


