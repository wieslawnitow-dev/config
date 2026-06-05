# ТЗ: SEO-структура сайта moskitiery для польского рынка

## 1. Назначение

Документ описывает карту посадочных страниц, SEO-интенты, перелинковку и UX-flow для польского сайта по продаже и монтажу москитных сеток (`moskitiery`).

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

## 3. Главная страница `/`

### SEO-роль

Главная — основной ВЧ-хаб и главная коммерческая посадочная сайта. Она одновременно продает услугу, объясняет типы решений и ведет пользователя в нужный интент: тип изделия, место монтажа, задачу, цену, гео или B2B.

### Основной кластер

- `moskitiery`
- `moskitiery na wymiar`
- `moskitiery z montażem`
- `moskitiery na zamówienie`
- `producent moskitier`
- `montaż moskitier`
- `moskitiery cena`
- `moskitiery do okien i drzwi`
- `moskitiery z pomiarem`

### Структура главной

- `Moskitiery na wymiar z pomiarem i montażem`
- `Wybierz miejsce montażu`
- `Wybierz typ moskitiery`
- `Najczęstsze potrzeby`
- `Moskitiery w aglomeracji katowickiej`
- `Cena i szybka wycena`
- `Pomiar i montaż`
- `Rozwiązania dla domu i firm`
- `FAQ`

### Основные переходы

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

### Пресет калькулятора

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

## 4. Типы конструкций

Эти страницы продают конкретную конструкцию. Пользователь уже знает или предполагает тип москитной сетки.

```txt
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-elektryczne/
/moskitiery-przemyslowe/
```

### Общая структура страницы типа

- `Co to jest`
- `Do czego pasuje`
- `Gdzie nie pasuje`
- `Warianty wykonania`
- `Rodzaje siatki kompatybilne z tym typem`
- `Cena`
- `Pomiar i montaż`
- `Montaż w aglomeracji katowickiej`
- `Kalkulator z presetem`
- `Powiązane miejsca montażu`
- `FAQ`

### Ключевые страницы

#### `/moskitiery-ramkowe/`

Кластер:

- `moskitiery ramkowe`
- `moskitiera ramkowa`
- `moskitiery okienne ramkowe`
- `moskitiera ramkowa cena`

Назначение: массовая оконная конструкция для стандартных окон. Вести в `/moskitiery-na-okna/`, `/moskitiery-dla-kota/`, `/cennik-moskitier/`.

#### `/moskitiery-drzwiowe/`

Кластер:

- `moskitiery drzwiowe`
- `moskitiera na drzwi`
- `moskitiera drzwiowa na zawiasach`
- `moskitiera drzwiowa z magnesem`

Назначение: распашные сетки на двери, где есть частый проход. Вести в `/moskitiery-na-drzwi-balkonowe/`, `/moskitiery-tarasowe/`, `/moskitiery-dla-kota/`.

#### `/moskitiery-rolowane/`

Кластер:

- `moskitiery rolowane`
- `moskitiera rolowana`
- `moskitiera w kasecie`
- `moskitiera rolowana cena`

Назначение: сетка, которая сворачивается в кассету.

Важно явно отсечь неверный интент:

```txt
Moskitiery rolowane nie są roletami zewnętrznymi. To siatki przeciw owadom zwijane do kasety, montowane w oknie lub drzwiach.
```

#### `/moskitiery-przesuwne/`

Кластер:

- `moskitiery przesuwne`
- `moskitiera przesuwna`
- `moskitiera do drzwi przesuwnych`
- `moskitiera do HST`
- `moskitiera do PSK`

Назначение: раздвижные системы, большие остекления, HST/PSK, террасные проходы. Вести в `/moskitiery-na-drzwi-przesuwne/`, `/moskitiery-tarasowe/`, `/moskitiery-plisowane/`.

#### `/moskitiery-plisowane/`

Кластер:

- `moskitiery plisowane`
- `moskitiera plisowana`
- `moskitiera plisowana tarasowa`
- `moskitiera plisowana cena`

