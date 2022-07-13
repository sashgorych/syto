# syto
# Товари
Товар може мати 4 стани.
* до  ```<div class='catalog-item'> ``` додається такі можливі класи:  
  - stock -знижка, + в ```<div class='prev-price'>``` додати попередню ціну
  -  best - значок найкраща пропозиція. 
  -  hot - значок гаряча пропозиція. 
  -  new - значок новинка
# Сторінка товару
*product-item.html 
Вставляється без змін айтем з каталогу. тобто ```div.catalog-item ``` ідентичний тому що на сторінці каталог

# Каталог товарів
  *catalog.html  
  - одна окрема секція з товарами це ``` <div class='catalog-list-container'>```
  - всередині цьої секції товари:
    - можуть виводитись плиткою. див. ```<div class='catalog-list'> ```
    - можуть виводитись слайдером. див. ```<div class='catalog-list slider'> ```
# Авторизація
Значок юзера в шапці ```<div class='user'> ``` якщо залогінений то в ```<a>``` вставити посилання на кабінет, якщо не залогінений то до ```<a>``` додати клас ''' go-auth '''  
``` div.auth_popup ``` попап з формами входу і реєстрації
# Кабінет
cabinet.html  
Складається з таких блоків:
- ```div.cabinet-info ``` інформація про користувача. при кліку на кнопку 'змінити дані' перекидує на сторінку з формою для зміни даних cabinet-change-user-data.html 
- ```div.cabinet-history ``` історія замовлень. Розмітка самої таблички ``` div.cart-table``` ідентична тій що в кошику, окрім останньої колонки з кнопкою 'повтор'. При кліку на цю кнопку позиція з цього 'попереднього замовлення' потрапляє в кошик.
- ```div.catalog-list-container ``` товари, виводяться слайдером
# Кошик
```<div class='cart-popup'> ```  
При кліку на кнопку 'придбати' на товарі викликати функцію showAddToCartPopup(назва продукту:string) - показати повідомлення про додавання в кошик  
У колонці 'Знижка' вивести розмір знижки або прочерк  
У колонці 'Кількість' ```div.counter ``` (чому він тільки тут хз) взятий з туркофі - відповідно функціонал підтягнути з туркофі.  
Після кліку на 'придбати' викликати функцію afterCartMsg(msg:string with html) - показує попап про успіх замовлення. msg по дефолту текст українською. Приклад msg: '<p>success</p>'
# Кнопки
 в більшості кнопок ```div.default-button ``` всередині є ```<div class='loading-indicator-div' style='display:none;'> ```. Якщо потрібно показати імітацію завантаження після кліку - змінити на display:block;  
 Приклад див. в кошику
# Попапи
*мають бути на кожній сторінці:
- div.search-mobile-form - пошук
- div.question_popup_form -  задати питання
- div.cart-popup - корзина
- div.notification_popup - великий попап для відображення повідомлень
- div.auth_popup - попап авторизації
- div.common_popup - попап для інших цілей
*
Функції:
- showNotification(content:string with html) показати стилізований інформаційний попап зі змінним контентом (зникає через 2сек)
- showSmallMessage(msg:string, status:[error, success]) показати маленький попап про успіх чи помилку з деяким текстом
- showAddToCartPopup(productName:string) показати повідомлення про додавання товару в кошик
- openPopup(popupId:string, content:string with html) показати простий попап з контентом 
# Контент сторінка
default-page.html - стандартна розмітка для сторінок, які можуть знадобитися в процесі розробки


