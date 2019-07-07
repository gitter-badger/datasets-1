# Призначення репозитарію

Репозитарій має у собі набір дата сетів та інструменти для створення, обробки чинний опублікованих opendata або публічних реєстрів, доступних як за постановою 835, так й поза неї.

## Базовий стек

Основним стеком виступає:

* Postgresql

    - Назва бази даних: opendata
    - Завжди використовуватися набір обов'язкових додаткових полів:

        - id (тип: uuid, дефолтне значення: "gen_random_uuid()")
            - Потребуе встановленного пакету postgresql-contrib
            - Потребуе реэстрації у базі данних "CREATE EXTENSION IF NOT EXISTS pgcrypto;"

* Python

## Рекомендований набір інформації по датасету

* Файл опису
* .sql файл з міграціями, для створення дата сету у базі даних
* Скрипт імпорту даних якщо вони опубліковані
* Скрипт нормалізації даних якщо він потрібен
* скрипт імпорту оброблених даних у базу даних
* графічне зображення структурі дата сету

## Список реєстрів відповідно постанові 835

### Мін'юст

01. [Єдиний державний реєстр юридичних осіб, фізичних осіб - підприємців та громадських формувань](/minjust/opendata/01)

### Держстат

17. [Класифікатор об'єктів адміністративно-територіального устрою України (КОАТУУ)](/ukrstat/opendata/17)

### Органи місцевого самоврядування

01. Основні положення генеральних планів населених пунктів та детальних планів територій

02. [Перелік об'єктів комунальної власності](/oms/opendata/02)

03. Перелік об'єктів комунальної власності, що передані в оренду чи інше право користування (з даними про умови передачі об'єктів в оренду)

04. Перелік незадіяних земельних ділянок і майнових об'єктів (приміщень) комунальної форми власності, які можуть бути передані в користування

05. Результати радіаційного контролю

06. Інформація про використання публічних коштів під час будівництва, ремонту та реконструкції об'єктів дорожньої інфраструктури та хід виконання проектів

07. Генеральні плани населених пунктів, історико-архітектурні опорні плани, плани зонування територій та детальні плани територій (за винятком відомостей, які відповідно до законодавства становлять інформацію з обмеженим доступом), їх проекти

08. Дані про місцезнаходження громадського транспорту в режимі реального часу

09. Звіти про виконання фінансових планів комунальних підприємств

10. Паспорти бюджетних програм місцевого бюджету

11. Звіти про виконання паспортів бюджетних програм місцевого бюджету

12. Титульні списки на проведення капітального та поточного ремонту, будівництва, реконструкції та благоустрою

13. Інформація про рекламні засоби (дані про місце розміщення рекламного засобу, його вид і розміри, найменування розповсюджувача зовнішньої реклами, номер його телефону, адреса електронної пошти, дата видачі дозволу та строк його дії, номер і дата укладення договору, якщо місце розміщення рекламного засобу належить до комунальної власності)

14. Реєстр боргових зобов'язань суб'єктів господарювання комунальної власності територіальної громади (як суб'єктів господарювання перед третіми особами, так і третіх осіб перед суб'єктами господарювання)

15. Перелік інвестиційних договорів, додатків, додаткових угод та інших матеріалів до них, умов, у тому числі посилань на оприлюднені ресурси в Інтернеті

16. Дані про об'єкти та засоби торгівлі (пересувна, сезонна та інші)

17. Відомості про схеми розміщення засобів сезонної торгівлі

18. Відомості про ярмарки (строк проведення, місце, кількість місць, вартість місць), організаторів ярмарків, договори, укладені з організаторами таких ярмарків

19. Дані про розміщення громадських вбиралень

20. Відомості про залучення, розрахунок розміру і використання коштів пайової участі у розвитку інфраструктури населеного пункту

21. Перелік перевізників, що надають послуги пасажирського автомобільного транспорту, та маршрутів перевезення

22. Відомості про транспортні засоби, які обслуговують пасажирські автобусні, тролейбусні та трамвайні маршрути перевезення (кількість транспортних засобів на кожному маршруті, марка, модель, державний номер, пасажиромісткість)

23. Розклад руху громадського транспорту

24. Дані про місце розміщення зупинок міського електро- та автомобільного транспорту

25. Перелік земельних ділянок, що пропонуються для здійснення забудови

26. Перелік укладених договорів (укладені договори, інші правочини, додатки, додаткові угоди та інші матеріали до них)

27. Актуальні списки власників/орендарів місцевих земельних ділянок

28. Відомості про лікарські засоби/препарати, придбані за бюджетні кошти, відомості про розподілення таких ліків між закладами охорони здоров'я та їх залишки в кожному з них

29. Бази даних щодо ремонту доріг: точне зазначення ділянки відремонтованої дороги (від кілометра до кілометра), ширина та довжина дороги, довжина ділянки, товщина дорожнього покриття, матеріали, види робіт, вартість робіт, гарантійний строк, виконавці робіт

30. Схеми планування територій та плани зонування територій (для сільських, селищних, міських рад)

31. Поіменні результати голосування депутатів на пленарних засіданнях органу місцевого самоврядування

32. Дані про депутатів місцевих рад, у тому числі контактні дані та графік прийому

33. Дані про зелені насадження, що підлягають видаленню, відповідно до виданих актів обстеження зелених насаджень

34. Надані містобудівні умови та обмеження

35. Дані про доступність будівель для осіб з інвалідністю та інших маломобільних груп населення

36. Дані про тарифи на комунальні послуги

37. Дані про надходження звернень на гарячі лінії, у аварійно-диспетчерські служби, телефонні центри тощо

38. Дані про електронні петиції, у тому числі, осіб, що їх підписали, та результати розгляду

39. Дані громадського бюджету, бюджету участі тощо, у тому числі про проекти, результати голосування, реалізацію підтриманих проектів

40. Перелік об'єктів комунальної власності, які підлягають приватизації

41. Дані про паркування, у тому числі про розміщення майданчиків, їх операторів, обладнання та функціонування

42. Адресний реєстр

43. Дані про надані адміністративні послуги

44. Дані про видані будівельні паспорти

45. Дані про медичних працівників закладів охорони здоров'я

46. Дані про педагогічних працівників закладів освіти

47. Дані про медичне обладнання комунальних закладів охорони здоров'я

48. Дані про розміщення спецтехніки, що використовується для надання комунальних послуг, благоустрою, здійснення будівельних та ремонтних робіт

49. Перелік бюджетних програм, у тому числі посилання на оприлюднені ресурси в Інтернеті

50. Перелік цільових програм, у тому числі посилання на оприлюднені ресурси в Інтернеті

51. Перелік розпорядників бюджетних коштів

52. Фінансова звітність суб'єктів господарювання комунального сектору економіки

53. Перелік дошкільних, середніх, позашкільних та професійно-технічних навчальних закладів і статистична інформація щодо них

54. Дані про черги дітей у дошкільні навчальні заклади

55. Території обслуговування загальноосвітніх навчальних закладів

56. Дані містобудівного кадастру, у тому числі геопросторові дані

57. Дані про видані дозволи на порушення об'єктів благоустрою

58. Черга на отримання земельних ділянок із земель комунальної власності

59. Дані обліку громадян, які потребують поліпшення житлових умов (квартирний облік)

60. Дані про споживання комунальних ресурсів (електроенергія, теплова енергія, природний газ, тверде паливо, холодна та гаряча вода) комунальними підприємствами, установами (закладами) та організаціями

61. Надходження і використання благодійної допомоги

62. Дані про надані містобудівні умови та обмеження

63. Планові та фактичні показники сплати за договорами оренди комунальної власності, розміщення тимчасових споруд, розміщення рекламних засобів

64. Дані про здійснення державного архітектурно-будівельного контролю, у тому числі про плани перевірок та складені документи (акти, приписи, протоколи, постанови)

65. Перелік та місцезнаходження закладів комунальних закладів охорони здоров'я, які забезпечені обладнанням гінекологічним, мамологічним обладнанням, що пристосоване до потреб осіб з інвалідністю з урахуванням особливостей їх пересування

## Список реєстрів поза 835

### Органи місцевого самоврядування

нррг
