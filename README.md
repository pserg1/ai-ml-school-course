# AI/ML для школьников 9-11 классов

22-недельный курс по искусственному интеллекту и машинному обучению для физико-математического лицея.

## 🚀 Как запустить сайт курса на GitHub Pages

### Шаг 1: Создание репозитория

1. Зайдите на [github.com](https://github.com)
2. Нажмите **"New repository"** (зеленая кнопка справа сверху)
3. Заполните:
   - **Repository name:** `ai-ml-school-course`
   - **Description:** "Курс AI/ML для школьников 9-11 классов"
   - **Public** (чтобы GitHub Pages работал бесплатно)
   - ✅ **Add a README file** (можно не ставить, мы загрузим свой)
4. Нажмите **"Create repository"**

### Шаг 2: Загрузка файлов

#### Вариант A: Через веб-интерфейс (проще всего)

1. В вашем новом репозитории нажмите **"Add file"** → **"Upload files"**
2. Перетащите все файлы из скачанной папки `ai-ml-school-course` в окно браузера:
   - `_config.yml`
   - `index.md`
   - `about.md`
   - `README.md`
   - Папки: `slides/`, `notebooks/`, `resources/`, `datasets/`
3. Внизу страницы нажмите **"Commit changes"** (зеленая кнопка)

#### Вариант B: Через GitHub Desktop (если хотите использовать GUI)

1. Скачайте [GitHub Desktop](https://desktop.github.com/)
2. Клонируйте ваш репозиторий
3. Скопируйте все файлы в локальную папку
4. Commit → Push

### Шаг 3: Включение GitHub Pages

1. В репозитории зайдите в **Settings** (вкладка справа сверху)
2. В левом меню выберите **Pages**
3. В разделе **"Source"** выберите:
   - Branch: **main** (или **master**, если так называется ваша ветка)
   - Folder: **/ (root)**
4. Нажмите **Save**
5. Подождите 1-2 минуты

✅ **Готово!** Ваш сайт доступен по адресу:
```
https://YOUR_USERNAME.github.io/ai-ml-school-course/
```

### Шаг 4: Обновление ссылок на Colab

В файле `index.md` замените `YOUR_USERNAME` на ваш реальный username GitHub:

```markdown
[💻 L1](https://colab.research.google.com/github/YOUR_USERNAME/ai-ml-school-course/blob/main/notebooks/week01/lecture01_intro_demo.ipynb)
```

Например, если ваш username `john_doe`, то:
```markdown
[💻 L1](https://colab.research.google.com/github/john_doe/ai-ml-school-course/blob/main/notebooks/week01/lecture01_intro_demo.ipynb)
```

Для редактирования прямо на GitHub:
1. Откройте файл `index.md` в репозитории
2. Нажмите кнопку-карандаш ✏️ (Edit this file)
3. Замените `YOUR_USERNAME`
4. Внизу страницы нажмите **"Commit changes"**

---

## 📁 Структура проекта

```
ai-ml-school-course/
├── _config.yml          # Конфигурация Jekyll
├── index.md             # Главная страница с таблицей курса
├── about.md             # О курсе
├── README.md            # Этот файл
├── slides/              # PDF презентации
│   ├── week01_lecture01_intro.pdf
│   └── ...
├── notebooks/           # Jupyter notebooks для Colab
│   ├── week01/
│   │   ├── lecture01_intro_demo.ipynb
│   │   ├── lecture01_intro_hw.ipynb
│   │   └── ...
│   └── ...
├── resources/           # Дополнительные материалы (ссылки на видео, статьи)
│   ├── week01.md
│   └── ...
└── datasets/            # Наборы данных (если нужны локальные)
    └── ...
```

---

## 📝 Как добавлять новые материалы

### Добавление новой недели

1. **Создайте слайды** в Google Slides
2. **Экспортируйте в PDF:** File → Download → PDF
3. **Загрузите на GitHub:**
   - Зайдите в папку `slides/`
   - Нажмите "Add file" → "Upload files"
   - Загрузите PDF файл (например, `week02_lecture03_span.pdf`)

4. **Создайте Colab notebooks:**
   - Откройте [Google Colab](https://colab.research.google.com/)
   - Создайте новый notebook
   - Добавьте код и описание
   - Сохраните: File → Save a copy in GitHub
   - Выберите репозиторий `ai-ml-school-course`
   - Укажите путь: `notebooks/week02/lecture03_span_demo.ipynb`

5. **Обновите таблицу на сайте:**
   - Откройте `index.md` на GitHub
   - Нажмите кнопку-карандаш ✏️
   - Найдите строку для Недели 2
   - Замените `TBD` на ссылки:
     ```markdown
     | **2** | Span и линейные комбинации | ... | [📝 L3](slides/week02_lecture03_span.pdf) | ...
     ```
   - Commit changes

6. **Добавьте ресурсы:**
   - Создайте файл `resources/week02.md` (аналогично `week01.md`)
   - Добавьте ссылки на видео, статьи, игры

### Быстрое редактирование через веб-интерфейс

- Любой файл можно отредактировать прямо на GitHub:
  1. Откройте файл
  2. Нажмите ✏️ (Edit this file)
  3. Внесите изменения
  4. Commit changes
- Изменения появятся на сайте через 1-2 минуты

---

## 🎓 Для преподавателей

### Советы по созданию Colab notebooks

1. **Demo notebook (с решениями):**
   - Подробные комментарии к коду
   - Визуализации (Matplotlib, Seaborn)
   - Примеры с выводом результатов

2. **Homework notebook (пустой шаблон):**
   - Скопируйте demo
   - Удалите код решения, оставьте только задания
   - Добавьте комментарии: `# TODO: Напишите код здесь`

3. **Структура notebook:**
   ```
   # Неделя 1, Занятие 1: Введение в ИИ
   
   ## Цели занятия
   - Понять, что такое ИИ
   - Создать первую модель
   
   ## 1. Импорт библиотек
   [код]
   
   ## 2. Загрузка данных
   [код]
   
   ## 3. Визуализация
   [код]
   
   ## 4. Задания для самостоятельной работы
   [задания]
   ```

### Сохранение notebooks в GitHub из Colab

1. В Colab: File → Save a copy in GitHub
2. Авторизуйтесь через GitHub (первый раз)
3. Выберите репозиторий: `ai-ml-school-course`
4. Укажите путь: `notebooks/weekXX/lectureXX_topic_demo.ipynb`
5. Commit message: "Add week XX lecture XX demo"
6. ✅ Сохранить

---

## ❓ FAQ

**Q: Как изменить тему сайта?**  
A: В файле `_config.yml` измените `theme: minima` на другую тему (например, `cayman`, `minimal`, `slate`). Полный список: [GitHub Pages themes](https://pages.github.com/themes/)

**Q: Можно ли использовать приватный репозиторий?**  
A: Да, но GitHub Pages для приватных репозиториев доступен только в платном плане GitHub Pro.

**Q: Как добавить свой домен?**  
A: В Settings → Pages → Custom domain укажите ваш домен и создайте файл `CNAME` в корне репозитория.

**Q: Сайт не обновляется?**  
A: Подождите 1-2 минуты после commit. Если не помогло, проверьте вкладку **Actions** в репозитории — там будут ошибки сборки (если есть).

**Q: Как удалить TBD из таблицы?**  
A: Просто замените `TBD` на ссылки на ваши материалы в `index.md`.

---

## 🛠️ Технические требования

- **Для студентов:** Только браузер + Google аккаунт (для Colab)
- **Для преподавателя:** GitHub аккаунт + Google аккаунт

---

## 📧 Контакты

Если у вас есть вопросы или предложения, создайте **Issue** в этом репозитории.

---

**Удачи в обучении! 🚀**
