# ТЗ: SEO-структура сайта moskitiery для польского рынка

## 1. Назначение

Документ описывает карту посадочных страниц, SEO-интенты, перелинковку, UX-flow и copy-brief для польского сайта по продаже и монтажу москитных сеток (`moskitiery`).

География пилота: `aglomeracja katowicka`.

Основной язык сайта: польский. Документ написан по-русски для проектирования, но URL, названия блоков, интенты и пользовательские категории должны использовать польскую терминологию.

## 2. Ключевые решения

- Главная `/` является главным SEO-хабом категории и закрывает ВЧ-кластеры `moskitiery`, `moskitiery na wymiar`, `moskitiery z montażem`.
- Отдельная страница `/moskitiery/` не создается, чтобы не конкурировать с главной. Если такой URL появится, он должен вести 301 на `/`.
- Калькулятор не выносится на отдельную SEO-страницу. Он размещается на каждой коммерческой странице и получает пресет из интента страницы.
- Страницы не размножаются по полной матрице `city + product + mount + mesh`.
- Гео закрывается двумя слоями: ограниченные индексируемые city landing pages + UX geo-layer на коммерческих страницах.
- Страницы по типу окон `PCV / drewniane / aluminiowe` не создаются отдельно. Они закрываются блоками внутри `/moskitiery-na-okna/`.
- Промышленный/B2B-интент закрывается одной страницей `/moskitiery-przemyslowe/`.

## 3. Формат описания посадочной страницы

Для каждой коммерческой посадочной страницы используется единый формат:

- `Кластер` — основные запросы страницы.
- `Интент` — что пользователь хочет решить.
- `Что раскрыть` — обязательные смысловые блоки для копирайтера.
- `Ограничения` — чего не обещать и какие варианты не подходят.
- `Коммерческий акцент` — где усиливать чек или доверие.
- `Перелинковка` — куда вести пользователя дальше.
- `Пресет` — начальное состояние калькулятора или формы.

## 4. Главная страница `/`

### Кластер

- `moskitiery`
- `moskitiery na wymiar`
- `moskitiery z montażem`
- `moskitiery na zamówienie`
- `producent moskitier`
- `montaż moskitier`
- `moskitiery cena`
- `moskitiery do okien i drzwi`
- `moskitiery z pomiarem`

### Интент

Пользователь ищет исполнителя и еще не всегда знает, какой тип москитной сетки нужен. Главная должна быть быстрым входом в выбор: место монтажа, тип конструкции, задача, город, цена.

### Что раскрыть

- `Moskitiery na wymiar z pomiarem i montażem`.
- Быстрый выбор: `Typ moskitiery`, `Miejsce montażu`, `Rodzaj siatki`, `Miasto`.
- Кратко показать весь ассортимент без перегруза.
- Объяснить, что сайт делает расчет в контексте выбранной страницы.
- Показать агломерацию Катовице как зону работы.

### Ограничения

- Не превращать главную в длинную энциклопедию.
- Не дублировать отдельную категорийную страницу `/moskitiery/`.
- Не пытаться на главной подробно закрыть все HST/PSK, anti-cat, meszki, przemysłowe — только дать входы.

### Коммерческий акцент

- `pomiar i montaż` как снижение риска ошибки.
- `na wymiar` как отличие от marketowych gotowych moskitier.
- Пакетные заказы: квартира, дом, несколько окон.
- Быстрый расчет и заявка без обязательного звонка.

### Перелинковка

```txt
/cennik-moskitier/
/pomiar-i-montaz-moskitier/
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-elektryczne/
/moskitiery-przemyslowe/
/moskitiery-na-okna/
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-drzwi-przesuwne/
/moskitiery-tarasowe/
/moskitiery-na-balkon/
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/moskitiery-katowice/
/moskitiery-chorzow/
/moskitiery-sosnowiec/
/moskitiery-gliwice/
/moskitiery-zabrze/
```

### Пресет

```json
{
  "intent": "home_hub",
  "mode": "guided_selection",
  "product": null,
  "mountPlace": null,
  "mesh": null,
  "city": null
}
```

## 5. Цена `/cennik-moskitier/`

### Кластер

- `moskitiery cennik`
- `moskitiera cena`
- `ile kosztuje moskitiera`
- `moskitiery na wymiar cena`
- `moskitiery z montażem cena`

### Интент

Пользователь хочет понять порядок цены и факторы расчета до контакта.

### Что раскрыть

- Цена зависит от размера, типа конструкции, полотна, цвета профиля, монтажа, количества и сложности проема.
- Примеры расчетов: okno standardowe, drzwi balkonowe, taras/HST, anti-cat.
- Показать, почему точная цена требует размеров или замера.
- На странице должен быть калькулятор с выбором типа и места монтажа.

### Ограничения

- Не обещать фиксированную цену для сложных HST/PSK, tarasów, przemysłowych otworów.
- Для B2B и больших проемов использовать `wycena indywidualna`.

