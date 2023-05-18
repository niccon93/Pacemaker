# Домашнее задание к занятию 10.3 «Pacemaker»


### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c Шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и вашу фамилию и имя
   - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
   - для корректного добавления скриншотов воспользуйтесь инструкцией ["Как вставить скриншот в шаблон с решением"](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
   - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.

Желаем успехов в выполнении домашнего задания!

---

### Задание 1

Опишите основные функции и назначение Pacemaker.

*Приведите ответ в свободной форме.*

Ответ:

Pacemaker - это менеджер ресурсов кластера, который используется для управления высокодоступными приложениями и сервисами в распределенной среде. Основные функции и назначение Pacemaker включают в себя:
1. Позволяет находить и устранять сбои на уровне нод и служб.
2. Не зависит от подсистемы хранения: общий диск не требуется.
3. Не зависит от типов ресурсов: все, что можно прописать в скрипты, можно кластеризовать.
4. Поддерживает STONITH (Shoot-The-Other-Node-In-The-Head), то есть умершая нода изолируется и запросы к ней не поступают, пока нода не отправит сообщение о том, что она снова в рабочем состоянии.
5. Поддерживает кворумные и ресурсозависимые кластеры любого размера.
6. Поддерживает практически любую избыточную конфигурацию.
7. Может автоматически реплицировать конфиг на все узлы кластера - не придется править все вручную.
8. Можно задать порядок запуска ресурсов, а также их совместимость на одном узле.
9. Поддерживает расширенные типы ресурсов: клоны (когда ресурс запущен на множестве узлов) и дополнительные состояния (master/slave и подобное) - актуально для СУБД (MySQL, MariaDB, PostgreSQL, Oracle).
10. Имеет единую кластерную оболочку CRM с поддержкой скриптов.
Pacemaker не является единственным решением для построения кластеров и существуют другие программы, такие как Corosync, Keepalived и Heartbeat, которые также могут использоваться для этой цели. Однако, Pacemaker считается одним из наиболее распространенных и мощных решений для построения кластеров в современных IT-системах.
---

### Задание 2

Опишите основные функции и назначение Corosync.

*Приведите ответ в свободной форме.*

Ответ:

Corosync - это программное обеспечение, которое используется для создания и управления кластерами серверов в высоконагруженных и отказоустойчивых системах. Основные функции и назначение Corosync включают в себя:
1. Обеспечение отказоустойчивости: Corosync обеспечивает отказоустойчивость системы, позволяя серверам в кластере работать в режиме резервирования. Если один из серверов выходит из строя, другой сервер в кластере автоматически принимает на себя работу, обеспечивая непрерывность работы системы.
2. Управление ресурсами: Corosync управляет ресурсами в кластере, такими как доступ к файловой системе, сетевым интерфейсам и другими ресурсами. Это позволяет обеспечить равномерное распределение ресурсов между серверами в кластере.
3. Синхронизация данных: Corosync обеспечивает синхронизацию данных между серверами в кластере, что позволяет сохранять целостность данных и избежать потери информации.
4. Мониторинг состояния системы: Corosync мониторит состояние серверов в кластере и предупреждает администраторов о возможных проблемах, таких как отказ сервера или перегрузка системы.
5. Управление доступом: Corosync управляет доступом к ресурсам в кластере, обеспечивая безопасность системы и защиту от несанкционированного доступа.
Corosync является важным инструментом для создания и управления отказоустойчивыми системами, которые могут обрабатывать большие объемы данных и обеспечивать непрерывность работы при возникновении сбоев.
---

### Задание 3

Соберите модель, состоящую из двух виртуальных машин. Установите Pacemaker, Corosync, Pcs. Настройте HA кластер.

*Пришлите скриншот рабочей конфигурации и состояния сервиса для каждого нода.*

Ответ:

![img](img/1.1.PNG)
![img](img/1.2.PNG)
![img](img/1.3.PNG)
![img](img/1.4.PNG)
![img](img/1.5.PNG)
