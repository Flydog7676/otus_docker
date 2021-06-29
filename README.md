# otus_docker
У меня рабочая машина на Ubuntu. Для создание стенда для работы с Docker необходимо сначала
1. Установить VirtualBox,Расширение Virtualbox Extension Pack и Vagrant
- Установка Virtualbox   ``` sudo apt install virtualbox ```
- Скачать плагин расширения ``` wget https://download.virtualbox.org/virtualbox/6.1.22/Oracle_VM_VirtualBox_Extension_Pack-6.1.22.vbox-extpack```
- установить плагин  ``` Файл - Настройки - Плагины ```, выбираем файл плагина и устанавливаем
- Скачиваем vagrant ``` wget https://releases.hashicorp.com/vagrant/2.2.16/vagrant_2.2.16_x86_64.deb ```
- Устанавливаем vagrant ``` sudo apt install ./vagrant_2.2.16_x86_64.deb ```
- Проверяем работу и версию установленного vagranta  ``` vagrant --version ```
2. Запуск через vagrant виртуальную машину c СentOs 8 и устанавливаем Docker
- Создаем папку CentOs_Docker   ``` mkdir CentOs_Docker ```
- Копируем туда файлы из  ``` https://github.com/nixuser/virtlab/tree/main/docker_demo/centos ```
- Заходим в созданную папку и запускаем ``` vagrant up ```
- Подключаемся к нашей виртуалке 
```
vagrant up
sudo su
```
- папка /vagrant - это общая папка с хостовой машиной
- переходим в /vagrant и запускаем файл ``` ./setup_docker.sh```
- Заходим на сайт ``` https://hub.docker.com/_/nginx ``` по инструкции закачиваем images ``` docker pull nginx ```
- Запускаем контейнер и монтируем папку с нужными файлами 
``` docker run --rm -d -p 8080:80 --name web -v /vagrant:/etc/nginx/conf.d/ nginx ```
- Заходим внутрь контейнера и проверяем файлы
```
docker exec -it web /bin/bash
ls /etc/nginx/conf.d
```