### Коммерческий акцент

- Прозрачная цена без скрытых доплат.
- Скидка/выгода при нескольких окнах.
- Замер снижает риск ошибки.

### Перелинковка

```txt
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-plisowane/
/moskitiery-tarasowe/
/moskitiery-na-okna-dachowe/
/moskitiery-przemyslowe/
/pomiar-i-montaz-moskitier/
```

### Пресет

```json
{
  "intent": "price",
  "mode": "calculator_first",
  "product": null,
  "mountPlace": null,
  "mesh": null
}
```

## 6. Замер и монтаж `/pomiar-i-montaz-moskitier/`

### Кластер

- `pomiar moskitier`
- `montaż moskitier`
- `moskitiery z montażem`
- `moskitiery z pomiarem`
- `montaż moskitier na wymiar`

### Интент

Пользователь сомневается, сможет ли правильно измерить проем, или хочет заказать услугу под ключ.

### Что раскрыть

- Как проходит pomiar.
- Когда можно измерить самому, а когда лучше вызвать специалиста.
- Какие проемы требуют точного замера: HST/PSK, okna dachowe, tarasy, duże przejścia, przemysłowe.
- Что входит в монтаж.
- Как готовить окно/двери к замеру.

### Ограничения

- Не обещать одинаковый монтаж для всех систем.
- Для PSK/HST и промышленных объектов обязательно указать необходимость индивидуальной оценки.

### Коммерческий акцент

- Гарантия точного размера.
- Меньше риска повреждения профиля.
- Быстрее оформить заказ на несколько окон.

### Перелинковка

```txt
/moskitiery-na-okna/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-drzwi-przesuwne/
/moskitiery-tarasowe/
/moskitiery-na-okna-dachowe/
/moskitiery-przemyslowe/
/cennik-moskitier/
```

### Пресет

```json
{
  "intent": "measurement_installation",
  "mode": "lead_form",
  "service": "pomiar_i_montaz"
}
```

## 7. Контакт `/kontakt/`

### Кластер

- `moskitiery kontakt`
- `montaż moskitier kontakt`
- `wycena moskitier`

### Интент

Пользователь хочет быстро связаться, отправить размеры или заказать замер.

### Что раскрыть

- Телефон, форма, email/WhatsApp если используется.
- Зона обслуживания: aglomeracja katowicka.
- Что отправить для быстрой wyceny: размеры, фото окна/двери, город, количество, тип проема.

### Ограничения

- Не делать контактную страницу вместо посадочной.
- Не скрывать фактический регион работы.

### Коммерческий акцент

- Быстрая заявка.
- Возможность приложить фото.
- Выезд на замер.

### Перелинковка

```txt
/pomiar-i-montaz-moskitier/
/cennik-moskitier/
/moskitiery-katowice/
```

### Пресет

```json
{
  "intent": "contact",
  "mode": "lead_form"
}
```

## 8. City landing pages aglomeracji katowickiej

### Индексируемые URL первого этапа

```txt
/moskitiery-katowice/
/moskitiery-chorzow/
/moskitiery-sosnowiec/
/moskitiery-gliwice/
/moskitiery-zabrze/
/moskitiery-bytom/
/moskitiery-ruda-slaska/
/moskitiery-tychy/
```

### Кластер шаблона

Для `{city}`:

- `moskitiery {city}`
- `moskitiery na wymiar {city}`
- `moskitiery z montażem {city}`
- `moskitiery do okien {city}`
- `moskitiery drzwiowe {city}`
- `moskitiera {city} cena`

### Интент

Пользователь ищет локального исполнителя с замером и монтажом в своем городе.

### Что раскрыть

- `Moskitiery na wymiar w {city}`.
- Pomiar i montaż w mieście.
- Najczęściej wybierane rozwiązania: ramkowe, drzwiowe, plisowane, rolowane, dla kota.
- Dzielnice, okolice или соседние города, если это реально полезно.
- Czas realizacji и warunki dojazdu.
- Локальный CTA.
- Калькулятор с `city={city}`.

### Ограничения

- Не создавать фейковый офис в каждом городе.
- Не писать один и тот же текст с заменой названия города.
- Не создавать `city + product/service` матрицу на старте.

### Коммерческий акцент

- Физический выезд на замер.
- Локальная скорость обслуживания.
- Реальные фото/кейсы/отзывы из города, когда появятся.

### Schema.org

Для city landing использовать JSON-LD `HomeAndConstructionBusiness` или `LocalBusiness`.

Правила:

- `address` указывать только реальный адрес компании.
- Для городов без офиса использовать `areaServed`, а не фейковый адрес.
- В `areaServed` указывать город, например `Katowice`, `Chorzów`, `Gliwice`.
- При возможности добавить `sameAs` или `additionalProperty` со ссылкой на стабильный гео-объект, но не делать это обязательным, если нет уверенности в корректной ссылке.

Пример:

