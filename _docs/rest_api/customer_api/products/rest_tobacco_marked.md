---
title: Маркированный табак
permalink: rest_tobacco_marked.html
sidebar: evorestreference
product: Customer API
---


Схема товара с типом `TOBACCO_MARKED`.

{% include important.html content="В связи с изменением законодательства, с первого января 2019 года значения `VAT_18` и `VAT_18_118` могут указывать как на 18%, так и на 20% ставку НДС." %}

```json
{
  "parent_id": "1ddea16b-971b-dee5-3798-1b29a7aa2e27",
  "name": "Сидр",
  "measure_name": "шт",
  "tax": "VAT_18",
  "allow_to_sell": true,
  "price": 123.12,
  "description": "Вкусный яблочный сидр",
  "article_number": "СДР-ЯБЛЧ",
  "code": "42",
  "barcodes": [
    "2000000000060"
  ],
  "type": "TOBACCO_MARKED",
  "id": "01ba18b6-8707-5f47-3d9c-4db058054cb2",
  "quantity": 12,
  "cost_price": 100.123,
  "attributes_choices": {},
  "store_id": "20180820-7052-4047-807D-E82C50000000",
  "user_id": "00-000000000000000",
  "created_at": "2018-09-11T16:18:35.397+0000",
  "updated_at": "2018-09-11T16:18:35.397+0000"
}
```

## Описание

Имя  | Тип  | Описание
-----|------|--------------
`parent_id`| `string` | *Необязательный*. Уникальный идентификатор группы или группы модификаций, к которой иерархически привязан товар или модификация товара. Если элемент номенклатуры находится в корне иерархии, то данное свойство не указывается.
`name`| `string` |  Название товара или модификации товара. До 128 символов.
`measure_name`| `string` |  Единица измерения для товара или модификации товара. Возможные значения: `шт`, `кг`, `л`, `м`, `км`, `м2`, `м3`, `компл`, `упак`, `ед`, `дроб`. Товароучётные системы могут задавать свои единицы измерения, например: "пара", "палета", "карат" и т.д.
`tax`| `string` |  Код ставки НДС для товара или модификации товара. Возможные значения: `NO_VAT` – без НДС; `VAT_0` – основная ставка 0%; `VAT_10` – основная ставка 10%; `VAT_10_110` – расчётная ставка 10%; `VAT_18` – основная ставка 18%; `VAT_18_118` – расчётная ставка 18%.
`allow_to_sell`| `boolean` |  Признак разрешения продажи. Указывает можно добавить товар в чек или нет: `true` - товар можно добавить в чек; `false` - товар нельзя добавить в чек.
`price`| `number` |  Отпускная цена товара или модификации товара.
`description`| `string` |  *Необязательный*. Описание товара или модификации товара.
`article_number`| `string` |  *Необязательный*. Артикул товара или модификации товара. До 20 символов.
`code`| `string` |  *Необязательный*. Код товара или модификации товара. До 10 символов.
`barcodes`| `array` |  *Необязательный*. Массив штрихкодов для товара, модификации товара или группы модификаций.
`type`| `string` |  Тип товара или модификации товара. Возможные значения: `NORMAL` – обычный; `ALCOHOL_MARKED` – маркированный алкоголь; `ALCOHOL_NOT_MARKED` – немаркированный алкоголь; `TOBACCO_MARKED` – маркированный табак; `SERVICE` – услуга.
`id`| `string` |  Идентификатор товара, уникальный в рамках магазина.
`quantity`| `number` |  *Необязательный*. Доступный к продаже остаток товара или модификации товара. До семи знаков в целой и трёх знаков в дробной части. Присутствует в схеме только если приложение имеет права на работу с остатками.
`cost_price`| `number` |  *Необязательный*. Закупочная цена товара или модификации товара.
`attributes_choices`| `object` |  *Необязательный*. Описание характеристик, которые применяются к модификации товара. Содержит объект, в котором ключи это идентификаторы характеристик, а значения - идентификаторы значений характеристик. Применимо только в случае, если элемент номенклатуры в иерархии является потомком группы модификаций товаров.
`store_id`| `string` | Идентификатор магазина, в базе которого хранится товар.
`user_id`| `string` | Идентификатор пользователя Эвотор, которому принадлежит смарт-терминал.
`created_at`| `string` | Время создания товара.
`updated_at`| `string` | Время обновления информации о товаре.