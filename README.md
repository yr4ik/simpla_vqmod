
#[Скачать последнюю версию](http://github.com/yr4ik/Simpla-vqmod/releases/)

[vQmod (Virtual Quick Mod)](https://github.com/vqmod/vqmod/wiki)  - это система, которая виртуально вносит изменения в исходный код системы но при этом не затрагивая файлы на прямую. Изменения вносятся путем создания XML-файла, в котором программно описывается, что и где искать/заменять. Эти файлы обрабатываются во время загрузки страницы. Затем файлы с уже внесенными изменениями сохраняются как временные, после чего эти файлы будут использоваться в дальнейшем при загрузке страниц.

Данный функционал активно использовался на старых версиях в движках OpenCart 1.5.х
После активного его использования пользователями, авторы OpenCart, решили и себе использовать такой же способ внесения правок для модулей. И с версии 2.0 в стандартный дистрибутив Opencart входит аналогичный модуль OCMod но более адаптирован к движку.

Установка затрагивает файлы:
* /.htaccess
* ~~/index.php~~ (убрано в версии 2.2)
* /api/Simpla.php
* /config/config.php
* ~~/simpla/index.php~~ (убрано в версии 2.2)



## Установка:
1. Скачиваем архив (приложенный ниже) и распаковываем его в корень сайта
2. При необходимости выставляем права 755 на каталоги vqmod и vqmod/vqcache
3. Проходим по ссылке http://ВАШ_САЙТ/vqmod/install
4. Если увидели сообщение:

>VQMOD HAS BEEN INSTALLED ON YOUR SYSTEM!

Значит все прошло успешно и можно начинать пользоваться

Наши моды ложим в папку **vqmod/xml**
Что касается синтаксиса xml-файлов - то [от авторов vqmod на англ](https://github.com/vqmod/vqmod/wiki/Examples) или [тоже самое на русском](http://senokosov.info/opencart/vqmod).
Так же, если кому нужно, то можно установить [генератор xml-файлов](https://github.com/uksb/vqgen)



## Удаление _(после версии 1.2)_:
1. Проходим по ссылке http://ВАШ_САЙТ/vqmod/uninstall
2. Вводим логин и пароль администратора.
3. Если увидели в конце сообщение: 

>VQMOD HAS BEEN UNISTALLED ON YOUR SYSTEM!

Значит все успешно удалено.



## Обновление _(после версии 1.2)_:
1. [Выполняем удаление vqmod](#Удаление-после-версии-12).
2. Удаляем все содержимое (**кроме папок cfg, mod и xml**) с папки vqmod
3. [Дальше устанавливаем новую версию с заменой файлов](#Установка) **кроме папки cfg (если там делались изменения)**


### Примечание:
После установки, в изменяемых файлах, появятся коды с комментариями:
```php
#VQMOD#
..... code ...
#VQMOD_END#
```
Их удалять и изменять - **нельзя**. Иначе будет невозможна деинсталяция vqmod.


**Примеры xml:**
[Добавление нового поля к товару](http://forum.simplacms.ru/topic/11871-237-vqmod-simpacms-v13/#entry92231)

**Примеры mod:**
[Возможность оставлять комментарии к страницам](http://forum.simplacms.ru/topic/12009-237-vqmod-возможность-оставлять-комментарии-к-страни/)
