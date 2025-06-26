# 🍰 Random Dessert Bot — n8n Workflow

Этот workflow для [n8n](https://n8n.io) делает следующее:

1. ⏰ Запускается по таймеру каждые **5 секунд**
2. 🌐 Делает GET-запрос к API [`spoonacular.com`](https://spoonacular.com/food-api) для получения **случайного десертного рецепта**
3. 📷 Отправляет изображение, название и ссылку на рецепт в указанный **Telegram-чат**

---

## 🔧 Структура Workflow

```mermaid
graph TD
  A[Schedule Trigger] --> B[HTTP Request (Spoonacular API)]
  B --> C[Telegram: sendPhoto]

![image](https://github.com/user-attachments/assets/b192dad9-87a5-41de-88e8-099a3299b758)
