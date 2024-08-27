# jenkins-practice

Hola, este repositorio solo está diseñado para documentar como he usado jenkins en la practica
sencilla de microservicios que hice. Esto porque hasta ahora no se si en jenkins se pueden usar exportables.

# AVANCES 26/07/2024

Hasta ahora ya configuré la instancia con docker, no fue complicado, hablando de que uso desktop para estas cosas jijijijjiji
![image](https://github.com/user-attachments/assets/83825131-c36a-45b8-9998-0799c5472c46)

Está interesante la herramienta, veo que para el sonarqube, el tema está en que puedes configurarlo desde el mismo jenkins como plugin,
entonces tu como dev puedes activarte una instancia para testear local y despues por pipeline. Para catar la herramienta me llevo ratito, lo justo:
![image](https://github.com/user-attachments/assets/60f66089-9dd1-413e-89ee-eb1407d76f2b)

Lo quie se ejecuto fue unos ejemplos que te da el propio jenkins, ahi aprendi que todavia hay que configurar las claves del
git con ssh en credentials
![image](https://github.com/user-attachments/assets/925037a8-11ec-4c19-8b4a-0e6aac79db0d)
![image](https://github.com/user-attachments/assets/793bdc3e-2a30-48da-a231-85b8cdf060fa)

![image](https://github.com/user-attachments/assets/d0f8c4a3-8f1e-4bb8-a72c-812f1bda31fe)

instalar el plugin de docker pa los comandos:
![image](https://github.com/user-attachments/assets/1bfb955d-2218-4919-aab4-8b7f39aeb334)


La gracia aqui creo sera que debo anexar los test cases dentro del proyecto para que el pipeline los acondicione
con los comandos.
