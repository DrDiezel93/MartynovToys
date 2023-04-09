Домашняя работа по Linux. Мартынов Е.А.

Создание директории
mkdir ‘Игрушки для школьников’
mkdir ‘Игрушки для дошколят’


Создание файла
cd 'Игрушки для школьников'
touch Настольные\ игры.txt
touch Роботы.txt
touch Конструктор.txt
cd
cd 'Игрушки для дошколят'
touch Мягкие\ игрушки.txt
touch Куклы.txt
touch Машинки.txt

Объединение директорий
cd 'Игрушки для дошколят'/
mv * /home/drdiezel/'Имя игрушки'/
rmdir 'Игрушки для дошколят'
cd 'Игрушки для школьников'/
mv * /home/drdiezel/'Имя игрушки'/
rmdir 'Игрушки для школьников'

Переименование директории
mv 'Имя игрушки' Игрушки

Смотрим содержимое
cd Игрушки/
ll
cd

Установить и удалить snap-пакет.

Установка
snap install gimp

Удаление
snap remove gimp
Создание задачи каждые 3 минуты
sudo vi /usr/local/bin/script.sh
    #!/bin/bash
    echo $(date) >> /var/log/testcron.log
    :w!
    :q
sudo chmod ugo+x /usr/local/bin/script.sh
sudo crontab -e
    0/3 * * * * /usr/local/bin/script.sh
crontab: installing new crontab
