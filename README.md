# KotoScience

## Опис проекту
Проект представляє собою Computer Vision модель з веб-формою для отримання даних.
Ціль проекту - створити модель, що зможе розпізнавати та визначати вид тварини за фото
наданим через веб-форму. Користувач також зможе отримати довідку за розпізнаним видом.

## Актуальність проекту
Актуальність нашого продукту полягає в тому, що продукти з схожим функціоналом платні або обмежені операційною системою.  
За допомогою веб-ресурсу, кожен користувач зможе дізнатись певну інформацію про тварину на зображенні.

## Функціонал продукту
Після того як користувач потрапив до веб-ресурсу, він має можливість завантажити зображення.
Далі, зображення класифікується і якщо зображення належить до якогось з відомих класів, то користувач отримує коротку довідку про даний клас тварин.
Якщо ж зображення було класифіковане як "невідоме", користувач отримує відповідне повідомлення, також йому буде запропоновано спробувати завантажити інше зображення.

## Стек технологій

**Python**

`Python` наразі є однією з найпопулярніших мов програмування, причинами цього стали:
* Простий та легкий синтаксис.
* Швидкість розробки. На перший погляд, це не так вже і важливо, але час розробника – це гроші замовника. Корпорації на кшталт Google та Apple вже майже десятиліття більшість своєї внутрішньої розробки ведуть, використовуючи цю мову.
* Спільнота. Любов до цієї мови зі сторони розробників створила величезну групу прихильників, яка активно підтримує перспективні проєкти, фреймворки, відповідає на складні питання на StackOverFlow, та розвиває мову.
* Універсальність. Ця мова на сьогодні є дуже гнучкою: за допомогою неї, можна навчати дітей програмуванюю, створювати веб-додатки, сервіси, тестувати сайти чи програми, використовувати машинне навчання та програмувати пристрої для Internet Of Things.

Якщо в інших сферах можливо знайти якісь альтернативи, то для задач машинного навчання `Python` посідає перше місце. Так, для статистики та деяких задач існує чудова мова `R`. Але для запуску програмного продукту ця мова не згодиться. Тому `Python` мова, яку однаково зручно використовувати, як для початкового концепту, так і для фінального. Google та Microsoft використовують цю мову як основну у задачах машинного навчання.

**PyTorch**

`PyTorch` - це бібліотека, написана мовою `Python`, що забезпечує тензорні обчислення з GPU-прискоренням, подібно до `NumPy`. `PyTorch` пропонує насичений API для вирішення прикладних завдань, пов'язаних з нейронними мережами. Перевагами цієї бібліотеки є:
* Динамічний граф. В порівняні з `TensorFlow`, яка використовує статичний граф, `PyTorch` використовує техніку, звану автодиференціацією у зворотному режимі, яка дозволяє змінювати спосіб поведінки мережі з прикладанням відносно невеликих зусиль, тобто динамічний обчислювальний граф або DCG.
* Налагодження. Так як обчислювальний граф визначається під час виконання програми, є можливість використовувати будь-який інструмент налагодження: `pdb`, `ipdb`, `PyCharm`.
* Паралелізм даних. Використовуючи `torch.nn.DataParallel` з будь-яким модулем можна домогтися майже магічного паралелізму даних за розміром батча.
* Візуалізація. Існує інтеграція з `Tensorboard`, проте для простішого використання з меншим функціоналом є `visdom`. Крім названих інструментів, можна використовувати стандартні засоби візуалізації - `matplotlib` і `seaborn`.

**FastAPI**

`FastAPI` - це сучасний та продуктивний фреймворк (доступний з версіями `Python` 3.6+). Він може обробляти як синхронні, так і асинхронні запити, а ще містить вбудовану підтримку валідації даних, серіалізації JSON, автентифікації та авторизації, а також OpenAPI-документації.`FastAPI` має наступні особливості:
* Швидкий. Оскільки асинхронна модель набагато продуктивніша за традиційну синхронну, фреймворк може позмагатися з Node та Go в продуктивності.
* Його розробники надихались Flask, тож FastAPI містить легкий мікрофреймворк з підтримкою декораторів, подібних на Flask-роути.
* Використовує переваги підказок типів у Python для оголошення параметрів, що дозволяє робити валідацію (через Pydantic) та створювати OpenAPI/Swagger-документацію.
* Створений на базі Starlette, підтримує розробку асинхронних API.
Порівнюючи даний фреймворк з `Flask`, ми звернули на головну первагу `FastAPI` - швидкість. Саме цей параметр став вирішальним, оскільки нейронна мережа досить ресурсно затратна важливо було не створювати додаткове навантаження, якщо це можливо. Також `FastAPI` є більш сучасним фреймворком і використовується передовими компаніями у проектах пов'язаних з задачами машинного навчання.

## Timeline

![timeline](https://github.com/shooterdimon/KotoScience/blob/main/timeline/timeline.png)
