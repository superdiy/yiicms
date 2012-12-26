Fad Yii Cms (dev)
===================

Легкая CMS на базе Yii (1.1.12) с основными модулями и расширениями для старта. При написании кода используется стиль PSR-1/PSR-2.

КОНФИГУРАЦИЯ
------------

/protected/config

      console.php       параметры для yiic (консоль)
      db.php            параметры подключения к базе данных (используется production.php)
      dev.php           параметры для разработки
      main.php          основные параметры - все остальные идут поверх него (mergeArray)
      production.php    конфигурация для продакшн-сервера
      urlRules.php      дополнительные правила для CUrlManager

ПОВЕДЕНИЯ
------------

/protected/components/behaviors

      AdjacencyListBehavior     простое дерево - смежные вершины (parent_id, level, sort_order (SortableBehavior))
      InlineWidgetsBehavior     встраивание виджетов в текст страницы
      NestedSetBehavior         вложенные множества (из yiiext)
      SaveBehavior              create_user_id, update_user_id, create_time, update_time
      SortableBehavior          sort_order
      StatusBehavior            статус

МОДУЛИ
------------

/protected/modules/

      admin/            главная админки — список и настройки модулей, версия Yii, PHP
      blog/             блог
      comment/          поведение комментариев
      contact/          обратная связь (поддержка отправки через SMTP)
      gallery/          галерея (galleria frontend)
      menu/             меню
      news/             новости
      page/             страницы
      rights/           права доступа (yii-rights)
      sitemap/          карта сайта (древовидный sitemap/, sitemap.xml)
      social/           социальные сети (vk, facebook)
      user/             пользователи (включает eauth, eoauth, lightopenid)

РАСШИРЕНИЯ
------------

/protected/extensions/

      aceEditor/        редактор кода (виджет)
      addThis/          социальные кнопки addThis (виджет)
      bootstrap/        yiiBooster
      elFinder/         файловый менеджер для tinyMce
      galleria/         galleria
      grid/             Nested Set GridView
      image/            Kohana Image Library
      jui/              DateTimePicker с выборкой времени
      mail/             SwiftMailer
      syncTranslit      поведение и виджет для транслита значений ActiveRecord
      tinymce           WYSIWYG редактор

/protected/modules/

      blog/extensions/taggable/     taggable Behavior
      gallery/widgets/photoManager  фотоменеджер
      news/widgets/LastNews         блок последних новостей
      user/extensions/eauth/        Yii EAuth extension

ДОПОЛНИТЕЛЬНО
------------
      /robots.txt                           Основные правила для поисковых роботов
      /protected/autocomplete.php           Автодополнение кода в IDE
      /protected/components/Controller      Расширенный RController
      /protected/components/FadTbGridView   Расширенный TbGridView
      /protected/components/WebModule       Расширенный CWebModule
      /protected/components/Widget          Расширенный CWidget

ПОЛЕЗНЫЕ ССЫЛКИ
------------

### Расширения fad yii cms

* [aceEditor](http://ace.ajax.org/)
* [addThis](http://www.addthis.com/)
* [grid](http://ludo.cubicphuse.nl/jquery-plugins/treeTable/doc/)
* [jui](http://trentrichardson.com/examples/timepicker/)
* [syncTranslit](http://snowcore.net/synctranslit)

### Сторонние расширения

* [YiiBooster](http://yii-booster.clevertech.biz/)
* [Yii-rights](http://www.yiiframework.com/extension/rights/)
* [TinyMce](http://www.yiiframework.com/extension/newtinymce/)
* [elFinder](http://elfinder.org/)
* [Galleria](http://www.yiiframework.com/extension/galleria/)
* [Kohana Image Library](http://www.yiiframework.com/extension/image/)
* [Yii EAuth extension](https://github.com/Nodge/yii-eauth)
* [loid extension](http://www.yiiframework.com/extension/loid)
* [EOAuth extension](http://www.yiiframework.com/extension/eoauth)

### Ресурсы

* [Tiwtter Bootstrap](http://twitter.github.com/bootstrap/)
* [RBAC](http://en.wikipedia.org/wiki/Role-based_access_control)
* [PSR-1/PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/)

ПЛАНЫ
------------

* **создание сайта и сообщества**
* Переход на sourceLanguage = en (~15%)
* создание нечто блоков контента (подобно ModX)
* создание шаблонов для управления правами пользователей (Rights ext) под CMS
* инсталлятор
* возможность изменять страницу прямо на сайте (подобно Google Sites)

Буду рад любой помощи в улучшении проекта, и, конечно же, пулл реквестам.