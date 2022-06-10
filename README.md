# Криптографические методы защиты информации

Учебное пособие по [защите информации](http://wikimipt.org/wiki/%D0%97%D0%B0%D1%89%D0%B8%D1%82%D0%B0_%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%B8) [кафедры радиотехники и систем управления МФТИ](https://mipt.ru/education/chairs/radiotech_telecom/).

* [Владимиров Сергей Михайлович](http://wikimipt.org/wiki/%D0%92%D0%BB%D0%B0%D0%B4%D0%B8%D0%BC%D0%B8%D1%80%D0%BE%D0%B2_%D0%A1%D0%B5%D1%80%D0%B3%D0%B5%D0%B9_%D0%9C%D0%B8%D1%85%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2%D0%B8%D1%87)
* [Габидулин Эрнст Мухамедович](http://wikimipt.org/wiki/%D0%93%D0%B0%D0%B1%D0%B8%D0%B4%D1%83%D0%BB%D0%B8%D0%BD_%D0%AD%D1%80%D0%BD%D1%81%D1%82_%D0%9C%D1%83%D1%85%D0%B0%D0%BC%D0%B5%D0%B4%D0%BE%D0%B2%D0%B8%D1%87)
* [Колыбельников Александр Иванович](http://wikimipt.org/wiki/%D0%9A%D0%BE%D0%BB%D1%8B%D0%B1%D0%B5%D0%BB%D1%8C%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2_%D0%90%D0%BB%D0%B5%D0%BA%D1%81%D0%B0%D0%BD%D0%B4%D1%80_%D0%98%D0%B2%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D1%87)
* [Кшевецкий Александр Сергеевич](http://wikimipt.org/wiki/%D0%9A%D1%88%D0%B5%D0%B2%D0%B5%D1%86%D0%BA%D0%B8%D0%B9_%D0%90%D0%BB%D0%B5%D0%BA%D1%81%D0%B0%D0%BD%D0%B4%D1%80_%D0%A1%D0%B5%D1%80%D0%B3%D0%B5%D0%B5%D0%B2%D0%B8%D1%87)

## Последние релизы (сборки, готовые PDF)
* Релизы в формате PDF: https://github.com/vlsergey/infosec/releases
* Online-версия: https://vlsergey.github.io/infosec/
<sub>(может содержать проблемы вёрстки, см. проект [tex2html](https://github.com/vlsergey/tex2html))</sub>

## Инструкция по сборке
### Установка необходимых компонент

#### Linux (Debian, Ubuntu)
Установка TeXLive и языков:
```
$ sudo apt-get install texlive-latex-base \
    texlive-latex-recommended \
    texlive-latex-extra \
    texlive-science \
    texlive-bibtex-extra \
    texlive-fonts-recommended

$ sudo apt-get install texlive-lang-german \
    texlive-lang-italian \
    texlive-lang-french \
    texlive-lang-european \
    texlive-lang-cyrillic
```

#### OS X:

Скачиваем дистрибутив **MacTeX**: https://www.tug.org/mactex/ (2Gb). Пакета **BasicTeX** будет недостаточно. При установке MacTeX Вы можете отказаться от GUI-программ, чтобы сэкономить место на жестком диске.

#### Windows:

Воспользуйтесь дистрибутивом **MiKTeX**: https://miktex.org/. Большая часть необходимых пакетов будет запрошена к устаровке во время первой сборки (автоматически). Кроме них нужно вручную установить два пакета для поддержки векторых шрифтов в PDF: `cm-super` и `cm-unicode`.

### Клонирование и сборка (Unix)

```
$ git clone https://github.com/vlsergey/infosec
$ cd infosec
$ pdflatex Information\ Security.tex
```
### Cборка (Windows)

```
> pdflatex "Information Security.tex"
```

## Настройки редакторов

### [TeXstudio](https://www.texstudio.org/)

* Default Bibliography Tool: `txs://biber` (`biber.exe %`)
* Default Index Tool: `txs://texindy` (`texindy.exe -M mystyle.xdy -L russian -C utf8 "Information Security.idx"`)

## Какие «ошибки» исправлять не нужно

* При оформлении списков используется правило, что если элементы списка являются предложениями, то перед началом списка не ставится двоеточие (а ставится точка, и все элементы начинаются со строчной буквы).
* Внутри формул, за исключением многострочных, не используется дополнительное оформление даже для удобочитаемости.
* В книге принято, что внутри предложения используется «--» для отделения частей, фамилии в названиях отделяются тремя: «~---~».

## Отличия определений в пособии от [словаря криптографических терминов](https://www.infosystems.ru/upload/iblock/154/slovar.pdf)

| Определение в пособии | Определение в [словаре криптографических терминов](https://www.infosystems.ru/upload/iblock/154/slovar.pdf) | Комментарий |
|---|---|---|
| атака «человек посередине» | атака «противник в середине» | "Человек" ближе к английскому "man", чем "противник". Кроме того термин стал уже общеупотребителен в других источниках. |
| ——— | дешифрование | Чтобы не путать читателей и будущих криптоаналитиков термин «дешифрование» не используется в пособии, чтобы не путать с дословным переводом слова "decipher" — "расшифрование". |
| ключ закрытый | ключ секретный | В пособии термин "ключ секретный" ("secret key") используется только для обозначения ключей шифрования в симметричных криптосистемах. Для асимметричных используется термин "ключ закрытый" ("private key"). |
