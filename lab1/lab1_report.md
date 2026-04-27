University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [Cloud platforms as the basis of technology entrepreneurship](https://) ADD link

Year: 2026

Group: U4125

Author: Popova Alina Romanovna

Lab: Lab1

Date of create: 27.04.2026

Date of finished: 

# Отчет по выполнению лабораторной работы

1. На вкладке Service Accounts создала сервисный аккаунт - apopova-sa-lab1-cloud-platform@cloud-platforms-as-the-basis.iam.gserviceaccount.com:
<img width="1439" height="778" alt="image" src="https://github.com/user-attachments/assets/5acea36f-06fe-495c-95fb-7b5b5cb8dade" />
<img width="1439" height="731" alt="image" src="https://github.com/user-attachments/assets/44a2e10a-dbd3-49c5-b52d-5c5a1093ca18" />
Это необходимо для предоставления доступа приложению к облаку. ( А не вручную через личный аккаунт)

2. Перейдем к созданию виртуальной машины:

   Создала виртуальную машину с Machine type e2-micro в режиме spot (Минимальная конфигурация ресурсов):
<img width="1440" height="780" alt="image" src="https://github.com/user-attachments/assets/ca7fbc32-b8b0-4697-bbba-38ff2885be0e" />
<img width="1131" height="731" alt="image" src="https://github.com/user-attachments/assets/1a2bbd41-8a7a-405b-9060-e8c91ea16f26" />

3. Нашла бакет при помощи утилиты и скопировала оттуда файлы на свою локальную VM
<img width="1440" height="777" alt="image" src="https://github.com/user-attachments/assets/b5c91b28-48e1-42fa-b3c1-244d2e77068e" />

4. Перешла к изменению прав для моего service account - поменяла storage admin на compute viewer
<img width="1440" height="773" alt="image" src="https://github.com/user-attachments/assets/a6fe9a38-4042-49aa-a160-7d7861235fb6" />

5. Повторно скопировала данные в папку на мою VM - данные скопировались (обновились)
<img width="1440" height="778" alt="image" src="https://github.com/user-attachments/assets/d71b2ecb-092e-4128-9ba2-c1c5bc507b6b" />
После изменения роли сервисного аккаунта с Storage Admin на Compute Viewer доступ к данным в бакете сохранился. Это связано с тем, что доступ к Cloud Storage может предоставляться другими ролями (например, Editor) или наследоваться на уровне проекта. Таким образом, удаление одной роли не всегда приводит к потере доступа, если существуют другие разрешения.

7. Остановила и удалила VM
<img width="1440" height="781" alt="image" src="https://github.com/user-attachments/assets/c56b0010-fff8-4f16-b055-e478cb30b174" />
<img width="1440" height="777" alt="image" src="https://github.com/user-attachments/assets/38041747-fb34-4679-af48-d0c64dafcdc3" />

