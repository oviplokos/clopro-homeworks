## Задание 1. Yandex Cloud 

**Что нужно сделать**

1. Создать бакет Object Storage и разместить в нём файл с картинкой:

 - Создать бакет в Object Storage с произвольным именем (например, _имя_студента_дата_).
 - Положить в бакет файл с картинкой.
 - Сделать файл доступным из интернета.
 
2. Создать группу ВМ в public подсети фиксированного размера с шаблоном LAMP и веб-страницей, содержащей ссылку на картинку из бакета:

 - Создать Instance Group с тремя ВМ и шаблоном LAMP. Для LAMP рекомендуется использовать `image_id = fd827b91d99psvq5fjit`.
 - Для создания стартовой веб-страницы рекомендуется использовать раздел `user_data` в [meta_data](https://cloud.yandex.ru/docs/compute/concepts/vm-metadata).
 - Разместить в стартовой веб-странице шаблонной ВМ ссылку на картинку из бакета.
 - Настроить проверку состояния ВМ.
 
3. Подключить группу к сетевому балансировщику:

 - Создать сетевой балансировщик.
 - Проверить работоспособность, удалив одну или несколько ВМ.
4. (дополнительно)* Создать Application Load Balancer с использованием Instance group и проверкой состояния.

Полезные документы:

- [Compute instance group](https://registry.terraform.io/providers/yandex-cloud/yandex/latest/docs/resources/compute_instance_group).
- [Network Load Balancer](https://registry.terraform.io/providers/yandex-cloud/yandex/latest/docs/resources/lb_network_load_balancer).
- [Группа ВМ с сетевым балансировщиком](https://cloud.yandex.ru/docs/compute/operations/instance-groups/create-with-balancer).

---

## Решение

* Скрин Бакета
  ![image](https://github.com/user-attachments/assets/b25ae841-60e4-451a-baae-7c4cb1e772ee)


Полученная ссылка для скачивания - https://storage.yandexcloud.net/kdonets-2025-13-01/cats.jpeg

#### Решение


![image](https://github.com/user-attachments/assets/ddb40c50-b115-484a-adc4-aefa52a93f02)



     * Скрин Instance Group  
     
![image](https://github.com/user-attachments/assets/ce3892a6-8f36-4200-afb9-61edfd5ca5df)


   - Скрин картинки на инстансе из Instance Group 
![image](https://github.com/user-attachments/assets/980a7f54-bc46-4407-beb6-656e6a52e69b)


3. Подключить группу к сетевому балансировщику:

 - Создать сетевой балансировщик.
 - Проверить работоспособность, удалив одну или несколько ВМ.

#### Решение


![image](https://github.com/user-attachments/assets/2b80327f-04a6-43ed-a6ea-4d9c1a6ef98b)



- Проверка работоспособности при удалении одной машины


![image](https://github.com/user-attachments/assets/33110718-8b1b-475e-ab6c-d79b7c628e32)


![image](https://github.com/user-attachments/assets/ed600927-842e-463e-975c-9383222dd24c)

