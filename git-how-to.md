Давайте создадим наш первый ключ при помощи команды:
ssh-keygen -t ed25519 -C "имя.фамилия@phystech.edu"

Где ed25519 это просто формат ключа, а после ключа -C идёт ваш email.
есть ли у нас уже созданные ключи:
ls ~/.ssh

 Вывести значение ключа на экран можно при помощи команды:
cat ~/.ssh/id_ed25519.pub

как добавить ключ на гитхаб
выберите пункт Settings, найдите слева пункт SSH and GPG keys, нажмите на кнопку New SSH key.
получить ключ в терминале
cat ~/.ssh/id_ed25519.pub
Чтобы проверить правильно ли вы всё сделали вызовите команду:
ssh -T git@github.com
Она должна вернуть
Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.

копируем репозиторий на комп
git clone <url>