```json
{
  "@context": "https://schema.org",
  "@type": "HomeAndConstructionBusiness",
  "name": "Brand",
  "areaServed": {
    "@type": "City",
    "name": "Katowice"
  },
  "url": "https://example.pl/moskitiery-katowice/"
}
```

### Перелинковка

City page ведет в канонические страницы услуг с UX-параметром города:

```txt
/moskitiery-ramkowe/?city=katowice
/moskitiery-na-drzwi-balkonowe/?city=katowice
/moskitiery-na-drzwi-przesuwne/?city=katowice
/moskitiery-plisowane/?city=katowice
/moskitiery-dla-kota/?city=katowice
```

### Пресет

```json
{
  "intent": "city_landing",
  "mode": "city_service_selection",
  "city": "katowice"
}
```

## 9. UX geo-layer на коммерческих страницах

### Назначение

Гео-модуль дает пользователю выбор города и преднастраивает калькулятор, но не создает дублей `city + every service`.

### Где используется

На всех коммерческих страницах: главная, цена, монтаж, типы конструкций, места монтажа, полотна/задачи, B2B.

### Что раскрыть

Блок:

```txt
Montaż w aglomeracji katowickiej
```

Содержит:

- короткий общий текст по агломерации;
- список городов;
- прямые ссылки на индексируемые city landing pages;
- выбранный город для калькулятора;
- краткий локальный текст по выбранному городу;
- локальный CTA.

### Важное техническое правило

Индексируемые city pages должны быть доступны как обычные ссылки:

```html
<a href="/moskitiery-katowice/">Katowice</a>
<a href="/moskitiery-chorzow/">Chorzów</a>
<a href="/moskitiery-sosnowiec/">Sosnowiec</a>
```

Дизайнер может стилизовать их как вкладки или кнопки, но в HTML это должны быть crawlable links.

UX-состояние услуги может использовать параметр:

```txt
/moskitiery-ramkowe/?city=katowice
```

Правила:

- canonical параметрной версии указывает на чистую страницу услуги;
- параметрные URL не попадают в sitemap;
- параметрные URL не являются отдельными SEO-страницами;
- основной гео-трафик собирают `/moskitiery-{city}/`.

## 10. Типы конструкций

### `/moskitiery-ramkowe/`

#### Кластер

- `moskitiery ramkowe`
- `moskitiera ramkowa`
- `moskitiery okienne ramkowe`
- `moskitiera ramkowa cena`

#### Интент

Пользователь хочет классическую оконную москитную сетку на рамке.

#### Что раскрыть

- Что такое moskitiera ramkowa.
- Для каких окон подходит.
- Какие крепления возможны.
- Когда подойдет anti-cat или przeciwpyłkowa.
- Как снять/поставить рамку на сезон.

#### Ограничения

- Не позиционировать как решение для HST/PSK, больших террасных проходов и okien dachowych.
- Для больших нестандартных проемов вести в plisy/przesuwne/rolowane.

#### Коммерческий акцент

- Самый массовый и выгодный вариант.
- Хорошо подходит для нескольких окон в квартире.
- Можно повышать чек через anti-cat, kolor profilu, montaż.

#### Перелинковка

```txt
/moskitiery-na-okna/
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/moskitiery-na-meszki/
/cennik-moskitier/
```

#### Пресет

```json
{
  "intent": "product_type",
  "product": "ramkowa",
  "allowedMountPlaces": ["okno", "okno_pcv", "okno_drewniane", "okno_aluminiowe"],
  "excludedMountPlaces": ["taras", "okno_dachowe", "hst_psk"]
}
```

### `/moskitiery-drzwiowe/`

#### Кластер

- `moskitiery drzwiowe`
- `moskitiera na drzwi`
- `moskitiera drzwiowa na zawiasach`
- `moskitiera drzwiowa z magnesem`

#### Интент

Пользователь ищет сетку на проходную дверь.

#### Что раскрыть

- Распашная конструкция на zawiasach.
- Rączka, magnes, zatrzask, samozamykacz.
- Где подходит: drzwi balkonowe, tarasowe, gospodarcze.
- Как влияет частота прохода.

#### Ограничения

- Не рекомендовать как основной вариант для HST/PSK и больших раздвижных систем.
- Уточнить, что для очень широких проемов лучше plisy/przesuwne.

#### Коммерческий акцент

- Удобство ежедневного прохода.
- Самозакрывание и фурнитура.
- Усиление для животных.

#### Перелинковка

```txt
/moskitiery-na-drzwi-balkonowe/
/moskitiery-tarasowe/
/moskitiery-dla-kota/
/moskitiery-na-drzwi-przesuwne/
```

#### Пресет

```json
{
  "intent": "product_type",
  "product": "drzwiowa",
  "mountPlace": "drzwi",
  "recommendedOptions": ["magnes", "samozamykacz"]
}
```

### `/moskitiery-rolowane/`

#### Кластер

