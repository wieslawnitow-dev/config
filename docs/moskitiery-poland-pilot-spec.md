# ТЗ: посадочные страницы для moskitiery в Польше

## 1. Назначение документа

Документ описывает SEO-структуру и клиентский flow для польской версии нишевого сайта по москитным сеткам (`moskitiery`) с калькулятором на каждой коммерческой странице.

Основной язык сайта: польский.

Документ написан по-русски для проектирования, но URL, названия интентов, блоков и видимые пользовательские категории должны использовать польскую терминологию.

## 2. Базовые принципы

- Калькулятор не имеет отдельной основной SEO-страницы.
- Калькулятор размещается на каждой коммерческой странице и получает преднастройки из интента страницы.
- Индексируемые страницы создаются под чистые интенты: главная, общий хаб, тип изделия, место монтажа, тип полотна/задача, цена, монтаж, информационные страницы.
- Пересечения интентов не плодятся автоматически как отдельные URL. Например `miasto + typ + miejsce + siatka` закрывается блоками, пресетами калькулятора и внутренними переходами.
- Гео может использоваться как слой интерфейса и калькулятора, но базовая карта ниже описывает интенты без размножения по городам.
- Все внутренние названия на сайте должны быть польскими: `Miejsce montażu`, `Typ moskitiery`, `Rodzaj siatki`, `Zastosowanie`, `Cena`, `Pomiar i montaż`.

## 3. Главная страница `/`

### SEO-роль

Главная страница закрывает самый широкий коммерческий интент и вводит пользователя в выбор решения.

Главная не должна быть дублем `/moskitiery/`. Она отвечает за общий оффер бизнеса: москитные сетки на заказ, замер, изготовление, монтаж, сервисный регион, доверие и быстрый выбор направления.

### Основной кластер

- `moskitiery na wymiar`
- `moskitiery z montażem`
- `moskitiery na zamówienie`
- `producent moskitier`
- `montaż moskitier`
- `moskitiery do okien i drzwi`
- `moskitiery cena`
- `moskitiery z pomiarem`

### Интент пользователя

Пользователь еще не всегда знает тип изделия. Он хочет понять, что можно заказать, сколько примерно стоит, подходит ли решение к его окну/двери/ tarasowi и как быстро получить расчет.

### Основные блоки

- `Moskitiery na wymiar z pomiarem i montażem`
- `Wybierz miejsce montażu`
- `Wybierz typ moskitiery`
- `Najczęstsze potrzeby`
- `Cena i szybka wycena`
- `Pomiar i montaż`
- `Obsługiwane lokalizacje`
- `FAQ`

### Ссылки с главной

```txt
/moskitiery/
/moskitiery-na-okna/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-tarasowe/
/moskitiery-na-okna-dachowe/
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-plisowane/
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/cennik-moskitier/
/pomiar-i-montaz-moskitier/
```

### Пресет калькулятора

```json
{
  "intent": "home",
  "product": null,
  "mountPlace": null,
  "mesh": null,
  "mode": "guided_selection"
}
```

## 4. Общий хаб `/moskitiery/`

### SEO-роль

`/moskitiery/` является главным тематическим хабом по категории `moskitiery`.

Если главная продает бизнес и быстрый вход в заказ, то `/moskitiery/` системно объясняет категорию: какие бывают москитные сетки, куда ставятся, чем отличаются, какие варианты подходят под разные задачи.

### Основной кластер

- `moskitiery`
- `moskitiera`
- `rodzaje moskitier`
- `jakie moskitiery wybrać`
- `moskitiery okienne`
- `moskitiery drzwiowe`
- `moskitiery na wymiar`
- `moskitiery do domu`
- `moskitiery do mieszkania`
- `moskitiery do okien i drzwi`

### Интент пользователя

Пользователь изучает категорию или сравнивает варианты. Он может быть как в информационном, так и в коммерческом интенте. Страница должна переводить его в конкретные типы изделий, места монтажа и задачи.

### Основные блоки

- `Rodzaje moskitier`
- `Miejsce montażu`
- `Rodzaj siatki`
- `Która moskitiera pasuje do Twojego okna lub drzwi?`
- `Cena i czynniki wpływające na wycenę`
- `Pomiar i montaż`
- `Najczęstsze pytania`

