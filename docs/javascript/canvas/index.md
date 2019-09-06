# Javascript свойства и методы элемента canvas

HTML5 тег `<canvas>` используется для отображения графики на лету при помощи скриптов (обычно JavaScript).

Тем не менее, сам по себе элемент `<canvas>` не имеет инструментария для рисования. Это всего лишь контейнер для графики. Чтобы в действительности что-то нарисовать в элементе `<canvas>`, необходимо использовать соответствующий скрипт.

Метод `getContext()` возвращает объект, предоставляющий методы и свойства для рисования в элементе `<canvas>`.

В данном справочнике приводится информация о свойствах и методах объекта `getContext("2d")`, который может использоваться для вывода в элементе `<canvas>` текста, линий, прямоугольников, кругов и др.

Internet Explorer 9, Firefox, Opera, Chrome и Safari поддерживают элемент `<canvas>` и его свойства и методы. Internet Explorer 8 и более ранние версии не поддерживают элемент `<canvas>`.

## Цвета, стили, тени

Свойства:

`fillStyle`
: Устанавливает/возвращает цвет, градиент или шаблон, используемый для заливки графического объекта

`shadowBlur`
: Устанавливает/возвращает уровень размытости для теней

`shadowColor`
: Устанавливает/возвращает цвет для теней

`shadowOffsetX`
: Устанавливает/возвращает горизонтальное расстояние тени от фигуры

`shadowOffsetY`
: Устанавливает/возвращает вертикальное расстояние тени от фигуры

`strokeStyle`
:Устанавливает/возвращает цвет, градиент или шаблон, используемый для обводки фигуры

Методы:

`addColorStop()`
: Определяет цвета и позицию остановки в объекте градиента

`createLinearGradient()`
: Создает линейный градиент (для использования с содержимым элемента `<canvas>`)

`createPattern()`
: Размножает заданный элемент в заданном направлении

`createRadialGradient()`
: Создает радиальный/круговой градиент (для использования на содержимом элемента `<canvas>`)

## Стили линий

Свойства:

`lineCap`
: Устанавливает/возвращает стиль концов нарисованной линии

`lineJoin`
: Устанавливает/возвращает тип угла, созданного пересечением двух линий

`lineWidth`
: Устанавливает/возвращает ширину текущей линии

`miterLimit`
: Устанавливает/возвращает максимальную длину среза

## Прямоугольники

Методы:

`clearRect()`
: Очищает заданную область пикселей внутри данного прямоугольника

`fillRect()`
: Рисует "залитый" прямоугольник

`rect()`
: Создает прямоугольник

`strokeRect()`
: Рисует прямоугольник (без заливки)

## Контуры

Методы:

`arc()`
: Создает дугу/кривую (используется для создания окружностей или их части)

`arcTo()`
: Создает дугу/кривую между двумя касательными

`beginPath()`
: Начинает контур или сбрасывает текущий контур

`bezierCurveTo()`
: Создает кубическую кривую Безье

`clip()`
: Обрезает область любой формы и размера, находящуюся вне указанного контура

`closePath()`
: Замыкает контур соединяя последнюю точку с первой

`fill()`
: Делает заливку текущей фигуры (контура)

`isPointInPath()`
: Возвращает значение `true`, если заданная точка находится внутри текущего контура, в обратном случае возвращается значение `false`

`lineTo()`
: Добавляет новую точку контура и создает линию к этой точке от последней заданной точки

`moveTo()`
: Передвигает точку контура в заданные координаты не рисуя линию

`quadraticCurveTo()`
: Создает квадратичную кривую Безье

`stroke()`
: В действительности рисует определенный вами контур

## Трансформации

Методы:

`rotate()`
: Поворачивает текущий графический объект

`scale()`
: Изменяет масштаб текущего графического объекта

`setTransform()`
: Сбрасывает текущую матрицу трансформации в начальное состояние, а затем вызывает метод `transform()` с теми же параметрами

`transform()`
: Применяет заданную матрицу трансформации

`translate()`
: Ретранслирует позицию `(0,0)` в новое место

## Текст

Свойства:

`font`
: Устанавливает/возвращает свойства шрифта для текстового содержимого

`textAlign`
: Устанавливает/возвращает выравнивание для текстового содержимого

`textBaseline`
: Устанавливает/возвращает базовую линию, используемую при выводе текста

Методы:

`fillText()`
: Рисует текст с заливкой

`measureText()`
: Возвращает объект, содержащий ширину заданного текста

`strokeText()`
: Рисует текст без заливки

## Вывод изображений

Методы:

`drawImage()`
: Рисует изображение, содержимое другого элемента `<canvas>` или видео

## Пиксельные манипуляции

Свойства:

`data`
: Возвращает объект, содержащий данные изображения заданного объекта `ImageData`

`height`
: Возвращает высоту объекта `ImageData`

`width`
: Возвращает ширину объекта `ImageData`

Методы:

`createImageData()`
: Создает новый, пустой объект `ImageData`

`getImageData()`
: Возвращает объект `ImageData`, который копирует пиксельные данные заданной прямоугольной области холста

`putImageData()`
: Помещает данные изображения (из заданного объекта `ImageData`) обратно в элемент `<canvas>`

## Компоновка

Свойства:

`globalAlpha`
: Устанавливает/возвращает текущее значение прозрачности или альфа-канала графического объекта

`globalCompositeOperation`
: Устанавливает/возвращает то, как исходное (новое) изображение нарисовано на целевом (существующем) изображении

## Другое

Методы:

`save()`
: Сохраняет состояние текущего контекста

`restore()`
: Возвращает ранее сохраненное состояние и атрибуты

`createEvent()`

`getContext()`

`toDataURL()`