# testovoeDragAndDrop

## Description

### Task

Задача: сделать рабочую страницу с изображения.

Дизайн не требуется. Достаточно схематичной страницы, как на изображении.

Блоки снизу:
Слева - вещи у пользователя
Справа - вещи на выбор

Блоки сверху:
Слева - выбранные вещи из вещей пользователя (блок снизу-слева)
Справа - выбранная вещь из вещей на выбор (блок снизу-справа).

Объекты вещей имеют одинаковую структуру, отличаются только названием и номером.

### Mechanics of work

Снизу-справа можно выбрать одновременно только 1 вещь, которая должна отображаться справа-сверху.

Снизу-слева можно выбрать от 1 до 6 вещей, которые должны отображаться в верхней левой части в порядке выбора.

### Additional features

Draggable для перетаскивания в нижних блоках из левого массива в правый

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
