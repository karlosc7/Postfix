# Postfix
Servicio de correo y además webmail con Horde

# Comandos
 postqueue
Este es un comando importante ya que permite administrar la cola de mensajes, o los mensajes pospuestos por el servidor.

 postqueue -f Intenta enviar todos los mensajes que están en la cola de espera o como mensaje pospuesto o postergado.

 postqueue -p Permite mostrar todos los mensajes que están en la cola de correo.

 postfix flush Tiene la misma función de enviar todos los mensajes.

 postqueue -s nombredeldominio Intenta enviar todos los mensajes que salgan del nombrededominio especificado.

 postsuper -d ALL Eliminará todos los mensajes que estén en la cola de mensajes.

 postsuper -d ALL deferred Eliminará todos los mensajes que hayan sido rebotados por el destinatario.

 postqueue -p | tail -n 1 | cut -d’ ‘ -f5� Muestra numéricamente cuantos mensajes hay en la cola de correo.

 postcat -q ID Si tenemos el ID del mensaje, con este comando lo podemos visualizar fácilmente.

 postfix start|stop|abort� Inicia, detiene o detiene abruptamente el servicio de Postfix.

 postfix reload Recarga todos los archivos de configuración de Postfix.

 postfix status Indica el estado actual del servicio Postfix en el sistema.

 mailq| grep ‘^[A-Z0-9]’|grep @dominio.com|cut -f1 -d’ ‘ |tr -d \*|postsuper -d – Borra todos los correos enviados por el dominio.com de la cola de mensajes.

 qshape Permite ver todos los correos en una estructura de árbol.