Назначение: premium-решение для больших проходов, балконных и террасных дверей, HST/PSK. Усиливать высокий чек.

#### `/moskitiery-elektryczne/`

Кластер:

- `moskitiery elektryczne`
- `moskitiera elektryczna`
- `moskitiera sterowana pilotem`
- `moskitiera tarasowa elektryczna`
- `screen tarasowy z moskitierą`

Назначение: автоматизированные системы для больших проемов, пергол, террас, B2B и premium-домов. Вести в `/moskitiery-tarasowe/`, `/moskitiery-przemyslowe/`, `/pomiar-i-montaz-moskitier/`.

## 5. Промышленный и хозяйственный интент `/moskitiery-przemyslowe/`

### Решение по карте

Создается одна общая индексируемая страница:

```txt
/moskitiery-przemyslowe/
```

Отдельные страницы под `hala`, `magazyn`, `gastronomia`, `brama garażowa`, `świetlik dachowy`, `czerpnia` на первом этапе не создаются.

### Главный кластер

- `moskitiery przemysłowe`
- `moskitiera przemysłowa`
- `siatki przeciw owadom dla przemysłu`
- `siatki przeciw owadom do hal`
- `moskitiery do hal`
- `moskitiery do magazynów`
- `moskitiery do hal produkcyjnych`
- `moskitiery do hal chłodniczych`
- `moskitiery na bramy wjazdowe`
- `zabezpieczenie przed owadami dla firm`

### Секции внутри страницы

- `Bramy wjazdowe i garażowe`
- `Hale produkcyjne i magazyny`
- `Gastronomia i zaplecza kuchenne`
- `Świetliki dachowe i wentylacja`
- `Czerpnie, wentylatory, urządzenia techniczne`
- `Kurtyny PCV antyinsektowe jako alternatywa`

### Подача страницы

H1:

```txt
Moskitiery przemysłowe i siatki przeciw owadom dla firm
```

Страница должна быть обзорной B2B-посадочной с заявкой на индивидуальную выцену, а не бытовым калькулятором.

Пресет:

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

## 6. Места монтажа

Эти страницы подбирают решение по объекту установки. Пользователь знает место, но не всегда знает правильную конструкцию.

```txt
/moskitiery-na-okna/
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-drzwi-przesuwne/
/moskitiery-tarasowe/
/moskitiery-na-balkon/
```

### Что убрано из отдельных URL

Не создавать отдельно:

```txt
/moskitiery-na-okna-pcv/
/moskitiery-na-okna-drewniane/
/moskitiery-na-okna-aluminiowe/
/moskitiery-na-loggie/
```

Они закрываются блоками внутри основных страниц.

### `/moskitiery-na-okna/`

Кластер:

- `moskitiery na okna`
- `moskitiera na okno`
- `moskitiery okienne`
- `moskitiera okienna cena`
- `moskitiera na okno PCV`
- `moskitiera na okno drewniane`
- `moskitiera na okno aluminiowe`

Внутренние H2-блоки:

- `Moskitiery na okna PCV`
- `Moskitiery na okna drewniane`
- `Moskitiery na profile aluminiowe`

### `/moskitiery-na-drzwi-przesuwne/`

Кластер:

- `moskitiera do drzwi przesuwnych`
- `moskitiera do drzwi przesuwnych HST`
- `moskitiera przesuwna PSK`
- `moskitiera na duże okno tarasowe`
- `moskitiera do systemu HST`

Эта страница должна быть усилена как premium/high-ticket. В блоке `Czego nie wybierać` указать, что обычная распашная moskitiera drzwiowa часто не подходит для HST/PSK и больших террасных систем.

### `/moskitiery-tarasowe/`

Кластер:

- `moskitiery tarasowe`
- `moskitiera na taras`
- `moskitiera do drzwi tarasowych`
- `moskitiera do pergoli`

Рекомендуемые типы: `plisowane`, `przesuwne`, `elektryczne`.

## 7. Полотна и задачи

```txt
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/moskitiery-na-meszki/
/moskitiery-transparentne/
/moskitiery-antysmogowe/
```

