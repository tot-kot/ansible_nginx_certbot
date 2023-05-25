## Playbook для установки Nginx proxy с Let's Encrypt SSL сертификатом
#### Устанавливает:
* Nginx
* epel-release
* snapd
* certbot

#### Настройка окружения:
1. Установить зависимости  
```
ansible-galaxy install -r requirements.yaml  
ansible-galaxy collection install -r requirements.yaml
```
2. Добавить в *inventory.yaml* адрес сервера
2. Поправить Upstream и Hostname в *vars.yaml*
3. Запустить playbook `ansible-playbook playbook.yaml`

#### Выпуск и настройка сертификата:
```
sudo certbot --nginx
```