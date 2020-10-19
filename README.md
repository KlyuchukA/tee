1. Создать виртуальную машину
2. Подключиться к ней по ssh klyuchuk@84.201.136.49
3. sudo apt install docker.io - устанавливает докер
4. sudo dockerd - запустить докер демона и оставляешь его работающим
5. Во втором окне дополнительно логинишься по ssh klyuchuk@84.201.136.49
6. sudo docker pull caddy - скачать доккер
7. Посмотреть все images командой: sudo docker images
8. sudo docker run -d -P --name static-site caddy  - запускаеь сервис caddy
9. sudo docker port static-site - тут типо прописывает? какие у тебя порты открыты
10. и вот так я на зашла туда http://84.201.161.239:32770
11. Проверим что контейнер запущен командой sudo docker ps
12. Создадим папку командой sudo mkdir /usr/share/caddy
13. Снавигируемся в эту папку sudo cd /usr/share/caddy
14. Создадим в ней файлик sudo touch index.html
15. Раздадим права на редактирование файлика sudo chmod 777 index.html
16. Внесем  в файлик данные для отображения на странице
17. Зайгрузили картинку в репозиторий github
18. Командой sudo wget https://github.com/KlyuchukA/tee/blob/master/dockercat.jpg подтянули картинку в linux
19. нАДО СОЗДАТЬ VOLUME
20. sudo docker run -d --name=test -p 80:80 newcat13:latest -
21. Создать новый имидж командой: sudo docker build -t newcat13 .
22. Запустить новый контейнер с созданным имиджем sudo docker run -d --name=test3 -p 80:80 myapp2:latest


docker run -d --name=caddy_test13 -p 80:80 -v $PWD:/usr/share/caddy caddy:latest
sudo docker port caddy_test


vim index.html

 http://84.201.161.239:327700
 http://80.0.0.0.0:32770
 http://84.201.136.49:32770
 
 
84.201.136.49

 
 git config --global user.name "KlyuchukA"
 git config --global user.email nusika_93@mail.ru
 
  wget https://github.com/torvalds/linux/archive/v4.11-rc6.tar.gz
 wget https://github.com/KlyuchukA/tee/dockercat.jpg
 
 http://84.201.161.239:80
 
 http://84.201.136.49
 
 sudo wget https://github.com/KlyuchukA/tee/blob/master/dockercat2.png
 
 
 sudo cp -rp /usr/share/caddy/* /to/cmp/caddy
 
 с монтированием:
 docker run -d --name=caddy_test -p 80:80 -v $PWD:/usr/share/caddy caddy:latest
 
 sudo docker run -d --name=test2 -p 80:80 -v $PWD:/usr/share/caddy myapp2:latest
 
