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
- div.common_popup - попап для інших цілей
- div.notification_popup
- div.auth_popup
*
Функції:
showNotification(content:html) показати інформаційний попап (зникає через 2сек)
openPopup(popupId:string, content:html) показати попап з контентом
# Авторизація
Значок юзера в шапці ```<div class='user'> ``` якщо залогінений то в ```<a>``` вставити посилання на кабінет, якщо не залогінений то до ```<a>``` додати клас ''' go-auth '''
