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


# AVANCES 28/08/2024

No pude subir avance ayer debido a que me desesperé porque al hacer mvn clean install no conseguia poder arrancar
el mendigo MYSQL en el jenkins, pensé por mi novatez que docker enlazaria mysql anfitrion a los contenedores pero no,
busqué y busqué pero no encontraba documentación clara de como funcionaba el plugin de mysql database
para jenkins, debido a eso descubri que en docker se puede acceder al root e instalar maria db como mysql.

![image](https://github.com/user-attachments/assets/c1a5e14f-372b-41cd-ba81-129c43fb5293)

Solo de esa manera... wala, jenkins con mysql:
![image](https://github.com/user-attachments/assets/d0874a38-c68e-4ca5-8db1-b9fb979d575e)
![image](https://github.com/user-attachments/assets/6d811ce5-fa03-4394-a6e8-a0b3335ef485)
![image](https://github.com/user-attachments/assets/5bf9b29d-2e41-4a0c-ae0a-9516e44d8984)


Creo ahora podré continuar con los testings con JUNIT y MOCKITO.

Ah también se tenia que crear la base de datos en la instancia, se me olvido also configurar la contraseña de la instancia local mysql.
Significa que, en entornos de prueba se puede configurar un dump file que se autocargue de un repositorio de git, crear una bdd
para pruebas o tener un docker separado linkeado para evitar una exportación continua y en base a eso crear el ambiente para
los microservicios:

![image](https://github.com/user-attachments/assets/2586cd1f-fd9e-4d62-8db1-ce0c9c0ca3e4)

Al final va a jalar:
![image](https://github.com/user-attachments/assets/55838d62-e135-4903-8ec2-ab1ad63569e3)

![image](https://github.com/user-attachments/assets/26456bc6-a115-46e8-a184-6ef5f119b074)

Ahora si, podré concluir con JUNIT, mockito y alguna otra cuestion de java que se me haya pasado