### Ссылки с `/moskitiery/`

```txt
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-elektryczne/
/moskitiery-na-okna/
/moskitiery-na-okna-pcv/
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-tarasowe/
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/cennik-moskitier/
```

### Пресет калькулятора

```json
{
  "intent": "category_hub",
  "product": null,
  "mountPlace": null,
  "mesh": null,
  "mode": "compare_and_select"
}
```

## 5. Страницы по типу изделия

Эти страницы продают конкретную конструкцию. Пользователь уже знает или подозревает, какой тип москитной сетки ему нужен.

### Карта

```txt
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-elektryczne/
```

### Общая структура страницы типа изделия

- `Co to jest`
- `Do czego pasuje`
- `Gdzie nie pasuje`
- `Warianty wykonania`
- `Rodzaje siatki kompatybilne z tym typem`
- `Cena`
- `Pomiar i montaż`
- `Kalkulator z presetem`
- `Powiązane miejsca montażu`
- `FAQ`

### Пресеты и перелинковка

#### `/moskitiery-ramkowe/`

Кластер:

- `moskitiery ramkowe`
- `moskitiera ramkowa`
- `moskitiery okienne ramkowe`
- `moskitiera ramkowa cena`

Целевое использование: стандартные окна, особенно PCV.

Покупатель: хочет простое, надежное и относительно недорогое решение.

Ссылки:

```txt
/moskitiery-na-okna/
/moskitiery-na-okna-pcv/
/moskitiery-dla-kota/
/moskitiery-przeciwpylkowe/
/cennik-moskitier/
```

Пресет:

```json
{
  "intent": "product_type",
  "product": "ramkowa",
  "allowedMountPlaces": ["okno", "okno_pcv", "okno_drewniane", "okno_aluminiowe"],
  "excludedMountPlaces": ["taras", "okno_dachowe", "duze_przejscie"]
}
```

#### `/moskitiery-drzwiowe/`

Кластер:

- `moskitiery drzwiowe`
- `moskitiera na drzwi`
- `moskitiera drzwiowa na zawiasach`
- `moskitiera drzwiowa z magnesem`

Целевое использование: двери balkonowe, tarasowe, wejściowe, gospodarcze.

Покупатель: хочет часто проходить через проем без снятия сетки.

Ссылки:

```txt
/moskitiery-na-drzwi-balkonowe/
/moskitiery-tarasowe/
/moskitiery-dla-kota/
/pomiar-i-montaz-moskitier/
```

#### `/moskitiery-rolowane/`

Кластер:

- `moskitiery rolowane`
- `moskitiera rolowana`
- `moskitiera w kasecie`
- `moskitiera rolowana cena`

Целевое использование: окна, двери, okna dachowe, места, где сетку нужно убирать в кассету.

Покупатель: хочет удобство и эстетичный вид.

Ссылки:

```txt
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-okna/
/moskitiery-elektryczne/
```

#### `/moskitiery-przesuwne/`

Кластер:

- `moskitiery przesuwne`
- `moskitiera przesuwna`
- `moskitiera do drzwi przesuwnych`
- `moskitiera do HST`

Целевое использование: drzwi przesuwne, systemy HS/HST, loggie, duże przeszklenia.

Покупатель: имеет нестандартное или крупное остекление.

Ссылки:

```txt
/moskitiery-na-drzwi-przesuwne/
/moskitiery-tarasowe/
/moskitiery-plisowane/
```

#### `/moskitiery-plisowane/`

Кластер:

- `moskitiery plisowane`
- `moskitiera plisowana`
- `moskitiera plisowana tarasowa`
- `moskitiera plisowana cena`

Целевое использование: taras, balkon, duże drzwi, drzwi przesuwne, premium.

Покупатель: хочет удобное и эстетичное решение для большого проема.

Ссылки:

```txt
/moskitiery-tarasowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-drzwi-przesuwne/
/moskitiery-przesuwne/
```

#### `/moskitiery-elektryczne/`

Кластер:

- `moskitiery elektryczne`
- `moskitiera elektryczna`
- `moskitiera sterowana pilotem`
- `moskitiera tarasowa elektryczna`
- `screen tarasowy z moskitierą`