- `moskitiery rolowane`
- `moskitiera rolowana`
- `moskitiera w kasecie`
- `moskitiera rolowana cena`

#### Интент

Пользователь ищет сетку, которая сворачивается в кассету и не требует сезонного снятия.

#### Что раскрыть

- Siatka zwijana do kasety.
- Prowadnice, listwa, mechanizm sprężynowy или ручное управление.
- Когда rolowana удобнее ramkowa.
- Где подходит: okna, drzwi balkonowe, okna dachowe.

#### Ограничения

Обязательно отделить от роллет:

```txt
Moskitiery rolowane nie są roletami zewnętrznymi. To siatki przeciw owadom zwijane do kasety, a nie aluminiowe rolety zabezpieczające okno.
```

Не обещать совместимость с толстой anti-cat без проверки системы.

#### Коммерческий акцент

- Удобство и эстетика.
- Нет необходимости снимать на сезон.
- Хорошо для okien dachowych и аккуратных оконных решений.

#### Перелинковка

```txt
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-okna/
/moskitiery-elektryczne/
```

#### Пресет

```json
{
  "intent": "product_type",
  "product": "rolowana",
  "allowedMountPlaces": ["okno", "drzwi_balkonowe", "okno_dachowe"]
}
```

### `/moskitiery-przesuwne/`

#### Кластер

- `moskitiery przesuwne`
- `moskitiera przesuwna`
- `moskitiera do drzwi przesuwnych`
- `moskitiera do HST`
- `moskitiera do PSK`

#### Интент

Пользователь имеет большую раздвижную систему, балкон/террасу или HST/PSK и ищет совместимое решение.

#### Что раскрыть

- Как работает moskitiera przesuwna.
- Где подходит: duże przeszklenia, HST, PSK, taras.
- Разница между rozwiązaniem przesuwnym и plisowanym.
- Почему нужен точный pomiar.

#### Ограничения

Не писать общую фразу “подходит для всех раздвижных дверей”. Нужна экспертная ремарка:

```txt
W systemach HST i PSK sposób pracy skrzydła wpływa na dobór moskitiery. Przy PSK skrzydło najpierw odsuwa się od ramy, a następnie przesuwa w bok, dlatego zwykła moskitiera drzwiowa na zawiasach często koliduje z pracą drzwi. W takich przypadkach zwykle dobiera się moskitierę plisowaną lub przesuwną z odpowiednim odsunięciem profilu.
```

#### Коммерческий акцент

- Высокий чек.
- Точный замер.
- Премиальная фурнитура и направляющие.
- Комфорт для terasu/HST.

#### Перелинковка

```txt
/moskitiery-na-drzwi-przesuwne/
/moskitiery-tarasowe/
/moskitiery-plisowane/
/pomiar-i-montaz-moskitier/
```

#### Пресет

```json
{
  "intent": "product_type",
  "product": "przesuwna",
  "mountPlace": "hst_psk",
  "mode": "quote_recommended"
}
```

### `/moskitiery-plisowane/`

#### Кластер

- `moskitiery plisowane`
- `moskitiera plisowana`
- `moskitiera plisowana tarasowa`
- `moskitiera plisowana cena`

#### Интент

Пользователь ищет удобное premium-решение для большого прохода, террасы или двери balkonowej/przesuwnej.

#### Что раскрыть

- Siatka składana harmonijkowo.
- Почему хорошо подходит для szerokich przejść.
- Низкий порог, wygoda, estetyka.
- Сравнение с przesuwną и drzwiową.

#### Ограничения

- Не обещать anti-cat как стандартную совместимость.
- Для очень нестандартных размеров — wycena indywidualna.

#### Коммерческий акцент

- Premium.
- Большой проем.
- Эстетика и комфорт.
- HST/PSK, taras, balkon.

#### Перелинковка

```txt
/moskitiery-tarasowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-drzwi-przesuwne/
/moskitiery-przesuwne/
```

#### Пресет

```json
{
  "intent": "product_type",
  "product": "plisowana",
  "recommendedMountPlaces": ["taras", "drzwi_balkonowe", "hst_psk"]
}
```

### `/moskitiery-elektryczne/`

#### Кластер

- `moskitiery elektryczne`
- `moskitiera elektryczna`
- `moskitiera sterowana pilotem`
- `moskitiera tarasowa elektryczna`
- `screen tarasowy z moskitierą`

#### Интент

Пользователь ищет автоматизированное решение для большого проема, террасы, перголы, дома premium или коммерческого объекта.

#### Что раскрыть

- Napęd, pilot, przełącznik, aplikacja, smart home.
- Возможные датчики: wiatr, słońce, timer — если реально предлагаются.
- Отличие от обычных rolowanych.
- Где нужна индивидуальная wycena.

#### Ограничения

- Не обещать автоматику для всех типов окон.
- Не смешивать с полноценными roletami zewnętrznymi, если они не продаются.

