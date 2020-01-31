## Интеграция принтера Flying Bear Ghost 4S в Cura.

----
### Что сделано:

* В меню добавления нового принтера в Cura добавлены:
  * производитель Flying Bear
    * принтер Flying Bear Ghost 4S

* В профиле принтера настроены габариты рабочего стола, g-code начала и окончания печати.

* Скрыты все встроенные в Cura материалы (т.к. в основном недоступны для покупки и не используются). Generic материалы остаются видимыми и доступными для использования при создании новых материалов.

* Настройки принтера по-умолчанию(скорости, ускорения, джерки и пр.) взяты из стокового файла настроек robin_nano35_cfg.txt, дополнительные настройки печати - на основе существующих файлов для Creality Ender-3.

* В меню выбора материалов добавлены популярные у нас: Bestfilament и FD Plast. Влияет на температуры сопла и стола, обдув, ретракт и скорость ретракта. В описании рекомендации по печати от производителя.

* Отображение модели и текстуры стола Flying Bear Ghost 4S в окне программы.

----
> Полная версия:

> !!! На Github пока что только полная версия, разделение на полную и обычную будут позже.

> **!!! Полная версия не рекомендуется обычному пользователю  !!!**

>* Профили диаметра сопла (рядом с выбором материала вверху), влияют на ширину экструзии и сопустсвующие параметры. Созданы на основе существующих файлов для Creality Ender-3.

>* Профили качества (меняют высоту слоя и некоторые другие параметры), выбор привязан к диаметру сопла. Влияют на соотношение качество/скорость печати. Созданы на основе существующих файлов для Creality Ender-3.

>* Совместимость с профилями для Creality Ender-3, что позволяет импортировать их и использовать для Flying Bear Ghost 4S.

----
### Инструкция:

* Скачайте последний выпуск [ОБЫЧНОЙ](https://drive.google.com/open?id=13govLWyr8Txo5nbOs2NAE4m9y-cj8SGW) или [ПОЛНОЙ](https://drive.google.com/open?id=17S1zDlG4TW7I69NR5O05RSkkdTHsj6PY) версии
    
* Экспортируйте нужные вам профили печати из меню программы Cura

* Закройте программу Cura

* *Windows*: удалите все файлы по пути %USERPROFILE%\AppData\Local\cura\ВЕРСИЯ_КУРЫ\ 

>  Необязательный пункт. В процессе тестирования Cura иногда использовала кэш старой версии из этой папки вместо того, чтобы подхватывать изменения в новых файлах. Требуется дополнительное тестирование.

* *Windows*: распакуйте архив по пути %USERPROFILE%\AppData\Roaming\cura\ВЕРСИЯ_КУРЫ\

>  Во время обновления до новой версии, например 4.3 -> 4.4, Cura создаёт новую папку с названием, соответствующим новой версии. Есть шанс, что при этом файлы не мигрируют в новую папку и их придётся перенести вручную. Требуется дополнительное тестирование. Устанавливать в системную папку "Program Files" крайне не рекомендуется, т.к. профиль не оттестирован на 100%.

* Запустите программу Cura

* Если пакет файлов установлен впервые, добавьте новый принтер.

>Add Printer > Add a non-networked printer > Flying Bear > Flying Bear Ghost 4S

* Импортируйте профили печати если нужно. Профили от обычной версии импортируются и в обычную и в полную; от полной версии импортируются только в полную, т.к. требуют профилей качества.

>  В редких случаях файлы от  старых принтеров могут мешать нормальной работе интеграции. В этом случае нужно сделать сброс программы. !!! ВНИМАНИЕ! ДАЛЬНЕЙШИЕ ДЕЙСТВИЯ ПРИВЕДУТ К ПОТЕРЕ ВАШИХ НАСТРОЕК ПРОГРАММЫ И ПЕЧАТИ!!! Экспортировать ваши профили печати чтобы не потерять их. Закройте Cura. Сохраните папку %USERPROFILE%\AppData\Roaming\cura\ВЕРСИЯ_КУРЫ\ на всякий случай в другое место, затем удалите все папки и файлы из %USERPROFILE%\AppData\Roaming\cura\ВЕРСИЯ_КУРЫ\ и %USERPROFILE%\AppData\Local\cura\ВЕРСИЯ_КУРЫ\ . Это полностью сбросит Cura, удалит все ваши настройки, профили и т.д. После этого установите интеграцию как описано выше и добавьте новый принтер.

----
### Изменения:

* 2020.01.15 - первый релиз

* 2020.01.16 - переделан стартовый и конечный g-code, параметры печати для материалов Bestfilament и FD Plast исправлены c рекомендуемых на вменяемые

* 2020.01.17 - добавлена модель (автор @ORecTeam) и текстура стола Flying Bear Ghost 4S. Добавлен пункт инструкции с удалением папки в \AppData\Local

* 2020.01.21 - изменена текстура стола, логотип теперь сделан по-человечески (автор @RamSoft) и добавлена инструкция по сбросу программы Cura.

* 2020.01.31 - мелкие правки в профилях материалов

----
### Благодарности:

* @a3lme
* @TheDemonCat
* @ORecTeam
* @RamSoft
* Всем, кто помогал тестировать и находить ошибки