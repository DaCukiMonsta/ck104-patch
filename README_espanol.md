# Parche de firmware Motospeed CK104
Este es un parche de firmware para los teclados Motospeed CK104 y E-Element Z-88, para corregir un error en el que su software de control dice constantemente "Device is disconnected"/"El dispositivo está desconectado" y se niega a controlar la iluminación RGB del teclado.

# Riesgos - ¡debes leer!
** Existe cierto nivel de riesgo al realizar esta modificación. ** Si bien no implica modificar el hardware, sí implica modificar el firmware del teclado.
  1. No se conoce ninguna forma de realizar una copia de seguridad del firmware original del teclado. Esto significa que si el archivo de firmware no funciona, ** no podrá volver al estado operativo **.
  2. Actualizar el firmware es riesgoso. Desenchufar el teclado durante una actualización, o cualquier otro problema que haga que falle la transferencia del firmware, podría bloquear el teclado.
  3. ** Se sabe que el firmware actualizado reduce ligeramente el brillo máximo de los LED en el teclado. ** Esto se debe probablemente a la forma diferente en que controla los LED. Mi estimación completamente poco científica es que con el firmware actualizado, el brillo máximo es solo alrededor del 80-90% de lo que era originalmente. La mayoría de los usuarios ni siquiera se han dado cuenta de esto, y yo mismo lo dudé hasta que otros me preguntaron, es muy leve. ** No realice la modificación si no está satisfecho con esto. **
  4. El firmware que está colocando en su teclado es el de un modelo diferente, que funcionó. Esto es experimental, nadie ha hecho ningún trabajo para demostrar que es seguro o confiable, solo probamos algo y funcionó. No hay garantía de que el firmware funcione o de que no cause problemas con su teclado ahora o en el futuro. Se proporciona de forma gratuita con la esperanza de que ayude a alguien, por lo que no le debemos nada si sale mal.

Debido a estos riesgos, debe comprender y aceptar los siguientes puntos antes de realizar la modificación. Si el español no es su primer idioma, mire las copias traducidas y asegúrese de entenderlo.
  1. Es posible que esta modificación pueda bloquear permanentemente su teclado. Acepta que está dispuesto a correr este riesgo y tiene un teclado de repuesto para usar si esto rompe el actual. Si bien hasta ahora ha tenido una tasa de éxito del 100% con los usuarios, no se puede garantizar que funcione y que no romperá su teclado para siempre.
  2. Es su teclado, no el de otra persona. Si lo rompe, no hará que nadie se enoje (como un padre).
  3. Acepta que podría hacer que su teclado sea un poco menos brillante (ver arriba).
  4. Usted comprende que este recurso se proporciona completamente por buena voluntad y sin costo, y yo ni ningún contribuyente futuro a este repositorio somos responsables si rompe su teclado.
  5. ** No es posible volver a su firmware original en este momento. Esta modificación es permanente, no se puede deshacer. **

Si comprende y acepta todo esto, no dude en continuar.

# Instrucciones
Antes de seguir las instrucciones a continuación, ** debe ** comprender y aceptar los riesgos anteriores.

  1. Descargue los dos archivos exe, `update_firmware.exe` e` install_software.exe`. El primero se usa para realizar la actualización del firmware (y contiene el archivo del firmware), el segundo se usa para instalar un software de control ligeramente diferente que es compatible con el nuevo firmware.
  2. Este es el punto de **no retorno**. Con su teclado conectado a la computadora, ejecute `update_firmware.exe`. Esto actualizará *inmediatamente* el firmware del teclado, no le preguntará "¿está seguro?" Antes de hacerlo, así que no haga clic en el programa hasta que esté listo. Una vez que tenga éxito, debería decir "PASS". Hasta entonces, no desenchufe el teclado ni apague la computadora.
  3. Las luces del teclado se apagarán por completo y dejarán de responder. No se preocupe, esto es normal. Es porque necesita apagar y encender el teclado para que use el nuevo firmware. Para hacer esto, debe desenchufar el teclado, esperar unos segundos y luego volver a enchufarlo. Algunos usuarios informaron que tuvieron que usar un puerto USB diferente para volver a enchufarlo la primera vez, así que intente esto si aún no lo está iluminando.
  4. Desinstale cualquier software de control que ya esté usando con su teclado. Este es el software que dice "Device is disconnected"/"El dispositivo está desconectado", debe desinstalarlo ahora.
  5. Ejecute `install_software.exe` para instalar el nuevo software de control.
  6. Inicie el nuevo software de control que acaba de instalar, todo debería funcionar ahora.

La imagen del teclado en el nuevo software se verá un poco diferente a su teclado real, pero esto está bien, por favor ignórelo. Si tiene algún problema, puede abrir un problema en GitHub o contactarme en Discord DaCukiMonsta#8002, o Reddit [/u/DaCukiMonsta](https://www.reddit.com/u/DaCukiMonsta) y yo podría para intentar ayudarte. Por favor, recuerde que yo mismo no hablo español. Sin embargo, sé que mucha gente que usa este recurso no habla inglés. Entonces, si me hablas en tu idioma, intentaré traducir y hablarte en español, pero mi español no será perfecto. :)

# Control adicional
He estado escribiendo una biblioteca de Python para este firmware para permitirle controlar las luces RGB en el teclado de la forma que desee a través del código. Actualmente se encuentra en una etapa de prototipo y no funciona del todo, por lo que no lo he subido a ningún lado. Si quieres tener un lío con esto, avísame y puedo compartir mi código contigo, tal vez puedas ayudar a completarlo.

# Fuentes
El método original proviene de [esta publicación](https://www.reddit.com/r/MechanicalKeyboards/comments/7sghkk/eelement_z88_104_keys_lighting_and_macro_editor/) por el usuario de Reddit [/u/SharXeniX](https://www.reddit.com/u/SharXeniX). Esto se describe usando el firmware X2000 en un teclado E-Element Z-88. Sin embargo, dado que el Motospeed CK104 es un clon de este teclado (o tal vez al revés? Al menos, son iguales por dentro), pensé que también funcionaría para el CK104. Lo probé y acerté.

Los archivos ejecutables provienen originalmente de [esta página de la tienda] (https://www.lelong.com.my/e-element-x2000-z88-upgrade-version-rgb-waterproof-dustproof-104-tdcgaming-I5597538-2007- 01-Sale-I.htm), que ahora está muerto.

# Escaneo de VirusTotal
Mi antivirus informa que ambos archivos están limpios, pero estos son los resultados de un análisis de VirusTotal:
  - [install_software.exe (0/64)] (https://www.virustotal.com/gui/file/23e3498e4bc4a050305b68feb8b897964aa1bb8ce7b845bb3536c3ef58c05be1/detection) (nombre original "2- E-Element_K870_Driver_Setup_V1.0.5.exe")
  - [update_firmware.exe (1/71, probablemente falso positivo de la herramienta antivirus AI)] (https://www.virustotal.com/gui/file/b52ce5606fc2b002e227c329c5ac87aef85eb4587e061b97559f9a29c539d9d6/detection) (nombre original en chino "在线更新工具.exe", para "herramienta de actualización en línea", aunque no creo que se conecte a Internet)
