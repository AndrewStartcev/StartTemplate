# Базовый шаблон для верстки

Базовый шаблон для верстки с настроенной gulp сборкой

### Используемые технологии

Html, JavaScript, Gulp, Node, scss

### Установка

Рекомендуемая среда разработки - VS Code.
Предварительно установите Node.js (https://nodejs.org/en/) и gulp (https://gulpjs.com/).
Затем в консоли пропишите:

```bash
cd gulp
npm i
```

### Запуск

```bash
cd gulp
```

```bash
gulp
```

### Настройка контейнера

Переменные:

> app/scss/\_base.scss

```
$maxWidth: 1920; // Не меняем.
$maxWidthContainer: 1200; // Максимальный размер контейнера
$md1: $maxWidthContainer + 10; // Адаптив контейнера, когда экран меньше чем 1200
$md2: 767.98; // Переход адаптива с планшета в мобильное состаяние
```

Разметка:

> app/scss/\_grid.scss

```
.container {
	max-width: $maxWidthContainer + px;
	width: 100%;
	margin: 0 auto;
	@media (max-width: ($md1+px)) {
		max-width: 768px;
		padding: 0 30px;
	}
	@media (max-width: ($md2+px)) {
		max-width: 100%;
		padding: 0 10px;
	}
}
```

В дальнейшем медеа запросы можно использовать с переменными

```
@media (max-width: ($md2+px)) // {} 1200 - 768
@media (max-width: ($md2+px)) // {} 768 - 320
```
