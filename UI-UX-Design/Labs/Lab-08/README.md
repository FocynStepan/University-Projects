#  ЗВІТ ДО ЛАБОРАТОРНОЇ РОБОТИ №8
**Дисципліна:** Основи UX/UI дизайну  
**Тема:** UI-компоненти інтерфейсу: кнопки, форми та їх стани. Побудова інтерактивного UI Kit у Figma  
**Студент:** Фокін Степан, група РПЗ-33  

---

##  Мета роботи
- Ознайомитися з основними UI-компонентами інтерфейсу;
- Навчитися проєктувати кнопки, чекбокси, радіобатони та інпут-поля;
- Дослідити стани компонентів (default, hover, active, disabled, focus);
- Розробити систему компонентів у складі UI Kit;
- Навчитися використовувати варіанти (Variants) у Figma;
- Інтегрувати компоненти у власний інтерфейс фітнес-застосунку;
- Використати інструменти ШІ для генерації ідей або текстів для UI.

---

##  Матеріальне забезпечення
- Персональний комп'ютер, доступ до мережі Інтернет
- Обліковий запис Google
- Середовища Figma та FigJam

---

##  Короткі теоретичні відомості
1. **UI-компоненти** – повторно використовувані елементи (Buttons, Inputs, Switches, Checkboxes, Radio buttons), що формують взаємодію користувача з продуктом.
2. **Стани (States)** – візуальні відгуки на дії: `Default`, `Hover`, `Active/Pressed`, `Focus`, `Loading`, `Disabled`, `Error/Success`.
3. **Поля вводу** – містять `Label`, `Placeholder`, `Input Area`, `Icons`, `Helper/Error Text`.
4. **Принципи проєктування** – консистентність, зворотний зв'язок, доступність (a11y), повторне використання через `Components & Variants`.
5. **UI Kit** – бібліотека компонентів із чіткою системою станів, властивостей та правил використання.

---

##  Завдання для попередньої підготовки

###  Словник базових понять (UA / EN)
| Українською | English | Пояснення |
|-------------|---------|-----------|
| Варіант компонента | Component Variant | Підтип компонента, що відрізняється візуально або функціонально (напр. розмір, стан, колір). |
| Стан інтерфейсу | UI State | Візуальне відображення елемента під час взаємодії або очікування (напр. Disabled, Loading). |
| Автолейаут | Auto Layout | Інструмент Figma для динамічного розподілу відступів та вирівнювання шарів. |
| Властивість компонента | Component Property | Налаштування інстансу (Text, Boolean, Instance Swap), що спрощує редагування. |
| Валідація форми | Form Validation | Перевірка введених даних на відповідність правилам з миттєвим візуальним фідбеком. |
| Область натискання | Click / Tap Target | Мінімальний розмір зони взаємодії для пальця або курсору (зазвичай 44–48 px). |
| Плейсхолдер | Placeholder | Тимчасова підказка всередині поля вводу, що зникає при початку введення. |

###  Відповіді на запитання
1. **Які існують типи кнопок у UI-дизайні?**  
   `Primary` (головна дія), `Secondary` (альтернативна), `Tertiary/Ghost` (додаткова/текстова), `Icon/FAB` (швидка дія), `Destructive` (видалення/скасування).
2. **Чим відрізняється checkbox від radio button?**  
   Checkbox дозволяє обрати кілька незалежних опцій одночасно. Radio button – лише одну опцію з групи (взаємовиключний вибір).
3. **Чому важливо проєктувати стан "Disabled" для кнопок?**  
   Він запобігає помилковим діям, поки форма не заповнена або процес не завершено, і візуально інформує користувача про недоступність функції.
4. **Що таке стани компонентів і навіщо вони потрібні?**  
   Це візуальні зміни елемента у відповідь на дії користувача або системні події. Потрібні для зворотного зв'язку, покращення UX та доступності.
5. **Що таке "Focus state" і як він впливає на доступність?**  
   Це підсвічування елемента при навігації клавіатурою (Tab). Критично важливий для користувачів з обмеженими можливостями, які не використовують мишу/тач.

---

##  Хід роботи

###  Практичне завдання №1. Аналіз UI-компонентів (FigJam)
**1. Короткий мануал по типах, станах та стилях**  
*(Зафіксовано у FigJam у вигляді структурованої таблиці-довідника)*

| Компонент | Типи | Ключові стани | Стилі / Правила |
|-----------|------|---------------|-----------------|
| **Buttons** | Primary, Secondary, Ghost, Icon | Default, Hover, Pressed, Disabled, Loading | 1 Primary на екран. Padding 12-16px. Radius узгоджений з картками. |
| **Checkbox** | Single, Group, Indeterminate | Unchecked, Checked, Disabled, Error | Використовується для фільтрів, угод. Label обов'язковий. |
| **Radio Button** | List, Card-style, Inline | Unselected, Selected, Disabled | Для єдиного вибору з ≥2 варіантів. Візуальна група обов'язкова. |
| **Input Fields** | Outlined, Filled, Underline, Search | Default, Focus, Filled, Error, Success | Label зовні/зверху. Placeholder – приклад. Helper/Error text під полем. |

**2. Аналіз 3 прикладів інтерфейсів (Fitness App)**
| Приклад | Кнопки | Інпути | Селектори | Ідеї для мого проєкту |
|---------|--------|--------|-----------|------------------------|
| **Zynora (AI Fitness)** | Primary залиті, Secondary outline, Icon-buttons | Outlined з floating label, числові з префіксами | Toggle, Radio-cards, Dropdown | Floating label, картки-радіобатони для вибору цілей |
| **Ready Player Fit** | Primary gradient, Ghost nav, FAB "Add" | Filled light bg, progress indicators | Checkboxes, Segmented control, Radio-cards | Progress bars, Segmented control (Day/Week/Month) |
| **Workout Tracker (Ref.)** | Primary orange, Secondary outline, Pill-filters | Search bar, Number inputs | Segmented, Radio-cards (color-coded), Chips | Кольорове кодування карток, Circular progress, Pill buttons |

