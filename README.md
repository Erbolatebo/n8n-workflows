# 🍰 Random Dessert Bot — n8n Workflow

Этот workflow для [n8n](https://n8n.io) делает следующее:

1. ⏰ Запускается по таймеру каждые **5 секунд**
2. 🌐 Делает GET-запрос к API [`spoonacular.com`](https://spoonacular.com/food-api) для получения **случайного десертного рецепта**
3. 📷 Отправляет изображение, название и ссылку на рецепт в указанный **Telegram-чат**

---

![image](https://github.com/user-attachments/assets/0fc67522-20c7-4428-8181-7b1f61c51a8c)

---

## 🔧 Структура Workflow

```mermaid
graph TD
  A[Schedule Trigger] --> B[HTTP Request (Spoonacular API)]
  B --> C[Telegram: sendPhoto]

