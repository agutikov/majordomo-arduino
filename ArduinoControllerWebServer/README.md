 Контроллер-исполнительное устройство (к проекту http://smartliving.ru/)
 Platform: Arduino UNO R3 + EthernetShield W5100
 IDE: Arduino 1.0.1

 исполнительные устройства (реле) подключены к Digital 3 - 9

 обращение по http://xx.xx.xx.xx/ выдаст справочную информацию по этому устройству (нужно для того, чтобы когда обращаешься
 по IP к устройству понять что это за контроллер и пр.)

 /state - состояние всех портов
 /command - выполнение команды
         команды можно вызывать серией в 1 запросе. Например http://xx.xx.xx.xx/command?3=CLICK&4=CLICK&5=ON&6=OFF
         только длинна строки запроса не должна привышать maxLength
 /getdev - получить список всех устройст на 1-wire
         формат вывода: 
                T<номер устройства на шине>:<HEX адрес устройства>:<текущая температура в градусах цельсия>;[...]
                (пример T0:1060CF59010800E3:24.06;T1:109ABE59010800FE:24.56;)


Скачать зависимости:
$ git clone https://github.com/sirleech/Webduino.git
$ git clone https://github.com/ppicazo/OneWire
$ git clone https://github.com/mysensors/Arduino.git
                
Добавить библиотеки:               
Arduino IDE меню -> Sketch -> Import Library -> Add Library 
добавить все три библиотеки: OneWire, Webduino и Arduino/libraries/DallasTemperature


