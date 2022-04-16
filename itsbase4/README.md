# Лабораторная работа № 4. Робин Бобин Барабек
####

Есть (ну как есть, для начала их нужно поднять) виртуальные машины:
1.rrobin
2.web1
3.web2

#### Задачи: 
* Сервера web1, web2 должны работать по порту 8080, отдавать кастомную страницу;
* На сервере rrobin должна быть балансировка нагрузки серверов web1 и web2;
* Установка и настройка должна быть Ansible-сценарием;
* Создать playbook, где расписываем роли  web1, web2, rrobin


<a href="https://imgbb.com/"><img src="https://i.ibb.co/MZKhJzv/index.jpg" alt="index" border="0"></a>

#### Используемые команды:

nginx- Веб-сервер и почтовый прокси-сервер, работающий на Unix-подобных операционных системах.
SELinux  — реализация системы принудительного контроля доступа, которая может работать параллельно с классической избирательной системой контроля доступа

```
vagrant up
```
> Запуск виртуальных машин и серверов
```
sudo apt install nginx
```
> Установка nginx(Вдруг не установлен, у меня вот не был, к примеру)
```
sudo systemctl enable nginx
```
> Добавление в автозагрузку 
```
ansible-playbook nginx.yml
```
> Запуск самого Playbook-а

## Кастомная страница 1

<a href="https://ibb.co/SVbkcLZ"><img src="https://i.ibb.co/ssnTCBX/2022-04-04-22-48-11-cut-photo-ru.png" alt="2022-04-04-22-48-11-cut-photo-ru" border="0"></a>

## Кастомная страница 2 
<a href="https://ibb.co/rH3RpRS"><img src="https://i.ibb.co/1TMtXt5/2022-04-04-22-48-15-cut-photo-ru.png" alt="2022-04-04-22-48-15-cut-photo-ru" border="0"></a>
#### Как выполнить задание?

    Клонировать репозиторий
    git clone https://github.com/q1ove/Levchenko-s-labs.git
    В терминале открыть папку itsbase
    Открываем Vagrantfile
    меняем 46ую строчку ssh_pub_key = File.readlines("/home/sirius/.ssh/id_rsa.pub").first.strip
        надо указать тут свой путь до ключа
    чтобы поднять виртуальные системы, вводим в консоль vagrant up
    чтобы установить весь софт, вводми в консольansible-playbook nginx.yml
#### Всё! Гуд джоб


