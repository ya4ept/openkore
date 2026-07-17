# Примеры оформления MkDocs

## Выделение текста

**Жирный текст**
```
**Жирный текст**
```
<u>Подчёркнутый текст</u>
```
<u>Подчёркнутый текст</u>
```
_Курсив_
```
_Курсив_
```

## Заметки

!!! notes "Заметка"
    Текст заметки
```
!!! notes "Заметка"
    Текст заметки
```

??? example "пример"
    пример чего-нибудь
```
??? example "пример"
    пример чего-нибудь
```
!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack)
```
!!! tip ""
    Category: [config.txt](/cat/config.txt) | [attack](/cat/config.txt-attack)
```
## Иконки

| Иконка          | Текст             |
| --------------- | ----------------- |
| :simple-github: | `:simple-github:` |

## Ссылки

ссылка с предпросмотром: [`<boolean>`](References.md#boolean_flag){ data-preview }
```
[`<boolean>`](References.md#boolean_flag){ data-preview }
# если файл References.md находится выше в директории, то указать путь: ..\References.md#boolean_flag
```

## Использование шаблона

Вставить текст со страницы:

--8<-- "template/OnlyWhenAiAuto.md"
`--8<-- "template/OnlyWhenAiAuto.md"`
