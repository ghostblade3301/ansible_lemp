# Установка LEMP-стека с cms joomla
1. Клонируем репизиторий
```bash
git@github.com:ghostblade3301/ansible_lemp.git
```
2. Выполняем запуск playbook. Сначала вводим пароль от sudo, а затем пароль от хранилища.
```bash
ansible-playbook install_lemp.yaml -i inventory.yaml -b -K --ask-vault-pass
```
3. Выполняем установку joomla. Используем следующий адрес:
```
http://ip-адрес-вашего-сервера/installation/index.php
```
4. Далее указываем название вашего сайта.

![01](https://github.com/ghostblade3301/ansible_lemp/blob/main/screenshots/01.jpg)

5. Затем необходимо будет указать логин и пароль администратора. Он не должен быть короче 12 символов.

![02](https://github.com/ghostblade3301/ansible_lemp/blob/main/screenshots/02.jpg)

6. Далее, для заполнения полей используем переменные и их значения из файла vault.yaml.
Структура файла vault.yaml показана в файле vault.example

![03](https://github.com/ghostblade3301/ansible_lemp/blob/main/screenshots/03.jpg)