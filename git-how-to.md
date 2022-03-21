**Создание ssh ключей**
Открыть Git-Bash. Вставить следующий код:
```ssh-keygen -t ed25519 -C "your_email@example.com"```
Эта команда создаёт новую пару ключей: приватный и публичный
Нажать Enter, чтобы принять предложенное название и расположене файла по умолчанию.
>Enter file in which to save the key (/c/Users/vergg/.ssh/id_ed25519):
Нажать дважды Enter, чтобы не создавать пароль для доступа к ключу
>Enter passphrase (empty for no passphrase):
>Enter same passphrase again:
**Добавление ssh ключей в аккаунт на GitHub**
Открыть 'Settings'
Открыть 'SSH and GPG keys'
Нажать 'New SSH key'
Копировать ключ из созданного текстового файла с публичным ключом и вставить его в окно key
Нажать 'Add SSH key'
**Клонирование репозиторий**
Включить ssh-agent следующей командой:
>eval "$(ssh-agent -s)"
Добавить приватный ключ в агент:
>ssh-add ~/.ssh/file_with_key
Пройти аутентификацию:
>ssh -T git@github.com
Открыть директорию в которое производится клонирование:
>cd directoria
Клонировать репозиторий:
>git clone SSH_URL_of_file