### Общая структура

- `Dla kogo`
- `Co daje ten rodzaj siatki`
- `Z którymi typami moskitier jest kompatybilny`
- `Z którymi typami nie jest kompatybilny`
- `Cena i ograniczenia`
- `Kalkulator z presetem rodzaju siatki`
- `Powiązane typy i miejsca montażu`

### `/moskitiery-dla-kota/`

Кластер:

- `moskitiera dla kota`
- `moskitiera anti cat`
- `siatka dla kota na okno`
- `mocna moskitiera dla kota`

Совместимость:

```txt
Dobrze:
  /moskitiery-ramkowe/
  /moskitiery-drzwiowe/
  /moskitiery-przesuwne/

Ograniczenie:
  /moskitiery-rolowane/

Nie jako główny wariant:
  /moskitiery-plisowane/
  moskitiery magnetyczne
  moskitiery na rzep
```

## 8. Цена и монтаж

### `/cennik-moskitier/`

Кластер:

- `moskitiery cennik`
- `moskitiera cena`
- `ile kosztuje moskitiera`
- `moskitiery na wymiar cena`

Назначение: объяснить факторы цены, дать примеры и перевести в нужный тип/место монтажа.

### `/pomiar-i-montaz-moskitier/`

Кластер:

- `pomiar moskitier`
- `montaż moskitier`
- `moskitiery z montażem`
- `moskitiery z pomiarem`

Назначение: снять страх ошибки в размерах и продать замер/монтаж.

## 9. Geo SEO: aglomeracja katowicka

### Цель

Собрать локальный коммерческий трафик без размножения дублей `city + every service`.

### Индексируемые city landing pages

Первый этап:

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

Второй этап после проверки спроса:

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

Не создавать на старте:

```txt
/katowice/moskitiery-ramkowe/
/chorzow/moskitiery-plisowane/
/tychy/moskitiery-dla-kota/
/moskitiery-ramkowe-katowice/
/moskitiery-plisowane-chorzow/
```

### Кластер city landing

Для `/moskitiery-katowice/`:

- `moskitiery Katowice`
- `moskitiery na wymiar Katowice`
- `moskitiery z montażem Katowice`
- `moskitiery do okien Katowice`
- `moskitiery drzwiowe Katowice`
- `moskitiera Katowice cena`

Аналогично для остальных городов.

### Структура city landing

- `Moskitiery na wymiar w {city}`
- `Pomiar i montaż w {city}`
- `Najczęściej wybierane rozwiązania`
- `Moskitiery ramkowe, drzwiowe, plisowane, rolowane, dla kota`
- `Dzielnice / okolice / sąsiednie miejscowości`
- `Czas realizacji i warunki dojazdu`
- `Kalkulator z presetem city={city}`
- `FAQ lokalne`

City page ведет дальше в канонические страницы услуг с UX-параметром города:

```txt
/moskitiery-ramkowe/?city=katowice
/moskitiery-na-drzwi-balkonowe/?city=katowice
/moskitiery-na-drzwi-przesuwne/?city=katowice
/moskitiery-plisowane/?city=katowice
/moskitiery-dla-kota/?city=katowice
```

Эти параметрные URL не являются отдельными SEO-страницами.

## 10. UX geo-layer на коммерческих страницах

### Где используется

На всех коммерческих страницах:

```txt
/
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
```

### Структура модуля

Блок:

```txt
Montaż w aglomeracji katowickiej
```

Содержит:

- список городов;
- короткий локальный текст по выбранному городу;
- сроки/условия замера;
- локальный CTA;
- пресет калькулятора `city`;
- ссылку на индексируемую city landing, если она существует.

### Правила URL

Каноническая страница услуги:

```txt
/moskitiery-ramkowe/
```

UX-состояние:

```txt
/moskitiery-ramkowe/?city=katowice
```

Правила:

- canonical параметрной версии указывает на чистую страницу услуги;
- параметрные URL не попадают в sitemap;
- параметрные URL не считаются отдельной SEO-сеткой;
- основной гео-трафик собирают city landing pages формата `/moskitiery-{city}/`.

