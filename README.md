# AI-копирайтер для автоматической публикации статей на сайт

Этот кейс про ИИ-ассистента, который пишет статьи, генерирует изображения, title, description и публикует материалы на сайте. Весь процесс можно автоматизировать или управлять вручную, проверяя и редактируя тексты перед публикацией.

**Точка "А"**

Это личный проект. Я давно занимаюсь сайтами: создаю, развиваю, монетизирую. Один из новых — сайт про собак. Обычная ситуация: заполнила его десятком статей, но быстро поняла, что для нормального трафика контента нужно гораздо больше. Самой писать — долго, дешёвые копирайтеры делают некачественные тексты, а дорогие невыгодны для нового проекта. В таком режиме на сайте появлялась максимум одна статья в день.

**Решение:** создать ИИ-ассистента, который возьмёт на себя написание статей, автоматическую генерацию заголовков и описаний, создание изображений и загрузку материалов на сайт в виде черновиков.

![image](https://github.com/user-attachments/assets/65502ee4-e222-4b5c-acf3-e219593d9981)

**Процесс работы**

**Сбор тем и ключевых слов**

Я собрала ключевые слова, а затем через ChatGPT сформировала к ним темы. Многие статьи требуют специализированной информации, например, по ветеринарии. В будущем ИИ-ассистент сможет обрабатывать такие темы, но для старта я выбрала те, которые не требуют сложных источников. Получилось около 100 тем, которые я занесла в Google-таблицу. Они использовались как заголовки и включались в title, description и первый абзац статьи.

![image](https://github.com/user-attachments/assets/0f9a2cb8-ec63-4e04-a022-61fad5e602c6)

**Создание базы знаний**

Для обучения ИИ я проанализировала уже опубликованные статьи, выявила основные шаблоны структуры и стиль написания. Все материалы начинались с вводного абзаца с описанием проблемы, имели 3–5 подзаголовков и завершались выводами с рекомендациями.

Я подготовила:

- Шаблоны структуры статей. Выбрала единый формат для первых 100 публикаций.
- Примеры текстов. Собрала лучшие статьи и обучила ИИ их стилю.
- Техническое задание. Описала требования к текстам, включая логику их построения.

**Настройка ИИ**

Вся система была связана через инструменты Make.com. Отдельного ассистента в OpenAI Assistants Playground я не создавала. Системный промт прописала в Make. ИИ поочерёдно брал темы из Google-таблицы и писал статьи, соблюдая заданную структуру и стиль. Автоматически генерировались title, description и отрывок с ключевыми мыслями. Затем создавалась основная картинка через DALL-E. Вся работа была интегрирована с CMS WordPress: статьи загружались в виде черновиков, что позволяло проверять их перед публикацией. 

![image](https://github.com/user-attachments/assets/f0a860a1-5fb2-489f-8a82-2f899a3661fc)


![image](https://github.com/user-attachments/assets/e03ba9b0-5206-4df5-a771-b1547dcc1080)

**Что не удалось**

DALL-E не всегда создавал точные изображения: примерно в 2–3 случаях из 10 картинки приходилось переделывать. В будущем планирую заменить её на Midjourney. Также первые версии статей были короче, чем требовалось. После корректировки требований по объёму и добавления ИИ-редактора этот вопрос удалось решить.

**Результаты**

- Частота публикаций: вместо 1 статьи в день теперь возможно автоматически генерировать новые каждые 15 минут. При ручном редактировании выходит 3–5 статей в день.
- Качество текстов: 80% публикаций без значительных правок.

**Итог**

ИИ-копирайтер оказался значительно дешевле и продуктивнее автора с биржи. В дальнейшем планирую доработать его так, чтобы он мог писать сложные статьи с экспертными данными, а также использовать нейросеть, которая не будет рисовать шпицев с пятью хвостами. 😆
