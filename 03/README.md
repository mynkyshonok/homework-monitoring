# Домашнее задание к занятию 15 «Система сбора логов Elastic Stack»

## Задание повышенной сложности

Не используйте директорию [help](./help) при выполнении домашнего задания.

## Задание 1

Вам необходимо поднять в докере и связать между собой:

- elasticsearch (hot и warm ноды);
- logstash;
- kibana;
- filebeat.

Logstash следует сконфигурировать для приёма по tcp json-сообщений.

Filebeat следует сконфигурировать для отправки логов docker вашей системы в logstash.

В директории [help](./help) находится манифест docker-compose и конфигурации filebeat/logstash для быстрого 
выполнения этого задания.

Результатом выполнения задания должны быть:

- скриншот `docker ps` через 5 минут после старта всех контейнеров (их должно быть 5):

<img width="1690" height="140" alt="image" src="https://github.com/user-attachments/assets/f1aa1ffa-8c3e-4d12-90f5-55175f19cc11" />

- скриншот интерфейса kibana;

<img width="1563" height="879" alt="image" src="https://github.com/user-attachments/assets/7d53119a-ecbf-4339-8657-898d5db7fcf0" />

- docker-compose манифест (если вы не использовали директорию help);

[docker-compose.yml](elk/docker-compose.yml)

- ваши yml-конфигурации для стека (если вы не использовали директорию help).

[filebeat.yml](elk/filebeat.yml)

[logstash.conf](elk/logstash.conf)

## Задание 2

Перейдите в меню [создания index-patterns  в kibana](http://localhost:5601/app/management/kibana/indexPatterns/create) и создайте несколько index-patterns из имеющихся.

Перейдите в меню просмотра логов в kibana (Discover) и самостоятельно изучите, как отображаются логи и как производить поиск по логам.

В манифесте директории help также приведенно dummy-приложение, которое генерирует рандомные события в stdout-контейнера.
Эти логи должны порождать индекс logstash-* в elasticsearch. Если этого индекса нет — воспользуйтесь советами и источниками из раздела «Дополнительные ссылки» этого задания.
 
---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---

 
