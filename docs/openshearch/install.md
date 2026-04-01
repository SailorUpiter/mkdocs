# Установка Opensearch
Ссылка на офф доку https://docs.opensearch.org/latest/install-and-configure/install-opensearch/tar/
Установка опенсерча производится из архива. 
Стендэлон
Подготавливаем ноду для установки. Все это дело работает на джаве. И хоть в архиве опенсерча уже есть жаба лучше поставить ее прямо на машину, что бы было проще работать
```
sudo apt update && sudo apt upgrade -y
sudo apt install openjdk-25-jdk
```
Отключим свап и настроем виртуальную память хоста
```
sudo vim /etc/sysctl.conf

vm.max_map_count=262144

sudo sysctl -p
cat /proc/sys/vm/max_map_count
```
После обновления и установки жабы, лучше всего перезагрузится. Далее мы качаем архив с опенсерчем с оффсайта 
```
wget https://artifacts.opensearch.org/releases/bundle/opensearch/3.5.0/opensearch-3.5.0-linux-x64.tar.gz
```
```
Распакуем архив
```