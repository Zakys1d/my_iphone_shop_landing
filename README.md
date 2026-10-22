# My iPhone Shop

Интернет-магазин техники Apple (телефоны, планшеты, аксессуары) на React и TypeScript.

[DEMO LINK](https://zakys1d.github.io/my_iphone_shop_landing/)

## Возможности

- Главная страница со слайдером баннеров, карточками категорий и подборками товаров
- Каталог по категориям: `phones`, `tablets`, `accessories`
- Сортировка, пагинация и поиск по товарам (параметры хранятся в URL)
- Страница товара: выбор цвета и объёма, характеристики, рекомендации
- Корзина и избранное с сохранением в `localStorage`
- Переключение светлой и тёмной темы
- Страницы «не найдено» и состояния загрузки и ошибок

## Технологии

- React 18+, React Router (`HashRouter`)
- TypeScript
- Vite
- SCSS Modules, classnames
- ESLint, Stylelint, Prettier (конфиги Mate Academy)

## Запуск

```bash
npm install
npm start
```

Остальные команды:

| Команда           | Что делает                                   |
| ----------------- | -------------------------------------------- |
| `npm start`       | Dev-сервер Vite                              |
| `npm run build`   | Проверка типов и сборка в `dist/`            |
| `npm run preview` | Локальный просмотр собранного проекта        |
| `npm run lint`    | Линтеры (`mate-scripts lint`)                |
| `npm test`        | Линтеры и тесты                              |
| `npm run deploy`  | Сборка и публикация на GitHub Pages          |

## Структура проекта

```
public/            статика: img/, fonts/, api/*.json (данные товаров)
src/
  api/             запросы к JSON-файлам с кэшем
  components/      переиспользуемые UI-компоненты
  context/         корзина, избранное, тема
  hooks/           useLocalStorage, useRequest, useDebouncedCallback
  modules/         страницы: Home, Category, ProductDetails, Cart, Favorites, NotFound
  styles/          глобальные стили и шрифты
  types/           типы Product, ProductDetails, CartItem и др.
  utils/           пагинация, параметры поиска, цвета
```

## Данные

Товары загружаются из статических файлов `public/api/` (`products.json`, `phones.json`, `tablets.json`, `accessories.json`), изображения лежат в `public/img/`. Бэкенд не нужен.
