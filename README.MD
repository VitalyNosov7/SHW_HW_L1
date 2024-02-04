# Домашнее задание к Уроку 1. ASP.NET база
---
Доработайте контроллер, дополнив его возможностью удалять группы и продукты, а также задавать цены. Для каждого типа ответа создайте свою модель.

---

# Решение:

В контроллере ProductController.cs (строки 68-73) реализован метод DeleteProduct(int id), который позволяет удалить продукт по Id продукта. 


```
        [HttpDelete]
        [Route("products")]
        public void DeleteProduct(int id)
        {
            storeContext.Products.Where(p => p.Id == id).ExecuteDelete();
        }

```