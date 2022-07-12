# syto
# Продукти. каталог
Може мати 4 стани.
* до  ```<div class='catalog-item'> ``` додається такі можливі класи:  
  - stock -знижка,
  -  best - найкраща проп. 
  -  hot - гаряча проп. 
  -  new - новинка
# Продукти. сторінка продукту
```div.catalog-item ``` ідентичний тому що на сторінці каталог
# Попапи
*мають бути на кожній сторінці:
- div.search-mobile-form - пошук
- div.question_popup_form - форма задати питання
- div.cart-popup - форма корзини
- div.notification_popup - великий попап для відображення повідомлень
- div.auth_popup - попап авторизації
- div.common_popup - попап для інших цілей
*
Функції:
- showNotification(content:html) показати стилізований інформаційний попап зі змінним контентом (зникає через 2сек)
- showSmallMessage(msg:string, status:[error, success]) показати маленький попап про успіх чи помилку з деяким текстом
- showAddToCartPopup(productName:string) показати повідомлення про додавання товару в кошик
- openPopup(popupId:string, content:html) показати простий попап з контентом 
# Авторизація
Значок юзера в шапці ```<div class='user'> ``` якщо залогінений то в ```<a>``` вставити посилання на кабінет, якщо не залогінений то до ```<a>``` додати клас ''' go-auth '''
