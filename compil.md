1.1. для выполнения компиляции ядра ставим зависимости /n
sudo yum install -y wget ncurses-devel make gcc bc bison flex elfutils-libelf-devel openssl-devel grub2 /n
(..кажется, чего не хватает, поставим sudo yum groupinstall "Development Tools")
1.2. скачиваем исходники (kernel.org)
wget https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.18.15.tar.xz
1.3. извлекаем ядро из архива tar -xvf linux-4.18.15.tar.xz
1.4. настраиваем ядро (выбираем опции, модули) sudo make menuconfig
по завершении опциональных настроек сохраняем  результат, в итоге появляется .config, в котором описаны описаны 
настройки скомпилированного ядра
1.5. после завершения конфигурации запускаем компиляцию sudo make
1.6. по завершении компиляции в /var/log/yum.log отображается перечень установленных пакетов
/n
