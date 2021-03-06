# DOC
## Используемые библиотеки:
1. jQuery
1. Fancybox - попапы, галерея
1. Slick.js - слайдеры
1. noUiRange - ползунки-переключатели
1. jquery-circle-progress - для отрисовки прогресса круга

## Компоненты
### Контейнер
Класс создания `case`
|Точка|Размер|
|:-:|:-:|
|>1500px|1470px|
|<=1500px|1170px|
|<=1199px|950px|
|<=992px|740px|
|<=767px|100%|

### Сетка
Отсутствует. Колоночная ориентация сделана по средству задания родителю колонки класса `row`, который является флексбоксом.

### Кнопка
Класс создания `btn`

Модификаторы

|Класс|Свойства|
|:-:|:-:|
|.--white|Белый цвет|
|.--yellow|Жёлтый цвет|
|.--blue|Синий цвет|


### Текстовое поле (инпут)
Класс создания `input`

Модификаторы

|Класс|Свойства|
|:-:|:-:|
|.--md|Высота 40px|
|.--b-gray|Серая рамка; загругленные углы|
|.--filter|Высота 35px; отсутствие загругленных углов; серая рамка|
|.--subscribe|Высота 50px; прозрачный задний фон; белая рамка|
|.--focus-c-blue|При фокусе задается голубой цвет|
|.--error|Рамка красного цвета|

### Селект (выпадающий список)
Класс создания `select`

Не имеет модификаций.

Структура генерируется на стороне JavaScript.

Принимает в себя стандартный тег `select` и его структуру. Для правильного отображения и работы всем вложенным тегам "option" необходимо задавать значение в атрибут "value". 

Для создания стандартного заголовка выпадающему списку, тегу "select" необходимо задать атрибут `data-placeholder=""`

При открытии добавляется класс `--open`


### Чекбокс
Для создания должен иметь классы `checkbox` и `check`

При клике добавляется/убирается класс `--checked`, а внутреннему инпуту добавляется/убирается атрибут `checked="checked"`

**Структура**
```
	<div class="checkbox check">
		<input class="checkbox__input" type="checkbox" name="nameCheckbox">
		<label class="checkbox__label">Чекбокс</label>
	</div>
```

### Радио
Для создания должен иметь классы `radio` и `rad`

При клике добавляется класс `--checked`, у его "соседей", которые берутся из атрибута `name=""` он убирается.

```
<div class="radio rad">
	<input class="radio__input" type="radio" name="nameCheckbox" value="€">
	<div class="radio__wrap">
		<div class="radio__title">Радио</div>
	</div>
</div>
```



### Табы

Структура
```
<div class="tabs">
	<div class="tabs-links">
		<a href="#tab-1" class="tabs-link">Ссылка 1</a>
		<a href="#tab-2" class="tabs-link">Ссылка 2</a>
		<a href="#tab-3" class="tabs-link">Ссылка 3</a>
	</div>
	<div class="tabs-list">
		<div id="#tab-1" class="tabs-item">Таб 1</div>
		<div id="#tab-2" class="tabs-item">Таб 2</div>
		<div id="#tab-3" class="tabs-item">Таб 3</div>
	</div>
</div>
```

Для обращения к табу, ссылке необходимо добавить атрибут `href` с идентификатор необходимого таба

Все ссылки должны иметь родителя с классом `tabs-links`
