# 🍰 Random Dessert Bot — n8n Workflow

Этот workflow для [n8n](https://n8n.io) делает следующее:

- ⏰ Запускается по таймеру каждые **5 секунд**
- 🌐 Делает GET-запрос к API [`spoonacular.com`](https://spoonacular.com/food-api) для получения **случайного десертного рецепта**
- 📷 Отправляет изображение, название и ссылку на рецепт в указанный **Telegram-чат**

---

![image](https://github.com/user-attachments/assets/072cc1e4-ace4-4e4d-905b-a89ae8af99c2)

---

## 🔧 Структура Workflow

```mermaid
graph TD
  A["Schedule Trigger"] --> B["HTTP Request"]
  B --> C["Telegram sendPhoto"]
