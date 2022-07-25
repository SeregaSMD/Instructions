# Как включить ssh в Windows 10

В ОС Windows 10 по умолчанию уже есть ssh. Его надо только активировать.

Зайдите в Параметры - Приложения - Приложения и возможности - Дополнительные компоненты. В указанном спсике найдите **Клиент OpenSSH**, жмите установить.

Откройте cmd.

Наберите команду 
```sh
C:\Users\USER\> ssh
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface]
           [-b bind_address] [-c cipher_spec] [-D [bind_address:]port]
           [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11]
           [-i identity_file] [-J [user@]host[:port]] [-L address]
           [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
           [-Q query_option] [-R address] [-S ctl_path] [-W host:port]
           [-w local_tun[:remote_tun]] destination [command]
```
Перейдите к созданию ssh ключа.


# Что такое ssh

SSH (англ. Secure Shell — «безопасная оболочка»[1]) — сетевой протокол прикладного уровня, позволяющий производить удалённое управление операционной системой и туннелирование TCP-соединений (например, для передачи файлов). Схож по функциональности с протоколами Telnet и rlogin, но, в отличие от них, шифрует весь трафик, включая и передаваемые пароли. SSH допускает выбор различных алгоритмов шифрования. SSH-клиенты и SSH-серверы доступны для большинства сетевых операционных систем.

#  Как сгенерировать ssh ключ для github

Необходимо выполнить команду
```sh
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Фразу пароль можно оставить пустой
```sh
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

Задайте имя ключа. В текущей директории появится два файла:
- *new_key* - закрытый ключ. Никому его не передавайте и храните в надежном месте!!!
- *new_key.pub* - открытый ключ. Его необходимо загрузить на github