Целевое использование: tarasy, pergole, duże przejścia, domy premium, lokale.

Покупатель: высокий чек, ожидает автоматику, удобство и интеграцию.

Ссылки:

```txt
/moskitiery-tarasowe/
/moskitiery-rolowane/
/pomiar-i-montaz-moskitier/
```

## 6. Страницы по месту монтажа

Эти страницы подбирают решение по объекту установки. Пользователь не обязан знать тип москитной сетки.

### Карта

```txt
/moskitiery-na-okna/
/moskitiery-na-okna-pcv/
/moskitiery-na-okna-drewniane/
/moskitiery-na-okna-aluminiowe/
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-balkon/
/moskitiery-na-loggie/
/moskitiery-tarasowe/
/moskitiery-na-drzwi-przesuwne/
```

### Общая структура страницы места монтажа

- `Jaki problem rozwiązuje ta strona`
- `Najlepsze typy moskitier dla tego miejsca`
- `Czego nie wybierać`
- `Wymiary i ograniczenia`
- `Polecane rodzaje siatki`
- `Cena`
- `Kalkulator z presetem miejsca montażu`
- `Powiązane typy moskitier`
- `FAQ`

### Примеры

#### `/moskitiery-na-okna/`

Кластер:

- `moskitiery na okna`
- `moskitiera na okno`
- `moskitiery okienne`
- `moskitiera okienna cena`

Рекомендуемые типы:

```txt
/moskitiery-ramkowe/
/moskitiery-rolowane/
```

Пресет:

```json
{
  "intent": "mount_place",
  "mountPlace": "okno",
  "recommendedProducts": ["ramkowa", "rolowana"],
  "defaultProduct": "ramkowa"
}
```

#### `/moskitiery-na-okna-dachowe/`

Кластер:

- `moskitiera na okno dachowe`
- `moskitiery na okna dachowe`
- `moskitiera do okna dachowego`

Рекомендуемые типы:

```txt
/moskitiery-rolowane/
/moskitiery-plisowane/
```

Не вести в рамковые как основной вариант.

#### `/moskitiery-na-drzwi-balkonowe/`

Кластер:

- `moskitiera na drzwi balkonowe`
- `moskitiery na drzwi balkonowe`
- `moskitiera balkonowa drzwiowa`

Рекомендуемые типы:

```txt
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-plisowane/
```

#### `/moskitiery-tarasowe/`

Кластер:

- `moskitiery tarasowe`
- `moskitiera na taras`
- `moskitiera do drzwi tarasowych`
- `moskitiera do pergoli`

Рекомендуемые типы:

```txt
/moskitiery-plisowane/
/moskitiery-przesuwne/
/moskitiery-elektryczne/
```

Коммерческий акцент: высокий чек, большие размеры, удобство, premium.

## 7. Страницы по типу полотна и задаче

Эти страницы закрывают не конструкцию, а причину покупки.

### Карта

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

### Пример `/moskitiery-dla-kota/`

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

Назначение: объяснить цену, показать диапазоны, дать калькулятор и перевести в тип/место монтажа.

Ссылки:

```txt
/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-plisowane/
/moskitiery-tarasowe/
/moskitiery-na-okna-dachowe/
```

### `/pomiar-i-montaz-moskitier/`

Кластер:

- `pomiar moskitier`
- `montaż moskitier`
- `moskitiery z montażem`
- `moskitiery z pomiarem`

Назначение: снять страх ошибки в размерах и продать выезд/монтаж.

Ссылки:

```txt
/moskitiery-na-okna/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-tarasowe/
/moskitiery-na-okna-dachowe/
```

## 9. Информационные страницы

Информационные страницы не размножаются по городам и не конкурируют с коммерческими страницами. Их задача: ответить на вопрос и перевести пользователя в коммерческий интент.

### Карта

```txt
/jak-wybrac-moskitiere/
/jak-zmierzyc-okno-pod-moskitiere/
/moskitiera-ramkowa-czy-rolowana/
/moskitiera-plisowana-czy-przesuwna/
/jaka-moskitiera-dla-kota/
/moskitiera-na-okno-dachowe-jaka-wybrac/
/jak-dbac-o-moskitiere/
```

