# Проблема XY

Оригинал: [XYProblem.Info](https://xyproblem.info/)

## Что это такое?

«Проблема XY» («Ошибка молотка», «Ошибка XY», «Вопрос XY», XY Problem) — это когда вы спрашиваете о своей _попытке решить_ проблему, а не о самой _проблеме_. В результате вызванного недопонимания все стороны теряют огромное количество времени и сил.

* Пользователь хочет X.
* Пользователь не знает как сделать X, но думает, что сможет найти решение, если ему удастся сделать Y.
* Пользователь не знает как сделать и Y.
* Пользователь спрашивает помощи по Y.
* Другие пытаются помочь пользователю с Y, но несколько в замешательстве, потому что Y кажется очень странной проблемой.
* Спустя кучу сообщений и потерянного времени, оказывается, что пользователю нужна помощь с X, а Y даже не является подходящим для X решением.

Проблема возникает, когда люди слишком фокусируются на своём решении, и не могут отступить и пояснить суть проблемы.

## Что делать в такой ситуации?

1. Старайтесь приложить контекст проблемы целиком, а не только о вашей попытке решения.

2. Если вас просят дать больше информации — сделайте это.

3. Если вы уже отмели какие-то варианты решения, расскажите, почему вы так поступили. Это позволяет получить представления о ваших требованиях к решению.

Помните: если бы ваша теория о решении была бы верна, то и не просили бы о помощи, так ведь?

## Примеры

### Пример №1

valera2000 требуются не последние 3 символа в названии файла — ему требуется его расширение. Так почему бы спросить не об этом?

```
<valera2000> Как получить последние три символа в названии файла?
<mary_goes_round> Если они в переменной foo, то: echo ${foo: -3}
<mary_goes_round> Но почему три символа? Тебе ТОЧНО требуется именно это?
<mary_goes_round> Может, расширение файла?
<valera2000> Ага.
<mary_goes_round> Нет гарантии, что расширение в названии файла будет состоять из трех символов.
<mary_goes_round> Так что просто их взятие будет работать только в определенных случаях.
<mary_goes_round> echo ${foo##*.}
```

### Пример №2

Если бы Валера начал с того, что он хочет предотвратить определение его ОС, диалог мог бы стать намного короче и продуктивнее.

```
Валера: 'nmap -O -A 127.0.0.1' выдаёт несколько линий с 'OS:'. Можно это как-то изменить?
Маша: Глянь исходный код nmap, найди как оно определяет Линукс, и перепиши стэк TCP/IP так, чтоб nmap не мог определить ОС.
Валера: Ага... Но я вообще не разбираюсь в API систем Линукса.
Маша: Ну, nmap определяется по тому, как оперирует стэк TCP/IP. Так что способа изменить это дело нет, кроме как переписыванием стэка.
Валера: Я очень хочу избежать вывода этих сообщений. Может, iptables справится с этой задачей?
Маша: Можешь просто не использовать определение ОС или сканирование версии в nmap.
Валера: Я хочу скрыть свою ОС от других, а не перестать видеть чужие.
```

[Источник 1](http://meta.stackoverflow.com/questions/66377/what-is-the-xy-problem) ··· [Источник 2](http://mywiki.wooledge.org/XyProblem)
