# Jenkins

## Cоздаем бесплатный истанс на амазоне и устанавливаем на нем дженкинс и докер

Дженкинс с помошью скрипта 
```
sudo apt-get update
sudo apt-get install openjdk-17-jdk
sudo apt-get update
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```
Докер с помошью команд

```
#скачивание скрипта установки Docker 

curl -fsSL https://get.docker.com -o get-docker.sh

#установка Docker

sudo sh get-docker.sh

#добавление в группу sudo (jenkins, Docker) 

sudo usermod -aG docker jenkins
sudo usermod -aG sudo jenkins
```

## Создаем докер файл и простое приложение

Докер файл

![image](pictures/dockerfile.png)

Простое приложение

![image](pictures/web.png)
