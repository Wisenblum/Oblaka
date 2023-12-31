# Аналитическая лабораторная работа 1
## Состав комманды
- Панин Михаил (Капитан) 368628 К3222
- Гневашев Андрей 368031 К3222
## Дано
1. Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Символ % в начале/конце означает, что перед/после него может стоять любой набор символов.
2. Google с документациями провайдера
## Описание сервисов
- Amazon ElastiCache - это сервис, спроектированный для формирования и управления хранилищами в памяти, совместимыми с Redis и Memcached. Обеспечивает полностью управляемое хранилище ключ-значение с временем отклика менее 1 миллисекунды, включая возможности развертывания, поддержки и масштабирования.
- Amazon Elasticsearch – это распределенный поисковый и аналитический движок на базе Apache Lucene. Обычно используется для таких примеров, как анализ журналов, полнотекстовый поиск, интеллектуальные системы безопасности, бизнес-аналитика и мониторинг текущих процессов.
- Amazon Quantum Ledger Database (QLDB) - это база данных, предоставляющая возможность вести записи с неизменяемой историей всех изменений, поддерживаемой криптографической проверкой данных. Она работает с языком запросов PartiQL и функционирует в режиме Serverless. Хотя она имеет некоторые схожести с блокчейном, она централизована и не требует нескольких подтверждений, что делает ее более эффективной. Подходит в ситуациях, где критически важно сохранять историю всех изменений, например, в финансовых транзакциях.
- Amazon Key Management Service (KMS) - это сервис, который предоставляет возможность создания криптографических ключей, управления их жизненным циклом и обеспечивает шифрование и дешифрование данных с использованием этих ключей для обеспечения высокого уровня безопасности данных. Доступ к ключам регулируется гибкой политикой безопасности. Ключи генерируются и хранятся в аппаратных модулях с соответствием стандарту FIPS 140, что гарантирует их высокую степень защиты. KMS тесно интегрирован с многими сервисами AWS, обеспечивая надежное управление ключами для различных сценариев использования.
- Amazon CloudHSM - это сервис, предоставляющий возможность размещения ключей шифрования и выполнения криптографических операций в выделенном кластере аппаратных модулей безопасного хранения (HSM). Этот сервис обеспечивает высокий уровень безопасности для ключей и криптографических операций, предоставляя изолированное окружение в виде кластера HSM в облаке. CloudHSM поддерживает различные стандарты безопасности и может использоваться для защиты конфиденциальных данных и выполнения критических криптографических функций в облаке AWS.
- Amazon Rekognition - это сервис, предоставляющий возможности компьютерного зрения для глубокого анализа фотографий и видеоматериалов. С помощью этого сервиса можно обнаруживать и анализировать лица, текст, а также идентифицировать логотипы и этикетки на изображениях. Кроме того, Rekognition обеспечивает функциональность модерации контента, позволяя выявлять материалы, несоответствующие стандартам безопасности (NSFW). Этот сервис может легко интегрироваться с другими сервисами AWS, расширяя возможности анализа изображений в облачной среде.
- Amazon Textract - это сервис, специализирующийся на компьютерном зрении с целью извлечения текста с различных типов документов, включая отсканированные документы, таблицы, формы и другие. Он обеспечивает возможность извлечения информации из текста, а также поддерживает распознавание рукописного текста. Textract значительно упрощает процесс анализа и обработки документов, автоматизируя извлечение текстовой информации.
- Amazon Lex - это сервис, который предоставляет возможность создания разговорных чат-ботов с использованием "разговорной" речи. Боты, созданные с помощью Amazon Lex, могут оперировать в соответствии с предварительно определенными сценариями разговора, обеспечивая идеальную базу для взаимодействия с пользователями. Этот сервис поддерживает как текстовые, так и голосовые беседы, предоставляя гибкость в выборе формата взаимодействия.
- AWS CodePipeline представляет собой полностью управляемый сервис для процессов непрерывной интеграции и развертывания (CI/CD). Пользователи могут воспользоваться им для автоматизации шагов создания, тестирования и развертывания программного обеспечения. CodePipeline обеспечивает детальную обратную связь о статусе выпуска, поддерживает интеграцию с различными инструментами и предоставляет возможность настройки гибких конвейеров поставки, способствуя оптимизации процессов разработки и развертывания.
- Amazon Simple Email Service (SES) представляет собой сервис по отправке электронной почты, который легко интегрируется в различные приложения. SES является идеальным выбором для отправки как транзакционных сообщений, так и массовых рекламных рассылок.
- Amazon Simple Notification Service (SNS) представляет собой сервис, предназначенный для отправки уведомлений как сервисам AWS, так и конечным пользователям (клиентам).

## Маппинг
![image](https://github.com/Wisenblum/Oblaka/assets/70391455/e19e30ae-f37d-4220-846a-6cb2eae733a7)
## Возможности миграции
Опираясь на mapping , мы можем сделать вывод, что сейчас масштабная миграция с AWS на Yandex.Cloud невозможна, так как условия некоторых сервисов не соблюдены. С другой стороны, значительную часть сервисов можно переносить уже сейчас.
## Итоговая таблица
![image](https://github.com/Wisenblum/Oblaka/assets/112980347/404a8465-afd6-4ee5-881a-05a083b355fa)

## Вывод
В процессе выполнения данной лабораторной работы была создана таблица, в которую были внесены сведения из материалов, предоставленных Amazon и Yandex. Задача работы успешно выполнена: мы изучили облачные сервисы и сформировали понимание различных способов использования сервисов в сервисной-модели
