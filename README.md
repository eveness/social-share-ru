# social-share-ru
Социальные кнопки для верстки (HTML & CSS & Inline-CSS BASE64 SVG).

![](https://img-fotki.yandex.ru/get/4515/99156821.0/0_1a0729_59c14de_orig.jpg)

[Демо на CodePen](http://codepen.io/eveness/pen/OyvXov)

## Установка
При помощи [Bower](http://bower.io/):
```
bower install social-share-ru
```

Скачать этот репозиторий:
```
git clone https://github.com/eveness/social-share-ru.git
```

## Переменные в шаблоне для замены
Переменная | Описание
---------|-------------
`{{url}}` | Ссылка для расшаривания (URL-кодированная).
`{{title}}` | Заголовок страницы.
`{{description}}` | Описание страницы.
`{{image}}` | Ссылка на изображение.
`{{hashtags}}` | Хэш-теги через запятую, без `#` (для LiveJournal и Twitter).
`{{via}}` | Ник автора в Twitter, без `@`.
`{{html}}` | HTML-код для поста (URL-кодированный) для LiveJournal, например `<p>{{description}}</p><p><a href="{{url}}">Подробнее</a></p>`.

## Использование разметки OpenGraph
Для контроля передачи данных в `<head>` добавить метаданные:
```html
  <meta property="og:title" content="{{title}}">
  <meta property="og:description" content="{{description}}">
  <meta property="og:url" content="{{url}}">
  <meta property="og:image" content="{{image}}">
  <meta property="og:type" content="website">
```

## Дополнительно
Не забывать, что `inline-block` имеет отступы в зависимости от браузера. Самый простой способ от них избавиться - убрать переводы строк и пробелы между всеми ссылками (сделать все ссылки в одну строку). Затем уже можно добавить нужный `margin` к классу `.social-share_link`.

Все исходные файлы SVG лежат соответственно в папке `svg`. Можно редактировать на свой вкус и вставлять, кодируя в Base64, например тут: [base64.ru](http://base64.ru/).

## Иконки
- Вконтакте, Facebook, Twitter, Google+, LinkedIn, Pinterest, Pocket: [Font Awesome](http://fontawesome.io/)
- Мой Мир@Mail.Ru: отредактированная версия [Social Flat Rounded Rects](https://www.iconfinder.com/icons/386659/mail.ru_mailru_icon) (Creative Commons (Attribution 3.0 Unported))
- LiveJournal: отредактированная версия [найденой иконки в обсуждении на GitHub](https://github.com/FortAwesome/Font-Awesome/issues/1657#issuecomment-68190079)

## Материалы и ссылки
- [Social Network Share Link Formats](http://themergency.com/social-network-links/)
- [Избавляемся от JavaScript в социальных кнопках (Facebook, VK, Twitter и др.)](http://habrahabr.ru/post/250021/)
- [Social Media Colours – Hex and RGB Colours of the Web](http://designpieces.com/2012/12/social-media-colours-hex-and-rgb/)
- [Элементарные социальные share-кнопки](http://habrahabr.ru/post/156185/)
- [LiveJournal share button](http://expange.ru/e/LiveJournal+share+button)
