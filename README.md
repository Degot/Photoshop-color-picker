Photoshop-color-picker
======================


Требования:

Браузер с поддержкой canvas.
Подключить colorPicker.js и colorPicker.css.
Подключить jQuery (тестировалось на 2.0.0, но вероятно заработает и на младших версиях).
Подключить jQuery UI разделы core, widget, mouse, slider (тестировалось на 1.9.2).

Подключение css и изображений от jQuery UI не требуется. Всё что нужно уже включено в colorPicker.css.


Использование:

Разместить тег с любым id в теле страницы, например <div id='cPicker'></div>.

Вызвать функцию создания объекта
var newPicker = new createColorPickerOjb('cPicker', 1, 128, 128, 128, function() {
	console.log( newPicker.getHEX() );
});


Параметры создания:
createColorPickerOjb(id, selectTab, r, g, b, onChange):
id - идентификатор тега где будет создан color picker,
selectTab - номер активной вкладки (1 - цвет; 2 - образцы),
r, g, b - цвет по умолчанию в формате RGB,
onChange - функция, которая будет выполняться при изменении цвета.


Публичные методы:
Доступны для вызова через созданный объект.
getHEX() - возвращает строку с цветом в формате HEX, пример '#385ea8'.
getRGB() - возвращает массив с цветом в формате RGB, пример [15, 30, 25].
setHEX(hex) - устанавливает переданный цвет в формате HEX, пример setHEX('#385ea8') или setHEX('385ea8').
setRGB(r, g, b) - устанавливает переданный цвет в формате RGB, пример setRGB(15, 30, 25).