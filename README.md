# Шаги для разворачивания Node.js приложения с Docker

1. node init
2. файл index.js (для node http)
   или установить express
```
npm i express
node index.js
```

3. Dockerfile
4. .dockerignore для исключения node_modules
5. Сборка докер файла 
```
sudo docker build -t simplenodeapp .
```
-t simplenodeapp - задаёт имя для image
6. запуск докера
```
sudo docker run -d simplenodeapp 
```
7. Описываем docker-compose
```
sudo docker compose up -d
```
8. Подключаемся к серверу
```
ssh root@<ip>
```
9. Установить на сервер [docker](https://docs.docker.com/engine/install/ubuntu) и git
```
apt install git

установка докера по ссылке:
от install apt repository 
до параграфа install from a package
```
10. Загрузить проект в gitHub/gitLab
11. Склонировать проект на сервер
```
git clone <project-url>
```
12. Перейти в папку с проектом
```
cd nodejs-app/
```
13. Поднять докер
```
sudo docker compose up -d
```