#### Коммерческий акцент

- Максимальный комфорт.
- Большие проемы.
- Dom premium, taras, pergola, B2B.

#### Перелинковка

```txt
/moskitiery-tarasowe/
/moskitiery-rolowane/
/moskitiery-przemyslowe/
/pomiar-i-montaz-moskitier/
```

#### Пресет

```json
{
  "intent": "product_type",
  "product": "elektryczna",
  "mode": "request_quote"
}
```

### `/moskitiery-przemyslowe/`

#### Кластер

- `moskitiery przemysłowe`
- `moskitiera przemysłowa`
- `siatki przeciw owadom dla przemysłu`
- `siatki przeciw owadom do hal`
- `moskitiery do hal`
- `moskitiery do magazynów`
- `moskitiery do hal produkcyjnych`
- `moskitiery na bramy wjazdowe`
- `zabezpieczenie przed owadami dla firm`

#### Интент

B2B-пользователь ищет защиту от насекомых для объекта: hala, magazyn, gastronomia, brama, świetlik, wentylacja.

#### Что раскрыть

Секции:

- `Bramy wjazdowe i garażowe`.
- `Hale produkcyjne i magazyny`.
- `Gastronomia i zaplecza kuchenne`.
- `Świetliki dachowe i wentylacja`.
- `Czerpnie, wentylatory, urządzenia techniczne`.
- `Kurtyny PCV antyinsektowe jako alternatywa`.

#### Ограничения

- Не создавать отдельные страницы под эти секции на старте.
- Не обещать бытовой калькулятор для промышленных объектов.
- Не продавать kurtyny PCV как основной продукт, если это не реальная услуга.

#### Коммерческий акцент

- Индивидуальный проект.
- Wytrzymałość, serwis, higiena, łatwe czyszczenie.
- Заявка на wycenę, а не мгновенная цена.

#### Перелинковка

```txt
/moskitiery-elektryczne/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/pomiar-i-montaz-moskitier/
/kontakt/
```

#### Пресет

```json
{
  "intent": "industrial",
  "mode": "request_quote",
  "fields": [
    "typ_obiektu",
    "miejsce_montazu",
    "szerokosc",
    "wysokosc",
    "liczba_otworow",
    "material_siatki",
    "sposob_otwierania",
    "czy_wymagany_montaz",
    "opis_problemu"
  ]
}
```

## 11. Места монтажа

### `/moskitiery-na-okna/`

#### Кластер

- `moskitiery na okna`
- `moskitiera na okno`
- `moskitiery okienne`
- `moskitiera okienna cena`
- `moskitiera na okno PCV`
- `moskitiera na okno drewniane`
- `moskitiera na okno aluminiowe`

#### Интент

Пользователь знает, что нужна сетка на окно, но не обязательно знает тип конструкции.

#### Что раскрыть

- Рекомендуемые типы: ramkowa, rolowana.
- Внутренние H2: `Moskitiery na okna PCV`, `Moskitiery na okna drewniane`, `Moskitiery na profile aluminiowe`.
- Различия по крепежу, толщине профиля, эстетике, цвету.
- Anti-cat, przeciwpyłkowa, micro mesh как опции.

#### Ограничения

- Не создавать отдельные URL под PCV/drewno/aluminium.
- Не вести okna dachowe сюда как основной интент — для них есть отдельная страница.

#### Коммерческий акцент

- Комплект на все окна.
- Замер и монтаж.
- Цвет профиля под окно.

#### Перелинковка

```txt
/moskitiery-ramkowe/
/moskitiery-rolowane/
/moskitiery-na-okna-dachowe/
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/cennik-moskitier/
```

#### Пресет

```json
{
  "intent": "mount_place",
  "mountPlace": "okno",
  "recommendedProducts": ["ramkowa", "rolowana"],
  "defaultProduct": "ramkowa"
}
```

### `/moskitiery-na-okna-dachowe/`

#### Кластер

- `moskitiera na okno dachowe`
- `moskitiery na okna dachowe`
- `moskitiera do okna dachowego`

#### Интент

Пользователь ищет решение для окна под наклоном, где стандартная рамка часто неудобна.

#### Что раскрыть

- Почему okno dachowe требует другого подхода.
- Рекомендуемые типы: rolowane, иногда plisowane.
- Монтаж внутри помещения, направляющие, кассета.
- Совместимость с klamką, roletą, wnęką.

#### Ограничения

- Не рекомендовать ramkowe как основной вариант.
- Не обещать стандартную цену без размеров и проверки окна.

#### Коммерческий акцент

- Спальни и детские на poddaszu.
- Удобство управления.
- Точный pomiar.

#### Перелинковка

```txt
/moskitiery-rolowane/
/moskitiery-plisowane/
/pomiar-i-montaz-moskitier/
/cennik-moskitier/
```

#### Пресет

