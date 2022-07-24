
# Code guide Дизайн студии IDEI

## Содержание

### [Автоматическая проверка кода](#автоматическая-проверка-кода)
### [CSS](#css)
- [Структура объявления](#структура-объявления)
- [Имена классов](#имена-классов)
- [Пробелы между комбинаторами](#пробелы-между-комбинаторами)
- [Кавычки](#кавычки)
- [Порядок свойств](#порядок-свойств)
## Автоматическая проверка кода

- Для поддержания единообразия в коде используется [EditorConfig](https://github.com/VafinArtem/ideicodeguide/blob/main/.editorconfig).
- Для автоформатирования кода можно использовать [prettier](https://github.com/VafinArtem/ideicodeguide/blob/main/.prettierrc)
- Для стилей Stylelint.

Все настройки уже находятся в проектах.
## CSS
### Структура объявления

- Перед открывающейся фигурной скобкой стоит пробел. После скобки запись идёт с новой строки.
- Свойства стоят на отдельных строках.
- Свойства внутри блока имеют один внутренний отступ в виде таба состоящего из двух пробелов.
- Между модификаторами, миксинами, вложенными селекторами внутри блока есть одна пустая строка.
- После двоеточия стоит пробел. Перед двоеточием пробел не нужен.
- В конце объявления стоит точка с запятой.
- Закрывающая скобка стоит на новой строке и без отступа.
- Между блоками правил есть одна пустая строка.

Примеры:

```css
/* Хорошо */
.block {
  @include btn-reset;
  
  margin-bottom: 0;
  margin-top: 0;
  font-size: 14px;
  line-height: 20;
  color: #ff0000;

  &--black {
    color: #000;
  }

  & .element {
    background-color: #ffffff
  }
}

.element {
  background-color: #000000;
}

/* Плохо */
.block{@include btn-reset;
margin-bottom: 0;
    margin-top: 0;
  font-size: 14px;line-height: 20;
  color :#ff0000
  &--black {
    color: #000;
  }& .element {
    background-color: #ffffff
  }}
.element {
  background-color: #000000;
}
```
### Имена классов

- Имена классов записаны строчными буквами.
- Для написания классов использованы английские слова и термины. В названиях классов и атрибутов нет транслита.

Примеры:

```css
/* Хорошо */
.alert-danger { … }
.tweet .user-picture { … }
.button { … }
.layout-center { … }

/* Плохо */
.testElement { … }
.t { … }
.big_red_button { … }
.knopka { … }
```
### Пробелы между комбинаторами

- До и после комбинатора между селекторами стоит один пробел.

Примеры

```css
/* Хорошо */
h2 + h3 {}
ul > li {}

/* Плохо */
h2+h2 p{}
ul >li {}
```
### Кавычки

- Во всех случаях в стилях использованы двойные кавычки.
- В необязательных случаях кавычки не опущены.

Примеры:

```css
/* Хорошо */
.field[type="text"] {
  background-image: url("images/cat.jpg");
}

/* Плохо */
.field[type=text] {
  background-image: url(images/cat.jpg);
}
```
### Порядок свойств

Объявления логически связанных свойств сгруппированы в следующем порядке:

1. Позиционирование
2. Блочная модель
3. Типографика
4. Оформление
5. Анимация
6. Разное

В проектах используется Stylelint, который помогает в этом.

Примеры: 

```css 
.declaration-order {
  /* Позиционирование */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;

  /* Блочная модель */
  display: block;
  float: right;
  width: 100px;
  height: 100px;
  margin: 10px;
  padding: 10px;

  /* Типографика */
  font-family: "Arial", sans-serif;
  font-style: normal;
  font-size: 13px;
  line-height: 20px;
  font-weight: 700;
  text-align: center;
  color: #333333;

  /* Оформление */
  background-color: #f5f5f5;
  border: 1px solid #e5e5e5;
  border-radius: 3px;
  opacity: 1;

  /* Анимация */
  transition: color 1s;

  /* Разное */
  will-change: auto;
}
```
## Авторы

[@ArtemVafin](https://www.github.com/ArtemVafin)


## Благодарность

[Htmlacademy.ru](https://htmlacademy.ru) за их [codeguide](https://codeguide.academy/).
## Лицензия

[MIT](https://choosealicense.com/licenses/mit/)