### Flow информационной страницы

- Короткий ответ на вопрос.
- 2-3 подходящих варианта.
- Блок `Najlepsze rozwiązania`.
- Ссылка на коммерческие страницы.
- Калькулятор с мягким пресетом.

Пример:

```txt
/jak-zmierzyc-okno-pod-moskitiere/
  -> /moskitiery-ramkowe/
  -> /pomiar-i-montaz-moskitier/
  -> /cennik-moskitier/
```

## 10. Навигационный flow на страницах

На каждой коммерческой странице должны быть блоки следующего перехода.

### Блок `Miejsce montażu`

```txt
Okna
Okna PCV
Okna drewniane
Okna aluminiowe
Okna dachowe
Drzwi balkonowe
Balkon
Loggia
Taras
Drzwi przesuwne
```

### Блок `Typ moskitiery`

```txt
Ramkowe
Drzwiowe
Rolowane
Przesuwne
Plisowane
Elektryczne
```

### Блок `Rodzaj siatki`

```txt
Standardowa
Dla kota
Przeciwpyłkowa
Na meszki
Transparentna
Antysmogowa
```

### Блок `Najczęstsze potrzeby`

```txt
Do mieszkania
Do domu
Na balkon
Na taras
Dla kota
Dla alergika
Do okna dachowego
Do dużego przejścia
```

## 11. Примеры пользовательских flow

### Пользователь ищет место установки

```txt
/ -> /moskitiery-na-drzwi-balkonowe/ -> /moskitiery-plisowane/ -> форма заявки
```

Логика: пользователь знает место, но не знает конструкцию. Страница места монтажа подбирает лучший тип.

### Пользователь ищет тип изделия

```txt
/ -> /moskitiery-ramkowe/ -> /moskitiery-na-okna-pcv/ -> калькулятор
```

Логика: пользователь уже знает тип, нужно подтвердить применимость и рассчитать цену.

### Пользователь ищет задачу

```txt
/ -> /moskitiery-dla-kota/ -> /moskitiery-ramkowe/ -> калькулятор с mesh=anti_cat
```

Логика: пользователь покупает не конструкцию, а безопасность для животного.

### Пользователь ищет premium-решение

```txt
/ -> /moskitiery-tarasowe/ -> /moskitiery-plisowane/ или /moskitiery-elektryczne/ -> заявка на замер
```

Логика: здесь нужно усиливать чек через комфорт, большие размеры, эстетику и автоматику.

## 12. Правила против дублей

- Не создавать отдельную страницу, если интент уже закрыт сильной страницей.
- Не дублировать `moskitiery-drzwiowe` и `moskitiery-na-drzwi`, если они отвечают на один и тот же запрос.
- Для дверей использовать основную страницу `/moskitiery-drzwiowe/`, а для конкретного места создавать `/moskitiery-na-drzwi-balkonowe/` и `/moskitiery-na-drzwi-przesuwne/`.
- Для `okna dachowe` использовать одну страницу `/moskitiery-na-okna-dachowe/`, не плодить дубль `moskitiery-na-dach`.
- Для калькулятора не создавать отдельную SEO-страницу, если он уже встроен во все коммерческие страницы.

## 13. Итоговая карта

```txt
/
/moskitiery/
/cennik-moskitier/
/pomiar-i-montaz-moskitier/
/kontakt/

/moskitiery-ramkowe/
/moskitiery-drzwiowe/
/moskitiery-rolowane/
/moskitiery-przesuwne/
/moskitiery-plisowane/
/moskitiery-elektryczne/

/moskitiery-na-okna/
/moskitiery-na-okna-pcv/
/moskitiery-na-okna-drewniane/
/moskitiery-na-okna-aluminiowe/
/moskitiery-na-okna-dachowe/
/moskitiery-na-drzwi-balkonowe/
/moskitiery-na-balkon/
/moskitiery-na-loggie/
/moskitiery-tarasowe/
/moskitiery-na-drzwi-przesuwne/

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
/moskitiera-na-okno-dachowe-jaka-wybrac/
/jak-dbac-o-moskitiere/
```
