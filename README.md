Disaster Recovery. FHRP и Keepalived Кондаков Павел  



------


### Задание 1
- Дана [схема](1/hsrp_advanced.pkt) для Cisco Packet Tracer, рассматриваемая в лекции.
- На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
- Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
- Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
- На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

![alt text](https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/z1%20conf%20r1.png)   
![alt text](https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/z1%20conf%20r2.png)   
![alt text](https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/z1%20final.png)  
  
https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/hsrp_advanced_kondakovpv.pkt  

------


### Задание 2
- Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного [файла](1/keepalived-simple.conf).
- Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
- Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
- Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
- На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

  
https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/nginx.sh  
  
https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/keepalived.conf

![alt text](https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/VirtualBox_ubuntu_15_12_2023_18_38_40.png)  

![alt text](https://github.com/PavelKondakov22/Disaster-Recovery.-FHRP-Keepalived/blob/main/VirtualBox_ub_15_12_2023_18_55_05.png)  