```json
{
  "intent": "mount_place",
  "mountPlace": "okno_dachowe",
  "recommendedProducts": ["rolowana", "plisowana"],
  "defaultProduct": "rolowana"
}
```

### `/moskitiery-na-drzwi-balkonowe/`

#### Кластер

- `moskitiera na drzwi balkonowe`
- `moskitiery na drzwi balkonowe`
- `moskitiera balkonowa drzwiowa`

#### Интент

Пользователь ищет сетку на проход на балкон.

#### Что раскрыть

- Рекомендуемые типы: drzwiowa, rolowana boczna, plisowana.
- Когда хватит распашной, а когда лучше plisa.
- Magnes, samozamykacz, wygodne przejście.
- Варианты для квартир и домов.

#### Ограничения

- Не смешивать с HST/PSK — для них отдельная страница.
- Не обещать anti-cat для любой системы.

#### Коммерческий акцент

- Удобный ежедневный проход.
- Доводчик/магнит.
- Усиленный вариант для животных.

#### Перелинковка

```txt
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-plisowane/
/moskitiery-dla-kota/
/moskitiery-na-drzwi-przesuwne/
```

#### Пресет

```json
{
  "intent": "mount_place",
  "mountPlace": "drzwi_balkonowe",
  "recommendedProducts": ["drzwiowa", "rolowana", "plisowana"],
  "defaultProduct": "drzwiowa"
}
```

### `/moskitiery-na-drzwi-przesuwne/`

#### Кластер

- `moskitiera do drzwi przesuwnych`
- `moskitiera do drzwi przesuwnych HST`
- `moskitiera przesuwna PSK`
- `moskitiera na duże okno tarasowe`
- `moskitiera do systemu HST`

#### Интент

Пользователь имеет HST, PSK, duże przeszklenie или tarasowe drzwi przesuwne и ищет технически совместимую москитную сетку.

#### Что раскрыть

- Разница между HST и PSK.
- Почему обычная распашная moskitiera drzwiowa часто не подходит.
- Рекомендуемые решения: plisowana, przesuwna, иногда rolowana boczna.
- Необходимость точного zamontowania и odsadzenia profilu.

#### Ограничения

Добавить экспертную формулировку:

```txt
W systemach HST i PSK sposób pracy skrzydła wpływa na dobór moskitiery. Przy PSK skrzydło najpierw odsuwa się od ramy, a następnie przesuwa w bok, dlatego zwykła moskitiera drzwiowa na zawiasach często koliduje z pracą drzwi. W takich przypadkach zwykle dobiera się moskitierę plisowaną lub przesuwną z odpowiednim odsunięciem profilu.
```

#### Коммерческий акцент

- Высокий чек.
- Экспертный замер.
- Plisowane/przesuwne как premium.
- Комфорт выхода на taras.

#### Перелинковка

```txt
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-tarasowe/
/pomiar-i-montaz-moskitier/
```

#### Пресет

```json
{
  "intent": "mount_place",
  "mountPlace": "hst_psk",
  "recommendedProducts": ["plisowana", "przesuwna"],
  "defaultProduct": "plisowana",
  "mode": "quote_recommended"
}
```

### `/moskitiery-tarasowe/`

#### Кластер

- `moskitiery tarasowe`
- `moskitiera na taras`
- `moskitiera do drzwi tarasowych`
- `moskitiera do pergoli`

#### Интент

Пользователь хочет защитить большой выход на террасу, pergolę или strefę wypoczynku.

#### Что раскрыть

- Большие размеры и частое использование.
- Рекомендуемые типы: plisowane, przesuwne, elektryczne.
- Когда нужна автоматика.
- Влияние ветра, ширины проема, порога.

#### Ограничения

- Не вести в простые ramkowe.
- Для очень больших проемов — individualna wycena.

#### Коммерческий акцент

- Premium и комфорт.
- Автоматика.
- Эстетика на террасе.
- Удобный проход без насекомых.

#### Перелинковка

```txt
/moskitiery-plisowane/
/moskitiery-przesuwne/
/moskitiery-elektryczne/
/moskitiery-na-drzwi-przesuwne/
```

#### Пресет

```json
{
  "intent": "mount_place",
  "mountPlace": "taras",
  "recommendedProducts": ["plisowana", "przesuwna", "elektryczna"],
  "mode": "quote_recommended"
}
```

### `/moskitiery-na-balkon/`

#### Кластер

- `moskitiera na balkon`
- `moskitiery balkonowe`
- `moskitiera na balkon w bloku`
- `moskitiera na loggię`

#### Интент

Пользователь ищет решение для балкона или лоджии, чаще в квартире.

#### Что раскрыть

- Окна балкона, drzwi balkonowe, loggia.
- Разные сценарии: обычный балкон, zabudowana loggia, выход на балкон.
- Рекомендуемые типы: ramkowe, drzwiowe, plisowane, przesuwne.

#### Ограничения

- Не создавать отдельную `/moskitiery-na-loggie/` на старте.
- Для нестандартных zabudów — pomiar.

