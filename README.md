# Тестовое задание

Achtung: для выполнения этого задания необходимо сделать fork - ... - pull request

## Задача

Используя https://www.npmjs.com/package/twitter#streaming-api решить следующую задачу:

Подписаться на сообщения где есть слово `"Trump"` и разделить их на две группы: где есть слово `"Putin"` и где есть слово `"Hillary"`.

Получится 2 источника сообщений `[Trump, Putin]` и `[Trump, Hillary]`. Их нужно скомбинировать таким образом:

```
            P1 P2    P3
T,P:     |--x--x-----x---------->
              H1          H2
T,H:     |----x-----------x----->

              [P1,H1]     [P2,H2]
combine: |----x-----------x----->
```

Результат каждой группы выводить в консоль в режиме реального времени:

```
Authors: P1.authorName, H1.authorName
Messages:
>>> P1.body
<<< P2.body
```

## Бонусная задача

Написать тесты

## Рекомендации

- Для реализации асинхронной обработки данных предлагаем воспользоваться одной из FRP библиотек на выбор(Rx.js, Bacon.js, Most.js, Kefir.js, etc).
- Для тестов Mocha, Chai