### Как не перегрузить страницу

Не раскрывать длинные тексты по всем городам сразу. Использовать компактный модуль:

- общий текст по агломерации;
- список городов;
- один активный город раскрыт;
- остальные города в компактном `details/accordion` или через интерактивный выбор;
- в HTML должен быть видимый список обслуживаемых городов.

Пример для `/moskitiery-ramkowe/`:

```txt
Moskitiery ramkowe z pomiarem w Katowicach, Chorzowie, Sosnowcu, Gliwicach, Zabrzu, Bytomiu, Rudzie Śląskiej i Tychach. Wybierz miasto, aby dopasować termin pomiaru i formularz wyceny.
```

## 11. Информационные страницы

Информационные страницы не размножаются по городам и не конкурируют с коммерческими страницами. Их задача: ответить на вопрос и перевести пользователя в коммерческий интент.

```txt
/jak-wybrac-moskitiere/
/jak-zmierzyc-okno-pod-moskitiere/
/moskitiera-ramkowa-czy-rolowana/
/moskitiera-plisowana-czy-przesuwna/
/jaka-moskitiera-dla-kota/
/jak-czyscic-i-myc-moskitiere/
/czy-sciagac-moskitiery-na-zime/
```

### Сезонные интенты

#### `/jak-czyscic-i-myc-moskitiere/`

Кластер:

- `jak umyć moskitierę`
- `czyszczenie moskitiery`
- `czyszczenie siatki na okno`
- `jak czyścić moskitierę ramkową`

Сезон: весна, начало сезона.

#### `/czy-sciagac-moskitiery-na-zime/`

Кластер:

- `czy ściągać moskitiery na zimę`
- `jak zdjąć moskitierę ramkową`
- `moskitiera na zimę`
- `przechowywanie moskitier`

Сезон: осень, конец сезона. Может вести в ремонт, замену полотна или новую покупку.

## 12. Навигационный flow

### Пользователь ищет общий продукт

```txt
/ -> выбор miejsca montażu / typu / miasta -> калькулятор или коммерческая страница
```

### Пользователь ищет город

```txt
Google: moskitiery Katowice
-> /moskitiery-katowice/
-> /moskitiery-ramkowe/?city=katowice
-> калькулятор с city=katowice
```

### Пользователь ищет место монтажа

```txt
/ -> /moskitiery-na-drzwi-przesuwne/ -> /moskitiery-plisowane/ -> заявка
```

### Пользователь ищет тип изделия

```txt
/ -> /moskitiery-ramkowe/ -> /moskitiery-na-okna/ -> калькулятор
```

### Пользователь ищет задачу

```txt
/ -> /moskitiery-dla-kota/ -> /moskitiery-ramkowe/ -> калькулятор с mesh=anti_cat
```

### Пользователь ищет premium/HST/PSK

```txt
/ -> /moskitiery-na-drzwi-przesuwne/ -> /moskitiery-plisowane/ или /moskitiery-przesuwne/ -> заявка на замер
```

### Пользователь ищет B2B

```txt
/ -> /moskitiery-przemyslowe/ -> заявка на индивидуальную wycenę
```

## 13. Правила против дублей

- Не создавать `/moskitiery/`, если главная является главным хабом.
- Не создавать отдельные страницы `PCV / drewniane / aluminiowe`; держать их блоками на `/moskitiery-na-okna/`.
- Не создавать city + service/product матрицу на старте.
- Создавать только city landing pages формата `/moskitiery-{city}/`.
- Для HST/PSK использовать `/moskitiery-na-drzwi-przesuwne/`, не плодить отдельные `/moskitiery-hst/` и `/moskitiery-psk/` на старте.
- Для `okna dachowe` использовать одну страницу `/moskitiery-na-okna-dachowe/`.
- Для промышленного интента использовать одну страницу `/moskitiery-przemyslowe/`.
- Для калькулятора не создавать отдельную SEO-страницу.

## 14. Итоговая карта URL

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

## 15. Второй этап расширения

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