#### Коммерческий акцент

- Комплект на балкон.
- Быстрый замер нескольких элементов.
- Anti-cat для квартир с животными.

#### Перелинковка

```txt
/moskitiery-na-okna/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-dla-kota/
/moskitiery-plisowane/
```

#### Пресет

```json
{
  "intent": "mount_place",
  "mountPlace": "balkon",
  "recommendedProducts": ["ramkowa", "drzwiowa", "plisowana"],
  "mode": "guided_selection"
}
```

## 12. Полотна и задачи

### `/moskitiery-dla-kota/`

#### Кластер

- `moskitiera dla kota`
- `moskitiera anti cat`
- `siatka dla kota na okno`
- `mocna moskitiera dla kota`

#### Интент

Пользователь хочет защитить окно/дверь от повреждения когтями и снизить риск побега животного.

#### Что раскрыть

- Anti-cat / pet screen как более прочное полотно.
- Совместимость: ramkowe, drzwiowe, czasem przesuwne.
- Усиленный профиль и крепление.
- Для каких случаев это не гарантия безопасности.

#### Ограничения

- Не обещать защиту от выпадения ребенка или 100% защиту животного.
- Не рекомендовать как стандарт для plisowanych, rzepowych, magnetycznych.

#### Коммерческий акцент

- Выше чек через усиленное полотно, профиль, монтаж.
- Квартиры с кошками, балконы, двери.

#### Перелинковка

```txt
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-na-balkon/
/moskitiery-na-okna/
```

#### Пресет

```json
{
  "intent": "mesh_task",
  "mesh": "anti_cat",
  "recommendedProducts": ["ramkowa", "drzwiowa", "przesuwna"]
}
```

### `/moskitiery-przeciwpylkowe/`

#### Кластер

- `moskitiera przeciwpyłkowa`
- `siatka przeciwpyłkowa`
- `moskitiera dla alergika`
- `moskitiery antyalergiczne`

#### Интент

Пользователь хочет уменьшить попадание pyłków, kurzu и аллергенов при проветривании.

#### Что раскрыть

- Плотнее стандартной сетки.
- Для alergików, жителей рядом с zielenią или ruchliwą drogą.
- Совместимость: ramkowe, drzwiowe, część rolowanych.
- Требует чаще чистить.

#### Ограничения

- Не обещать медицинский эффект.
- Указать компромисс: меньше airflow, выше цена.

#### Коммерческий акцент

- Premium-полотно.
- Сезон pylenia.
- Комбинация с несколькими окнами.

#### Перелинковка

```txt
/moskitiery-na-okna/
/moskitiery-ramkowe/
/moskitiery-rolowane/
/jak-czyscic-i-myc-moskitiere/
```

#### Пресет

```json
{
  "intent": "mesh_task",
  "mesh": "anti_pollen",
  "recommendedProducts": ["ramkowa", "drzwiowa", "rolowana"]
}
```

### `/moskitiery-na-meszki/`

#### Кластер

- `moskitiera na meszki`
- `siatka na meszki`
- `moskitiera na drobne owady`
- `gęsta siatka przeciw owadom`

#### Интент

Пользователь хочет защиту от мелких насекомых, против которых стандартная ячейка может быть недостаточной.

#### Что раскрыть

- Standardowa siatka może nie zatrzymać meszek.
- Нужна gęstsza siatka: micro mesh или выбранные przeciwpyłkowe/Poll-tex-полотна.
- Где особенно актуально: okolice wody, ogród, lato, Śląsk.
- Совместимость: чаще ramkowe, drzwiowe, часть rolowanych.

#### Ограничения

Обязательно указать компромисс:

```txt
Na meszki zwykła siatka o standardowym oczku może nie wystarczyć. Do ochrony przed drobnymi owadami stosuje się gęstszą siatkę typu micro mesh albo wybrane tkaniny przeciwpyłkowe. Trzeba jednak pamiętać, że gęstsze oczko może nieco ograniczać przepływ powietrza i wymaga częstszego czyszczenia.
```

#### Коммерческий акцент

- Выше чек через специализированное полотно.
- Летний сезон.
- Связка с przeciwpyłkowe.

#### Перелинковка

```txt
/moskitiery-przeciwpylkowe/
/moskitiery-na-okna/
/moskitiery-ramkowe/
/jak-czyscic-i-myc-moskitiere/
```

#### Пресет

```json
{
  "intent": "mesh_task",
  "mesh": "micro_mesh",
  "recommendedProducts": ["ramkowa", "drzwiowa", "rolowana"]
}
```

### `/moskitiery-transparentne/`

#### Кластер

- `moskitiera transparentna`
- `siatka transparentna do okna`
- `moskitiera z dobrą widocznością`
- `moskitiera high visibility`

#### Интент

Пользователь хочет защиту от насекомых без сильного ухудшения вида из окна.

#### Что раскрыть

