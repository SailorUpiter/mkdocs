#note #network #sfp
У нас все оборудование цисковсвкое. Кароточки тоже хуй пойми какие.
Посчитаем сколько всего надо:
6 серверов RJ45 (2 порта) 24 
2 сервера SFP+ (2 порта) 8
1 СХД SFP+ (4 порта) 8 
Подключение идет с 2-х сторон
Итого:
24 RJ4   Пример ASF-10G-T 10Gteck
16 SFP+  

Пересчет
6 серверов RJ45 по 2 порта = 12 штук
5 серверов SFP+ по 2 порта =20 штук
1 схд 4 портов rj45 = 4 штуки (4 было в комплекте они уже есть) 
Запас? 4 RJ45 
Итого 
16 RJ45
24 SFP+


Чисто теоретически заведутся все СФП. Практически а хуй его знает.

Точно рабочие
ASF-10G-T 10Gteck

Lenovo AFBR-709SMZ-ib8
ARISTA XVR-00001-02
Huawei LTF8501-BC+ 02310MNW
Текст письма

Здравствуйте. Для организации высокоскоростного подключения к хранилищу базы данных системы мониторинга PDU требуется SFP модули.  Для обеспечения отказоустойчивости и совместимости серверов требуется закупить:
24 модуля SFP ASF-10G-T 10Gteck или аналогичные
16 модулей SFP Lenovo AFBR-709SMZ-ib8, ARISTA XVR-00001-02, Huawei LTF8501-BC+ 02310MNW или аналогичных



Отчет о своместимости SFP
HPE 10GB SR SFP+ 455885-001  
SN 7CR909N16K
Ядро сети Работает
HP NIC Работает
Eonstore DS1012 Работает

Lenovo AFBR-709SMZ-ib8  
pn\sn 46c3448   Y050UC0C6FD0
 (Хпшеная в ленову работает)
Ядро сети (Работает)  
from core    to  HP DL360G9 SFP+ card  Работает
Eonstore DS1012 Работает
HP NIC (работает)

ARISTA XVR-00001-02
Sn XAP1114T3654
Ленова в аристу работает  
Ариста в Хп работает
Ядро сети (Работает)
HP NIC (работает)
Eonstore DS1012 Работает

Huawei LTF8501-BC+ 02310MNW
Sn J265A000290
Ядро сети (Работает)
Хуавей в аристу работает
Хуавей в ленову +  
Хуавей в ХП +
HP NIC (работает)
Eonstore DS1012 Работает

Оптические трансиверы  
СХД 8 Шт
Сервера HP 8 Шт
Сервера оракл 12 Шт
Rj45 трансиверы 16 ШТ


Карточки куда идет
деллы BCM57416 NetXtreme-E Dual-Media 10G RDMA Ethernet Controller (rev 01)
ХП rj54 Intel Corporation Ethernet Controller 10-Gigabit X540-AT2 (rev 01)
SFP+ карточки HP NC550SFP Dual Port 10Gbe Server adapter
Лезвие ядра сети Cisco C6800-32P10G