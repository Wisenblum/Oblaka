## Лабораторная работа 2
Вначале мы обновили все пакеты в репозитории Ubuntu и скачали docker на линукс с помощью команды "sudo apt update && sudo apt install docker.io" По окончании установки запустим службу Docker и добавим ее в автозагрузку, прописав данную команду в терминале:  "systemctl start docker && systemctl enable docker"
# Убедимся что сервис Docker запущен: "systemctl status docker"
![image](https://github.com/Wisenblum/Oblaka/assets/70391455/75c03458-d11b-41b9-af27-38c62a0980ba)
Создадим сначала плохой Dockerfile под названием Dockerfile.bad (также в процессе подключения к образу мы использовать команду "sudo su", так как было отказано в доступе)
![image](https://github.com/Wisenblum/Oblaka/assets/112980347/d110dede-31fb-4b57-ade9-2aebdf12bdc8)
Следом за плохим Dockerfile создадим хороший Dockerfile под названием Dockerfile.good
![image](https://github.com/Wisenblum/Oblaka/assets/112980347/7bc7be05-dce5-4822-91a6-6bc927c88414)
В хорошем Dockerfile исправлены:

-"плохие практики", включая использование конкретного тега базового образа, 
-разделение установки пакетов на несколько слоев,
-очистку кэша и временных файлов, 
-минимизацию одноразовых слоев и запуск только одного процесса в контейнере. 

Эти изменения улучшат безопасность, производительность и управляемость Docker-контейнера.
## Вывод
в данной лабораторной работе мы научились работать с Docker-ом, а именно:
-создавать Dockerfile
-подключаться к Docker образам
-работать с Docker HUB
-запускать Dockerfile
