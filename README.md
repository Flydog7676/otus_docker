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
- 