**3. Перелік компонентів для UI Kit фітнес-проєкту**
- `Button` (Primary/Secondary/Ghost/Icon) + 4 стани + Boolean `Show Icon`
- `Text Field` (Default/Password/Number/Search) + стани Focus/Error/Success
- `Checkbox` & `Radio Group` (List/Card) + стани Checked/Disabled
- `Toggle Switch` (On/Off/Disabled)
- `Validation Banner` (Inline/Toast)
- `Segmented Control` (Daily/Weekly/Monthly)

---

###  Практичне завдання №2*. Розробка кнопок та їх станів (Figma)
1. **Створення бази:** Frame → Auto Layout (H:16, V:12, Gap:8). Додано Rectangle (Fill container) для фону, Text (Montserrat Button-M), Instance іконки 24×24 (ЛР №7).
2. **Variants Setup:** Component Set з властивостями `Type` (Primary/Secondary) та `State` (Default/Hover/Pressed/Disabled).
3. **Налаштування станів:** Кольори взяті з палітри ЛР №6. 
   - `Primary`: Default (Accent), Hover (Accent-10%), Pressed (Accent-20%), Disabled (Neutral-200 + Neutral-400 text).
   - `Secondary`: Default (Transparent + Accent stroke), Hover (Accent-5 fill), Pressed (Accent-10 fill), Disabled (Neutral-300 stroke).
   - Іконки: `Outline` у Default, `Filled` у Pressed/Active (згідно з ЛР №7).
4. **Component Properties:** Додано `Text` (String), `Show Icon` (Boolean), `Icon` (Instance Swap).
5. **Prototype:** Налаштовано `While hovering` → Hover, `While pressing` → Pressed (Smart animate, 150ms). Disabled – без інтеракцій.
6. **Інтеграція:** Замінено старі кнопки на екранах `Dashboard` та `Workout Details`. Перевірено ієрархію (1 Primary на view), відступи (16-24px), контраст (≥4.5:1).


---

###  Практичне завдання №3**. Чекбокси, радіобатони, поля вводу та валідація


---

##  Посилання на проєкти
- **Figma (UI Kit + Screens):** [ПОСИЛАННЯ НА ФАЙЛ FIGMA](https://www.figma.com/design/UUKZ3Ib9nfPfTbNf923gbY/prototipa?node-id=0-1&p=f&t=2h1CLfWQqSvGMgVM-0)

- **FigJam (Аналіз + Мануал):** [ПОСИЛАННЯ НА ДОШКУ FIGJAM](https://www.figma.com/board/Y6p0MHfP1X8NRyg0iqUdD8/Labs?node-id=0-1&p=f&t=QVi99N9rW5AOFYhl-0)


---

##  Контрольні запитання
1. **Де доцільно розміщувати Placeholder, а де Label?**  
   `Label` розміщується зовні поля (зверху або зліва) і залишається видимим завжди – це ідентифікатор поля. `Placeholder` знаходиться всередині і показує формат/приклад вводу. Згідно з Nielsen Norman Group, найкраща практика – використовувати обидва: Label для постійної навігації, Placeholder для підказки.
2. **Який розмір "області натискання" є мінімально допустимим?**  
   Для мобільних пристроїв стандарт Apple HIG – `44×44 pt`, Material Design – `48×48 dp`. Для вебу рекомендується `48×48 px`. Це забезпечує комфортну взаємодію пальцем та зменшує помилкові натискання.
3. **Яку роль відіграє іконка в полі вводу?**  
   Іконка виконує роль `affordance` (підказки функції): "око" для показу пароля, лупа для пошуку, календар для дати, хрестик для очищення. Вона знижує когнітивне навантаження, прискорює розпізнавання патерну та покращує естетику без шкоди для юзабіліті.

---

##  Висновки
Під час виконання лабораторної роботи я систематизував знання про проєктування UI-компонентів та їхніх станів. Було розроблено інтерактивний UI Kit для фітнес-застосунку, що включає кнопки, чекбокси, радіобатони та інпут-поля з повним набором станів (Default, Hover, Pressed, Disabled, Focus, Error, Success). Використання `Variants` та `Component Properties` у Figma дозволило створити масштабовану систему, де зміна тексту, іконки або стану відбувається в один клік без порушення Auto Layout. Інтеграція компонентів у екрани Dashboard та Profile підтвердила важливість візуальної ієрархії, контрастності та дотримання принципів доступності (a11y). Особливу увагу приділено узгодженості з палітрою ЛР №6 та іконками ЛР №7 (Outline → Filled логіка). Робота закріпила навички проєктування форм, валідації даних та створення інтерактивних прототипів, що є критично важливим для сучасного UX/UI дизайну.

During this laboratory work, I systematized my knowledge of UI component design and their states. An interactive UI Kit for a fitness application was developed, including buttons, checkboxes, radio buttons, and input fields with a complete set of states (Default, Hover, Pressed, Disabled, Focus, Error, Success). Using `Variants` and `Component Properties` in Figma allowed me to build a scalable system where changing text, icons, or states happens in one click without breaking Auto Layout. Integrating components into the Dashboard and Profile screens confirmed the importance of visual hierarchy, contrast, and accessibility (a11y) principles. Special attention was paid to consistency with the Lab 6 color palette and Lab 7 icons (Outline → Filled logic). The work reinforced skills in form design, data validation, and interactive prototyping, which are essential for modern UX/UI design.
