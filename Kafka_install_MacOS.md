## Установка и настройка Kafka на MacOS

Заходим на официальный сайт [Apache Kafka](http://kafka.apache.org/downloads) и скачиваем tgz-файл.

Создаем новую папку, переносим туда файл и распаковываем архив:

```console
foo@bar:~$ mkdir kafka2
foo@bar:~$ mv Downloads/kafka_2.12-2.7.0.tgz kafka2/  
foo@bar:~$ cd kafka2
foo@bar:~$ tar -zxvf kafka_2.12-2.7.0.tgz
foo@bar:~$ rm kafka_2.12-2.7.0.tgz
foo@bar:~$ cd kafka_2.12-2.7.0
```

Находим подпапку `config` и в ней файл `server.properties`. Раскоментируем в нем строку
`listeners=PLAINTEXT://:9092`

И добавляем переменную KAFKA_HOME в файл `.zshrc`

```console
export KAFKA_HOME=/Users/afadeev/kafka2/kafka_2.12-2.7.0
export PATH=$PATH:$KAFKA_HOME/bin
```

