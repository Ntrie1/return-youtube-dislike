Read this in other languages: [English](SECURITY-FAQ.md), [русский](SECURITY-FAQru.md), [Français](SECURITY-FAQfr.md), [Türkçe](SECURITY-FAQtr.md), [Polski](SECURITY-FAQpl.md), [Deutsch](SECURITY-FAQde.md), [العربية](SECURITY-FAQar.md), [Bahasa Indonesia](SECURITY-FAQid.md), [中文](SECURITY-FAQcn.md), [български](SECURITY-FAQbg.md)

# Безпека

### Ви відстежуєте мою історію переглядів?

Ні. Код розширення знаходиться у відкритому доступі, і ви можете ознайомитись з ним самостійно. Єдина інформація, що передається - це ID відео, який необхідний для отримання даних про кількість відміток. Жодних додаткових заголовків не передається. На комунікаційному рівні серверу буде передано вашу публічну IP-адресу, а також час, коли було зроблено запит. Однак ніщо з цього ніяк не здатно вас ідентифіквати. Припускаючи середовище з нульовою довірою, найцінніше, що ми можемо отримати це динамічний IP. Який сьогодні ваш, а завтра – вашого сусіда. Якщо ви дійсно турбуєтеся про те, що ваш IP може бути відстежений, ви, ймовірно, вже використовуєте якийсь VPN.

### Чи можете ви однозначно ідентифікувати мене, коли я залишаю відмітку «Не подобається»?

Так. Коли ви залишаєте відео позначку «Не подобається», ми створюємо для вас випадковий унікальний ID, який не прив'язаний до вашого облікового запису Google. Це робиться для уникнення атаки ботів. Але немає жодного способу зв'язати цей випадковий ID до вас або вашого особистого облікового запису YouTube.

### Якою саме інформацією ви володієте?

Лише ID відео. Ні ваших коментарів, ні вашого імені користувача, ні того, з ким ви поділилися відео, ні будь-яких інших додаткових метаданих. Нічого. Лише ID відео.

### Як зберігається моя IP-адреса?

Внутрішня частина нашого сервера зберігає нехешовані IP-адреси лише в енергозалежній пам'яті (ОЗП). Ці адреси не зберігаються на жорсткому диску і тому ніде не записані. Ми хешуємо IP-адреси, і вони зберігаються замість інших. Це зроблено для запобігання вандалізму у базі даних.

### Я чув дискусію щодо OAuth і доступу до мого облікового запису YouTube!

Ця функція буде необов'язковою та дуже необхідною. Якщо ви творець YouTube і хочете поділитися з нами кількістю ваших відміток «Не подобається», ви зможете це зробити. За структурою [OAuth](https://uk.wikipedia.org/wiki/OAuth#:~:text=%D0%B1%D0%B5%D0%B7%20%D0%BD%D0%B5%D0%BE%D0%B1%D1%85%D1%96%D0%B4%D0%BD%D0%BE%D1%81%D1%82%D1%96%20%D0%B2%D0%B2%D0%BE%D0%B4%D1%83%20%D1%96%D0%BC%D0%B5%D0%BD%D1%96%20%D0%BA%D0%BE%D1%80%D0%B8%D1%81%D1%82%D1%83%D0%B2%D0%B0%D1%87%D0%B0%20%D1%82%D0%B0%20%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D1%8E) надбезпечний. Ви зможете відкликати доступ до свого облікового запису в будь-яку мить, і зможете дати нам обмежені дозволи. Ми не будемо вимагати жодних дозволів, крім необжідних. Ми будемо вимагати лише дозволи перегляду статистики ваших відео.

### Наскільки достовірна ця кількость відміток «Не подобається»?

Ми вжили заходів щодо запобігання атакам ботів і збираємося продовжувати працювати над підвищенням ефективності цієї сисеми надалі: це допоможе нам зберегти підрахунок відміток «Не подобається» як хороше представлення фактичної кількості. Звичайно, він ніколи не буде точним на всі 100%, тож ви самі вирішуєте, довіряти йому чи ні.

### Чому б вам не поділитися внутрішнім кодом вашого сервера?

Ми поділимося ним у якийсь момент – але зараз немає жодних причин це робити. Це дасть хибне почуття безпеки - адже в системі з нульовою довірою ми можемо з таким самим успіхом поділитися однією версією, але розгорнути іншу. Є багато причин тримати код у таємниці, зокрема, як ми боремося зі спамом. Приховування та затьмарення коду обробки спаму є доволі стандартною практикою.
