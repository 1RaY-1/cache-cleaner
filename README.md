## Что это?
Простой скрипт на баше который чистит кеш своего Линукс сервера.

Он будет ждать 15дней, и чистить кеш командами:
```
rm -rf /var/cache/httpd/proxy*
htcacheclean -n -t -p /var/cache/httpd/proxy -110000M -L12000
service httpd restart
```
И так бесконечно

**Реквизиты**:
Супер Юзер (ROOT)

## О логах
Будут создаваться логи после чистки (там будет дата и время когда очистился кеш) в файле ```$HOME/.cache_cleaner_log.txt```
Но эту функцыю можно отключить на строке 15.

## Учтите
Те комманды для чистки моего сервера возможно не подойдут для вашего, так что их можно спокойно изменить от 15-ой строки.

Весь код прокомментирован, так что должно быть всё понятно.
