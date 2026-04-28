<img width="1182" height="551" alt="image" src="https://github.com/user-attachments/assets/2ac0c00c-e1ca-4702-9c6e-7d83408139fa" />
# Отчет по работе

1. Перешла в Cloud Run -> Services -> Create Cloud Service
<img width="1440" height="781" alt="image" src="https://github.com/user-attachments/assets/be256950-a0ec-4ce8-8bb9-6be3e1130a41" />

Ресурсы постаивла минимальные:

<img width="1440" height="775" alt="image" src="https://github.com/user-attachments/assets/29706abd-bc89-4c09-9c76-54450f31bae2" />

2. Сервис создан:

<img width="1440" height="780" alt="image" src="https://github.com/user-attachments/assets/4059557e-b166-419b-a425-afa30a005a10" />
Перешла по ссылке для просмотра сервиса:

<img width="1440" height="856" alt="image" src="https://github.com/user-attachments/assets/5b986bbf-2fc4-4e54-a7c7-2e66395b1bd5" />
Сервис в облаке задеплоен.
3. Перешла в раздел Observability для просмотра логов и метрик:

<img width="1440" height="778" alt="image" src="https://github.com/user-attachments/assets/1327e145-847e-42b2-99f0-30a98806e80a" />
4. В Логах видим, что сервис успешно запустился, а также успешные запросы GET от пользователй (Я заходила на сайт)

<img width="1185" height="546" alt="image" src="https://github.com/user-attachments/assets/d8bed272-3983-4315-8e81-a5613ec55862" />
5. В метриках тоже все ок, видим, что запросов пока что мало, небольшое время отклика.

<img width="1182" height="551" alt="image" src="https://github.com/user-attachments/assets/f9bb7afb-5913-4e96-88b1-7b4fa9468edc" />

6. Перейдем к изменению порта на: 8090
Изменила порт и задеплоила сервис.

<img width="1440" height="778" alt="image" src="https://github.com/user-attachments/assets/42506605-2553-41d3-b6d9-66413629ccb4" />

<img width="1440" height="777" alt="image" src="https://github.com/user-attachments/assets/14c1c76f-8f7c-4b83-9e67-22fa4c150229" />

После изменения мы видим, что сервис успешно открывается:

<img width="1440" height="855" alt="image" src="https://github.com/user-attachments/assets/bc8d54a4-55eb-4412-ae05-e8ba076634cb" />
Также это видно в логах, ошибок в логах нет:

<img width="1440" height="776" alt="image" src="https://github.com/user-attachments/assets/368fdb32-cbb3-40ce-9c07-03137ac2d1b6" />

<img width="1185" height="551" alt="image" src="https://github.com/user-attachments/assets/4fee39cc-0fb4-4eda-a3a8-552db97d0682" />

Далее я распределила трафик 50/50 между двумя версиями:

<img width="1440" height="776" alt="image" src="https://github.com/user-attachments/assets/b8fede1b-19c6-4abc-850f-39db88b1bf9f" />
При распределении трафика не наблюдается резких изменений в нагрузке и скорости ответа сервиса.

<img width="1181" height="574" alt="image" src="https://github.com/user-attachments/assets/645fca90-305c-43f4-8421-b0ebb1e990b6" />
В логах фиксировались успешные ответы (HTTP 200), что свидетельствует о корректной работе обеих версий. Оба сервиса доступны по ссылке.
Метрики показали равномерную нагрузку, низкое время отклика и отсутствие ошибок. 
Существенной разницы в работе версий выявлено не было, так как функциональность сервиса осталась неизменной.