- Более тонкая/менее заметная сетка.
- Для окон с хорошим видом, salonu, tarasu.
- Совместимость: ramkowe, drzwiowe, przesuwne.

#### Ограничения

- Не продавать как самую прочную.
- Не путать с противоаллергенной или anti-cat.

#### Коммерческий акцент

- Эстетика.
- Премиальный вид.
- Подходит для видовых окон.

#### Перелинковка

```txt
/moskitiery-na-okna/
/moskitiery-ramkowe/
/moskitiery-tarasowe/
```

#### Пресет

```json
{
  "intent": "mesh_task",
  "mesh": "transparent",
  "recommendedProducts": ["ramkowa", "drzwiowa", "przesuwna"]
}
```

### `/moskitiery-antysmogowe/`

#### Кластер

- `moskitiera antysmogowa`
- `siatka antysmogowa na okno`
- `moskitiera filtrująca`
- `siatka do okna przeciw smogowi`

#### Интент

Пользователь ищет фильтрующее полотно, обычно для квартиры в городе.

#### Что раскрыть

- Это не обычная moskitiera, а specjalna tkanina filtrująca.
- Возможное снижение przepływu powietrza.
- Требует регулярной чистки/замены, если производитель это предусматривает.
- Лучше использовать осторожные формулировки.

#### Ограничения

- Не обещать медицинскую или гарантированную защиту от smogu.
- Не предлагать для всех конструкций без проверки совместимости.

#### Коммерческий акцент

- Городские квартиры.
- Premium/спецполотно.
- Связка с аллергией, пылью, дорогами.

#### Перелинковка

```txt
/moskitiery-przeciwpylkowe/
/moskitiery-na-okna/
/moskitiery-ramkowe/
```

#### Пресет

```json
{
  "intent": "mesh_task",
  "mesh": "filtering",
  "mode": "compatibility_check"
}
```

## 13. Информационные страницы

Информационные страницы не размножаются по городам и не описываются как коммерческие посадочные в этом brief. Их задача: ответить на вопрос и перевести пользователя в коммерческий интент.

```txt
/jak-wybrac-moskitiere/
/jak-zmierzyc-okno-pod-moskitiere/
/moskitiera-ramkowa-czy-rolowana/
/moskitiera-plisowana-czy-przesuwna/
/jaka-moskitiera-dla-kota/
/jak-czyscic-i-myc-moskitiere/
/czy-sciagac-moskitiery-na-zime/
```

## 14. Правила против дублей

- Не создавать `/moskitiery/`, если главная является главным хабом.
- Не создавать отдельные страницы `PCV / drewniane / aluminiowe`; держать их блоками на `/moskitiery-na-okna/`.
- Не создавать city + service/product матрицу на старте.
- Создавать только city landing pages формата `/moskitiery-{city}/`.
- Для HST/PSK использовать `/moskitiery-na-drzwi-przesuwne/`, не плодить отдельные `/moskitiery-hst/` и `/moskitiery-psk/` на старте.
- Для `okna dachowe` использовать одну страницу `/moskitiery-na-okna-dachowe/`.
- Для промышленного интента использовать одну страницу `/moskitiery-przemyslowe/`.
- Для калькулятора не создавать отдельную SEO-страницу.

## 15. Итоговая карта URL

```txt
/
/cennik-moskitier/
/pomiar-i-montaz-moskitier/
/kontakt/

/moskitiery-katowice/
/moskitiery-chorzow/
/moskitiery-sosnowiec/
/moskitiery-gliwice/
/moskitiery-zabrze/
/moskitiery-bytom/
/moskitiery-ruda-slaska/
/moskitiery-tychy/

/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-elektryczne/
/moskitiery-przemyslowe/

/moskitiery-na-okna/
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-drzwi-przesuwne/
/moskitiery-tarasowe/
/moskitiery-na-balkon/

/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/moskitiery-na-meszki/
/moskitiery-transparentne/
/moskitiery-antysmogowe/

/jak-wybrac-moskitiere/
/jak-zmierzyc-okno-pod-moskitiere/
/moskitiera-ramkowa-czy-rolowana/
/moskitiera-plisowana-czy-przesuwna/
/jaka-moskitiera-dla-kota/
/jak-czyscic-i-myc-moskitiere/
/czy-sciagac-moskitiery-na-zime/
```

## 16. Второй этап расширения

После проверки лидов, позиций и фактического спроса можно добавить:

```txt
/moskitiery-myslowice/
/moskitiery-siemianowice-slaskie/
/moskitiery-swietochlowice/
/moskitiery-dabrowa-gornicza/
/moskitiery-bedzin/
/moskitiery-czeladz/
/moskitiery-mikolow/
/moskitiery-tarnowskie-gory/
/moskitiery-piekary-slaskie/
```

Дробление на `city + product/service` разрешается только при наличии реальных данных: спрос, лиды, кейсы, фото, локальные отзывы и отдельная ценность страницы.
