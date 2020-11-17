---
title: Огляд фактичних даних
description: У цьому розділі наведено відомості про фактичні дані проекту.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: uk-UA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086914"
---
# <a name="actuals-overview"></a>Огляд фактичних даних

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Фактичні дані — це кількість виконаних у проекті робіт. Фактичні дані проекту можна відстежити у вихідних документах. До цих вихідних документів належать час, витрати та записи журналів, а також рахунки-фактури.

![Як можна відстежити фактичні дані проекту до вихідних документів](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Надіслати запис часу

У PSA, коли для проекту буде надіслано запис часу, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі. Одним із них є вартість, а інший – для невиставленого в рахунках збуту. Коли запис часу буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат. 

Логіка для введення цін за замовчуванням міститься в рядку журналу. Усі значення полів із запису часу копіюються до рядка журналу. Ці поля містять дату транзакції, сервісну роботу за договором, з якою проект зіставляється, і результат валюти з відповідного прайсу. 

Поля, що впливають на ціни за замовчуванням, наприклад **Роль** та **Організаційна одиниця** , призводять до введення належної ціни, яка буде ціною за замовчуванням у рядку журналу. У разі додавання настроюваного поля до запису часу, і якщо необхідно, щоб значення поля було розповсюджено на фактичні дані, створіть це поле у сутності "Фактичні дані", а за допомогою зіставлень полів скопіюйте поле із запису часу до фактичного значення.

## <a name="submitting-an-expense-entry"></a>Надсилання запису витрат

У PSA, коли для проекту буде надіслано запис витрат, який зіставляється з часом та матеріалами сервісної роботи за договором, створюються два рядки у журналі. Одним із них є вартість, а інший – для невиставленого в рахунках збуту. Коли запис витрат буде надіслано для проекту, який зіставляється з фіксованою ціною сервісної роботи за договором, створюється рядок у журналі лише для витрат.

Логіка для введення цін за замовчуванням для витрат залежить від категорії витрат, вибраних на сторінці **Запис витрат**. Дата угоди, сервісна робота за договором, з якою проект зіставляється, та грошова одиниця – усі вони використовуються для визначення відповідного прайсу. Проте, для самої ціни, сума, яку користувач ввів, встановлюється безпосередньо у пов'язаних із ним рядках журналів витрат для вартості і збуту за замовчуванням.

У поточній версії PSA, запис на основі категорії недоступний для кожної одиниці ціни за замовчуванням у записах витрат.

## <a name="using-entry-journals-to-record-costs"></a>Використання журналів проводок для запису витрат

У PSA, журнали проводок дають змогу записувати витрати або доходи за матеріалами, комісіями, часом, витратами, а також класами транзакції. Журнал містить заголовок, рядки та дію **Підтвердити**. Нижче наведено кілька сценаріїв, в яких можна використовувати журнал.

- Ви повинні записувати матеріальні витрати та збут за проектом.
- Слід перенести фактичні дані транзакції з іншої системи до PSA.
- Ви повинні записувати витрати, що відбулися в іншій системі, наприклад, придбання або вартість субпідрядних витрат.

> [!IMPORTANT]
> Використання журналів проводок для створення фактичних даних має виконувати лише користувач, який повністю обізнаний про вплив бухгалтерського обліку фактичних даних на проект. Це є наслідком того, що програма не перевіряє тип рядка в журналі або пов’язані ціни, введені в рядок у журналі. Через вплив цього типу журналу слід уважно визначати користувачів, яким надається доступ до створення журналів проводок.     


## <a name="recording-actuals-based-on-project-events"></a>Записування фактичних даних на основі подій проекту

PSA записує фінансові транзакції, що виникають під час проекту. Ці транзакції записуються як **фактичні дані**. У зазначених нижче таблицях відображаються типи фактичних даних, які створюються, залежно від того, чи є цей проект базується на часі й матеріалах, чи він є проектом з фіксованою ціною, чи він стадії попереднього продажу, чи це внутрішній проект.

**Ресурс належить до тієї самої організаційної одиниці, що й договірна одиниця проекту**

<table>
<thead>
<tr>
<th rowspan="3">Подія</th>
<th colspan="4">Оплачуваний або проданий проект</th>
<th rowspan="3">Проект на стадії попереднього продажу</th>
<th rowspan="3">Внутрішній проект</th>
</tr>
<tr>
<th colspan="2">Час і матеріали</th>
<th colspan="2">Фіксована ціна</th>
</tr>
<tr>
<th>Фактично</th>
<th>Грошова одиниця транзакцій</th>
<th>Фіксована ціна</th>
<th>Грошова одиниця транзакцій</th>
</tr>
</thead>
<tbody>
<tr>
<td>Створено запис часу.</td>
<td colspan="6">Немає справи в сутності фактичних даних</td>
</tr>
<tr>
<td>Запис часу надіслано.</td>
<td colspan="6">Немає справи в сутності фактичних даних</td>
</tr>
<tr>
<td rowspan="2">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</td>
<td>Фактичний показник вартості</td>
<td>Валюта договірної одиниці</td>
<td rowspan="2">Фактичний показник вартості</td>
<td rowspan="2">Валюта договірної одиниці
<td rowspan="2">Фактичний показник вартості</td>
<td rowspan="2">Фактичний показник вартості</td>
</tr>
<tr>
<td>Фактичний показник збуту, на який не виставлено рахунок - платний</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="3">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</td>
<td>Фактичний показник вартості</td>
<td>Валюта договірної одиниці</td>
<td rowspan="3">Фактичний показник вартості</td>
<td rowspan="3">Валюта договірної одиниці</td>
<td rowspan="3">Фактичний показник вартості</td>
<td rowspan="3">Фактичний показник вартості</td>
</tr>
<tr>
<td>Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="2">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</td>
<td>Скасування збуту, на який не виставлено рахунок</td>
<td>Валюта проектного договору</td>
<td rowspan="2">Збут за пробіг, на який виставлено рахунок</td>
<td rowspan="2">Валюта проектного договору</td>
<td rowspan="2">Незастосовно</td>
<td rowspan="2">Незастосовно</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="3">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</td>
<td>Скасування збуту, на який не виставлено рахунок</td>
<td>Валюта проектного договору</td>
<td rowspan="3">Незастосовно</td>
<td rowspan="3">Незастосовно</td>
<td rowspan="3">Незастосовно</td>
<td rowspan="3">Незастосовно</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок - оплачуваний за нову кількість</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Збут, виставлений в рахунку – неоплачуваний через розбіжності</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="2">Рахунок виправлено для збільшення оплачуваної кількості.</td>
<td>Збут, на який виставлено рахунок - Повернення</td>
<td>Валюта проектного договору</td>
<td rowspan="5">
<ul>
<li>Повернення виставленого рахунку за збут для проміжного етапу</li>
<li>Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></li>
</ul>
</td>
<td rowspan="5">Валюта проектного договору</td>
<td rowspan="5">Незастосовно</td>
<td rowspan="5">Незастосовно</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="3">Рахунок виправлено для зменшення оплачуваної кількості.</td>
<td>Збут, на який виставлено рахунок - Повернення</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок за нову кількість</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Збут, не виставлений в рахунку – оплачуваний через розбіжності</td>
<td>Валюта проектного договору</td>
</tr>
</tbody>
</table>

**Ресурс належить до організаційної одиниці, яка відрізняється від договірної одиниці проекту**

<table>
<thead>
<tr>
<th rowspan="3">Подія</th>
<th colspan="4">Оплачуваний або проданий проект</th>
<th rowspan="3">Проект на стадії попереднього продажу</th>
<th rowspan="3">Внутрішній проект</th>
</tr>
<tr>
<th colspan="2">Час і матеріали</th>
<th colspan="2">Фіксована ціна</th>
</tr>
<tr>
<th>Фактично</th>
<th>Грошова одиниця транзакцій</th>
<th>Фіксована ціна</th>
<th>Грошова одиниця транзакцій</th>
</tr>
</thead>
<tbody>
<tr>
<td>Створено запис часу.</td>
<td colspan="6">Немає справи в сутності фактичних даних</td>
</tr>
<tr>
<td>Запис часу надіслано.</td>
<td colspan="6">Немає справи в сутності фактичних даних</td>
</tr>
<tr>
<td rowspan="4">Час затверджено, і під час затвердження не було жодних змін або збільшень в оплачуваних годинах.</td>
<td>Фактичний показник вартості</td>
<td>Валюта договірної одиниці</td>
<td rowspan="4">Фактичний показник вартості</td>
<td rowspan="4">Валюта договірної одиниці</td>
<td rowspan="4">Фактичний показник вартості</td>
<td rowspan="4">Фактичний показник вартості</td>
</tr>
<tr>
<td>Фактичний показник збуту, на який не виставлено рахунок - платний</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Вартість одиниці ресурсів</td>
<td>Валюта одиниці ресурсів</td>
</tr>
<tr>
<td>Збут між організаціями</td>
<td>Валюта договірної одиниці</td>
</tr>
<tr>
<td rowspan="5">Час ухвалено, і під час затвердження відбувається зменшення оплачуваного часу.</td>
<td>Фактичний показник вартості</td>
<td>Валюта договірної одиниці</td>
<td rowspan="5">Фактичний показник вартості</td>
<td rowspan="5">Валюта договірної одиниці</td>
<td rowspan="5">Фактичний показник вартості</td>
<td rowspan="5">Фактичний показник вартості</td>
</tr>
<tr>
<td>Вартість одиниці ресурсів</td>
<td>Валюта одиниці ресурсів</td>
</tr>
<tr>
<td>Збут між організаціями</td>
<td>Валюта договірної одиниці</td>
</tr>
<tr>
<td>Фактичний показник збуту, на який не виставлено рахунок - оплачується за нову кількість</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Фактичний показник збуту, на який не виставлено рахунок - не оплачується через розбіжності</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="2">Рахунок-фактуру підтверджено, і не було змін або збільшення в оплачуваних годинах.</td>
<td>Скасування збуту, на який не виставлено рахунок</td>
<td>Валюта проектного договору</td>
<td rowspan="2">Збут за пробіг, на який виставлено рахунок</td>
<td rowspan="2">Валюта проектного договору</td>
<td rowspan="2">Незастосовно</td>
<td rowspan="2">Незастосовно</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="3">Підтверджено рахунок, відбулося зменшення оплачуваного часу.</td>
<td>Скасування збуту, на який не виставлено рахунок</td>
<td>Валюта проектного договору</td>
<td rowspan="3">Незастосовно</td>
<td rowspan="3">Незастосовно</td>
<td rowspan="3">Незастосовно</td>
<td rowspan="3">Незастосовно</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок - оплачуваний за нову кількість</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Збут, виставлений в рахунку – неоплачуваний через розбіжності</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="2">Рахунок виправлено для збільшення оплачуваної кількості.</td>
<td>Збут, на який виставлено рахунок - Повернення</td>
<td>Валюта проектного договору</td>
<td rowspan="5">
<ul>
<li>Повернення виставленого рахунку за збут для проміжного етапу</li>
<li>Змінення стану проміжного етапу з <strong>Виставлено рахунок</strong> на <strong>Готовий до виставлення рахунку</strong></li>
</ul>
</td>
<td rowspan="5">Валюта проектного договору</td>
<td rowspan="5">Незастосовно</td>
<td rowspan="5">Незастосовно</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td rowspan="3">Рахунок виправлено для зменшення оплачуваної кількості.</td>
<td>Збут, на який виставлено рахунок - Повернення</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Збут, на який виставлено рахунок за нову кількість</td>
<td>Валюта проектного договору</td>
</tr>
<tr>
<td>Збут, не виставлений в рахунку – оплачуваний через розбіжності</td>
<td>Валюта проектного договору</td>
</tr>
</tbody>
</table>