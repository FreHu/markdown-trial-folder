## 09:15:54 · bikes-prod / bikeshare_prod (read-only) · rides and revenue per day

```sql
select date(started_at) day, count(*) rides, sum(price) revenue_czk from ride group by day order by day desc limit 24
```

| day | rides | revenue_czk |
|---|---|---|
| 2026-10-30 | 1124 | 20901.05 |
| 2026-10-29 | 3012 | 13982.52 |
| 2026-10-28 | 2860 | 5562.16 |
| 2026-10-27 | 948 | 26596.06 |
| 2026-10-26 | 2747 | 16927.34 |
| 2026-10-25 | 3029 | 28973.07 |
| 2026-10-24 | 3992 | 13633.78 |
| 2026-10-23 | 1651 | 15640.31 |
| 2026-10-22 | 4052 | 30167.81 |
| 2026-10-21 | 1208 | 16546.74 |
| 2026-10-20 | 1501 | 30819.26 |
| 2026-10-19 | 1423 | 10206.39 |
| 2026-10-18 | 3571 | 19226.21 |
| 2026-10-17 | 2168 | 21212.10 |
| 2026-10-16 | 3957 | 26586.36 |
| 2026-10-15 | 1011 | 20707.88 |
| 2026-10-14 | 2059 | 27917.76 |
| 2026-10-13 | 2616 | 21731.29 |
| 2026-10-12 | 4076 | 32781.22 |

_19 rows · 1.6 s_

## 09:18:42 · bikes-test / bikeshare_test (read-only) · select id, meta from station where meta is not null limit 5

```sql
select id, meta from station where meta is not null limit 5
```

| id | meta |
|---|---|
| 75 | {"station":"Nové sady","docks":11,"lat":49.22818,"lon":16.62784,"notes":"Přední světlo nesvítí, za tmy se nedá jet.","contacts":["Zuzana Pokorná","Petr Novotný"]} |
| 74 | {"station":"Žabovřesky","docks":30,"lat":49.20946,"lon":16.60457,"notes":"Servis slíbil opravu do pátku 30. října.","contacts":["Zuzana Pokorná","Tomáš Král"]} |
| 63 | {"station":"Moravské náměstí","docks":29,"lat":49.22858,"lon":16.64396,"notes":"Prosím o vrácení poplatku 49 Kč za nedokončenou jízdu.","contacts":["Eva Horáková","Ondřej Marek"]} |

_3 rows · 1.8 s_

## 09:22:46 · dispatch-test (read-only) · select table_name, column_name from information_schema.columns where table_schema = 'public' and column_name i…

```sql
select table_name, column_name from information_schema.columns where table_schema = 'public' and column_name ilike '%recipe%'
```

| table_name | column_name |
|---|---|
| recipes | recipe |
| workflows | code_body |
| runs | recipe_json |
| recipes | recipe |
| recipes | recipe_json |
| run_steps | recipe_json |
| workflows | code_body |
| run_steps | recipe |
| run_steps | code_body |
| recipes | input_template |
| runs | code_body |
| run_steps | recipe |
| runs | recipe_version |
| workflows | recipe_version |
| workflows | recipe_version |
| run_steps | recipe_json |
| run_steps | recipe |
| workflow_actions | recipe_version |
| workflows | recipe_json |
| runs | recipe_json |
| runs | code_body |
| run_steps | input_template |

_22 rows · 1.2 s_

## 09:23:55 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 205906 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/9563?tab=history"},{"type":"string","title":"Searched","value":"ride 137355: 1 found"},{"type":"multiline","title":"Ticket… |

_1 rows · 0.6 s_

## 09:30:29 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Klára Veselá | company |
| Petr Novotný | company |
| Klára Veselá | student |

_3 rows · 0.4 s_

## 09:36:42 · bikes-prod / bikeshare_prod (read-only) · rides and revenue per day

```sql
select date(started_at) day, count(*) rides, sum(price) revenue_czk from ride group by day order by day desc limit 24
```

| day | rides | revenue_czk |
|---|---|---|
| 2026-10-30 | 983 | 34573.95 |
| 2026-10-29 | 3858 | 26319.41 |
| 2026-10-28 | 2078 | 32935.18 |
| 2026-10-27 | 1212 | 30296.34 |
| 2026-10-26 | 1689 | 5159.79 |
| 2026-10-25 | 3724 | 7363.87 |
| 2026-10-24 | 1310 | 8066.43 |
| 2026-10-23 | 1631 | 27661.29 |
| 2026-10-22 | 3361 | 14710.70 |
| 2026-10-21 | 3471 | 10757.91 |
| 2026-10-20 | 2320 | 27568.92 |
| 2026-10-19 | 3182 | 28505.93 |
| 2026-10-18 | 2182 | 13967.56 |
| 2026-10-17 | 2388 | 32833.80 |
| 2026-10-16 | 837 | 22817.68 |
| 2026-10-15 | 1774 | 22821.79 |
| 2026-10-14 | 1708 | 14452.47 |
| 2026-10-13 | 3735 | 19780.13 |

_18 rows · 0.9 s_

## 09:42:47 · bikes-prod / bikeshare_prod (read-only) · rides and revenue per day

```sql
select date(started_at) day, count(*) rides, sum(price) revenue_czk from ride group by day order by day desc limit 24
```

| day | rides | revenue_czk |
|---|---|---|
| 2026-10-30 | 3051 | 14634.71 |
| 2026-10-29 | 2098 | 28887.72 |
| 2026-10-28 | 1140 | 17588.14 |
| 2026-10-27 | 989 | 20587.95 |
| 2026-10-26 | 1497 | 13263.67 |
| 2026-10-25 | 1671 | 6348.71 |
| 2026-10-24 | 2432 | 34664.58 |
| 2026-10-23 | 3076 | 12687.60 |
| 2026-10-22 | 3083 | 17729.29 |
| 2026-10-21 | 1621 | 5876.76 |
| 2026-10-20 | 2567 | 14981.34 |
| 2026-10-19 | 1877 | 28171.06 |
| 2026-10-18 | 2719 | 26968.23 |
| 2026-10-17 | 3656 | 22751.02 |
| 2026-10-16 | 3505 | 23352.70 |
| 2026-10-15 | 3198 | 9389.70 |
| 2026-10-14 | 2345 | 25334.34 |
| 2026-10-13 | 1314 | 31835.18 |
| 2026-10-12 | 2485 | 25393.44 |

_19 rows · 2.2 s_

## 09:46:00 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1040 | flat tyre | 2026-10-01 |
| 1144 | brake | 2026-10-30 |
| 1502 | kickstand | 2026-10-05 |
| 1233 | brake | 2026-10-15 |
| 1497 | saddle | 2026-10-25 |
| 1333 | brake | 2026-10-24 |
| 1341 | saddle | 2026-10-25 |
| 1675 | chain | 2026-10-06 |
| 1614 | kickstand | 2026-10-01 |
| 1344 | display | 2026-10-27 |
| 1930 | lock | 2026-10-20 |
| 1681 | saddle | 2026-10-29 |
| 1317 | display | 2026-10-16 |
| 1451 | saddle | 2026-10-02 |
| 1342 | chain | 2026-10-12 |
| 1505 | flat tyre | 2026-10-08 |
| 1769 | brake | 2026-10-16 |
| 1888 | brake | 2026-10-29 |
| 1559 | brake | 2026-10-04 |
| 1646 | flat tyre | 2026-10-08 |
| 1461 | display | 2026-10-25 |
| 1026 | kickstand | 2026-10-02 |
| 1187 | bell | 2026-10-12 |
| 1463 | battery | 2026-10-21 |
| 1684 | kickstand | 2026-10-19 |
| 1900 | lock | 2026-10-08 |
| 1575 | saddle | 2026-10-19 |
| 1074 | saddle | 2026-10-26 |
| 1193 | chain | 2026-10-19 |
| 1219 | display | 2026-10-27 |
| 1588 | lock | 2026-10-20 |
| 1081 | light | 2026-10-05 |
| 1631 | flat tyre | 2026-10-16 |
| 1202 | chain | 2026-10-23 |
| 1649 | display | 2026-10-29 |
| 1601 | brake | 2026-10-05 |
| 1120 | kickstand | 2026-10-05 |
| 1923 | bell | 2026-10-02 |
| 1593 | flat tyre | 2026-10-29 |
| 1452 | saddle | 2026-10-08 |
| 1394 | bell | 2026-10-18 |
| 1658 | lock | 2026-10-03 |

_42 rows · 2.5 s_

## 09:46:43 · bikes-prod / bikeshare_prod (read-only) · rides and revenue per day

```sql
select date(started_at) day, count(*) rides, sum(price) revenue_czk from ride group by day order by day desc limit 24
```

| day | rides | revenue_czk |
|---|---|---|
| 2026-10-30 | 3997 | 24314.97 |
| 2026-10-29 | 1970 | 28495.61 |
| 2026-10-28 | 3074 | 30060.59 |
| 2026-10-27 | 2517 | 17137.35 |
| 2026-10-26 | 1962 | 29357.23 |
| 2026-10-25 | 3511 | 24261.75 |
| 2026-10-24 | 1585 | 9958.81 |
| 2026-10-23 | 2887 | 30176.02 |
| 2026-10-22 | 3484 | 15484.84 |
| 2026-10-21 | 3218 | 5283.86 |
| 2026-10-20 | 2933 | 31643.24 |
| 2026-10-19 | 3608 | 34410.94 |
| 2026-10-18 | 3556 | 6181.17 |
| 2026-10-17 | 1674 | 25696.24 |
| 2026-10-16 | 3903 | 33206.80 |
| 2026-10-15 | 2850 | 11771.36 |
| 2026-10-14 | 3063 | 10555.21 |
| 2026-10-13 | 3915 | 6153.22 |
| 2026-10-12 | 3264 | 5134.07 |
| 2026-10-11 | 1041 | 7514.53 |
| 2026-10-10 | 3251 | 28937.50 |
| 2026-10-09 | 2045 | 12302.77 |

_22 rows · 1.5 s_

## 09:50:31 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Tomáš Král | student |
| Tomáš Král | student |
| Petr Novotný | senior |
| Petr Novotný | senior |
| Jakub Fiala | student |
| Martin Procházka | company |
| Eva Horáková | student |

_7 rows · 0.9 s_

## 09:55:03 · bikes-prod / bikeshare_prod (read-only) · free docks per station

```sql
select s.name, count(*) free_docks
from dock d join station s on s.id = d.station_id
where d.bike_id is null group by s.name order by free_docks desc
```

| name | free_docks |
|---|---|
| Náměstí Míru | 3 |
| Hlavní nádraží | 24 |
| Výstaviště | 2 |
| Mendlovo náměstí | 23 |
| Lužánky | 9 |
| Královo Pole | 13 |
| Žabovřesky | 21 |
| Komárov | 4 |

_8 rows · 0.9 s_

## 09:56:52 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1455 | lock | 2026-10-21 |
| 1418 | bell | 2026-10-27 |
| 1851 | chain | 2026-10-02 |
| 1003 | bell | 2026-10-06 |
| 1394 | chain | 2026-10-02 |
| 1242 | saddle | 2026-10-04 |
| 1855 | flat tyre | 2026-10-21 |
| 1984 | lock | 2026-10-30 |
| 1764 | display | 2026-10-14 |
| 1286 | battery | 2026-10-30 |
| 1512 | chain | 2026-10-26 |
| 1165 | chain | 2026-10-22 |
| 1739 | light | 2026-10-11 |
| 1438 | kickstand | 2026-10-12 |
| 1780 | chain | 2026-10-28 |
| 1247 | display | 2026-10-20 |
| 1995 | brake | 2026-10-21 |
| 1666 | flat tyre | 2026-10-09 |
| 1544 | battery | 2026-10-29 |
| 1054 | battery | 2026-10-08 |
| 1542 | kickstand | 2026-10-18 |
| 1285 | flat tyre | 2026-10-26 |
| 1976 | saddle | 2026-10-04 |
| 1322 | brake | 2026-10-01 |
| 1928 | bell | 2026-10-26 |
| 1256 | bell | 2026-10-04 |
| 1355 | saddle | 2026-10-29 |
| 1302 | saddle | 2026-10-23 |
| 1358 | battery | 2026-10-04 |
| 1619 | flat tyre | 2026-10-11 |
| 1171 | lock | 2026-10-21 |
| 1900 | display | 2026-10-07 |
| 1774 | bell | 2026-10-02 |
| 1457 | kickstand | 2026-10-11 |
| 1280 | saddle | 2026-10-12 |
| 1484 | battery | 2026-10-16 |
| 1319 | lock | 2026-10-30 |
| 1456 | kickstand | 2026-10-03 |
| 1683 | chain | 2026-10-28 |
| 1812 | brake | 2026-10-07 |
| 1609 | chain | 2026-10-03 |
| 1940 | kickstand | 2026-10-08 |
| 1807 | kickstand | 2026-10-15 |
| 1120 | chain | 2026-10-23 |
| 1490 | bell | 2026-10-19 |
| 1488 | lock | 2026-10-18 |
| 1436 | bell | 2026-10-09 |
| 1049 | chain | 2026-10-29 |
| 1439 | display | 2026-10-16 |
| 1090 | lock | 2026-10-11 |
| 1547 | light | 2026-10-03 |
| 1905 | lock | 2026-10-01 |
| 1454 | battery | 2026-10-02 |
| 1509 | light | 2026-10-18 |
| 1005 | display | 2026-10-09 |
| 1960 | lock | 2026-10-16 |
| 1044 | kickstand | 2026-10-30 |
| 1051 | lock | 2026-10-26 |
| 1261 | saddle | 2026-10-17 |
| 1242 | flat tyre | 2026-10-06 |
| 1691 | lock | 2026-10-12 |
| 1963 | battery | 2026-10-09 |
| 1549 | flat tyre | 2026-10-03 |
| 1744 | brake | 2026-10-10 |
| 1792 | display | 2026-10-02 |
| 1100 | bell | 2026-10-04 |
| 1169 | flat tyre | 2026-10-03 |
| 1501 | lock | 2026-10-13 |
| 1746 | kickstand | 2026-10-18 |
| 1962 | flat tyre | 2026-10-06 |
| 1369 | bell | 2026-10-01 |
| 1957 | light | 2026-10-08 |

_72 rows · 0.3 s_

## 09:57:11 · bikes-prod / bikeshare_prod (read-only) · rides and revenue per day

```sql
select date(started_at) day, count(*) rides, sum(price) revenue_czk from ride group by day order by day desc limit 24
```

| day | rides | revenue_czk |
|---|---|---|
| 2026-10-30 | 2463 | 5108.47 |
| 2026-10-29 | 1852 | 34494.75 |
| 2026-10-28 | 1276 | 34472.42 |
| 2026-10-27 | 3247 | 24693.89 |
| 2026-10-26 | 2584 | 7802.58 |
| 2026-10-25 | 2664 | 10414.85 |
| 2026-10-24 | 3454 | 8402.30 |
| 2026-10-23 | 2696 | 8328.12 |
| 2026-10-22 | 1420 | 6397.23 |
| 2026-10-21 | 2939 | 5563.07 |
| 2026-10-20 | 1163 | 24675.82 |
| 2026-10-19 | 1019 | 15185.94 |
| 2026-10-18 | 3681 | 10856.64 |
| 2026-10-17 | 1135 | 33561.21 |
| 2026-10-16 | 2234 | 28264.48 |
| 2026-10-15 | 2679 | 19437.19 |

_16 rows · 1.1 s_

## 10:01:53 · bikes-prod / bikeshare_prod (read-only) · rides by hour of day

```sql
select hour(started_at) h, count(*) n from ride where started_at >= '2026-10-01' group by h order by h
```

| h | n |
|---|---|
| 0 | 3398 |
| 1 | 1464 |
| 2 | 3824 |
| 3 | 249 |
| 4 | 3154 |
| 5 | 1395 |
| 6 | 1506 |
| 7 | 2516 |
| 8 | 2931 |
| 9 | 686 |
| 10 | 2727 |
| 11 | 1840 |
| 12 | 3715 |
| 13 | 1934 |
| 14 | 3661 |
| 15 | 3586 |
| 16 | 1071 |
| 17 | 1395 |
| 18 | 2395 |
| 19 | 385 |
| 20 | 480 |
| 21 | 3315 |
| 22 | 3937 |
| 23 | 2439 |

_24 rows · 1.6 s_

## 10:03:33 · bikes-test / bikeshare_test (read-only) · facts of test ticket 926, to copy locally

```sql
select to_base64(facts) b from ticket where id = 926
```

| b |
|---|
| W3siYXQiOiIyMDI2LTEwLTE3VDE0OjU0OjQxWiIsImJ5IjoiY3VzdG9tZXIgY2FyZSIsImZhY3Qi⏎OiJUaWNrZXQgOTI2OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgbGlnaHQgZmF1bHQgb24gYmlr⏎ZSAxMTUxIGF0IE7DoW3Em3N0w60gTcOtcnUuIiwidHlwZSI6ImluZm9ybWF0aW9uIiwicXVvdGUi… |

_1 rows · 2.2 s_

## 10:08:07 · bikes-prod / bikeshare_prod (read-only) · rides by hour of day

```sql
select hour(started_at) h, count(*) n from ride where started_at >= '2026-10-01' group by h order by h
```

| h | n |
|---|---|
| 0 | 3089 |
| 1 | 3244 |
| 2 | 1003 |
| 3 | 1303 |
| 4 | 1308 |
| 5 | 3965 |
| 6 | 1943 |
| 7 | 702 |
| 8 | 1480 |
| 9 | 3728 |
| 10 | 1976 |
| 11 | 1943 |
| 12 | 1896 |
| 13 | 2397 |
| 14 | 1870 |
| 15 | 2401 |
| 16 | 3066 |
| 17 | 1251 |
| 18 | 2335 |
| 19 | 3807 |
| 20 | 1537 |
| 21 | 3637 |
| 22 | 909 |
| 23 | 211 |

_24 rows · 1.8 s_

## 10:12:00 · bikes-localhost / bikeshare (read-write) · local tickets with facts

```sql
select count(*) from ticket_note where facts is not null
```

| count(*) |
|---|
| 30 |

_1 rows · 2.0 s_

## 10:18:38 · bikes-prod / bikeshare_prod (read-only) · free docks per station

```sql
select s.name, count(*) free_docks
from dock d join station s on s.id = d.station_id
where d.bike_id is null group by s.name order by free_docks desc
```

| name | free_docks |
|---|---|
| Náměstí Míru | 6 |
| Hlavní nádraží | 4 |
| Výstaviště | 15 |
| Mendlovo náměstí | 14 |
| Lužánky | 18 |
| Královo Pole | 14 |

_6 rows · 0.5 s_

## 10:22:22 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Petr Novotný | student |
| Zuzana Pokorná | company |
| Petr Novotný | student |
| Martin Procházka | senior |
| Ondřej Marek | senior |

_5 rows · 2.5 s_

## 10:25:33 · dispatch-test (read-only) · select table_name, column_name from information_schema.columns where table_schema = 'public' and column_name i…

```sql
select table_name, column_name from information_schema.columns where table_schema = 'public' and column_name ilike '%recipe%'
```

| table_name | column_name |
|---|---|
| runs | recipe |
| workflow_actions | recipe_json |
| runs | input_template |
| workflows | recipe_json |
| runs | code_body |
| run_steps | recipe_json |
| workflows | recipe |
| runs | recipe |
| workflow_actions | recipe |
| runs | recipe_json |
| workflows | recipe |
| run_steps | recipe_version |
| workflow_actions | code_body |
| workflows | input_template |
| workflows | code_body |
| workflows | recipe_json |
| runs | recipe_json |
| recipes | input_template |
| workflow_actions | code_body |
| workflow_actions | recipe_version |
| run_steps | recipe_json |
| runs | recipe |
| recipes | code_body |
| runs | input_template |
| runs | code_body |
| runs | recipe_json |
| runs | recipe |
| recipes | code_body |
| workflows | recipe_json |
| workflows | code_body |
| recipes | code_body |
| recipes | recipe_json |
| runs | recipe_version |
| workflow_actions | recipe_json |
| recipes | recipe |
| runs | recipe_version |
| recipes | code_body |
| workflow_actions | input_template |
| recipes | recipe_json |
| recipes | code_body |
| workflow_actions | code_body |
| recipes | recipe_json |

_42 rows · 2.3 s_

## 10:28:47 · bikes-localhost / bikeshare (WRITE) · copy test ticket facts into local ticket 451

```sql
update ticket set facts = from_base64('W3siYXQiOiIyMDI2LTEwLTE3VDE0OjU0OjQxWiIsImJ5IjoiY3VzdG9tZXIgY2FyZSIsImZhY3QiOiJUaWNrZXQgOTI2OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxMTUxIGF0IE7DoW3Em3N0w60gTcOtcnUuIiwidHlwZSI6ImluZm9ybWF0aW9uIiwicXVvdGUiOiJCYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS4iLCJzb3VyY2UiOiJhY3Rpdml0eV9mYmE1NDFlZGQ3NGQwY2ZjMTVhMCJ9LHsiYXQiOiIyMDI2LTEwLTA4VDE0OjQ2OjE2WiIsImJ5Ijoic2VydmljZSB0ZWNobmljaWFuIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSByaWRlciByZXBvcnRlZCBhIGxpZ2h0IGZhdWx0IG9uIGJpa2UgMTU1NSBhdCBCeXN0cmMgcMWZw61zdGF2acWhdMSbLiIsInR5cGUiOiJwcm9taXNlIiwicXVvdGUiOiJQcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS4iLCJzb3VyY2UiOiJhY3Rpdml0eV9kM2Q2ZTJkNDA3MDJlMzU5YjljOSJ9LHsiYXQiOiIyMDI2LTEwLTE4VDA3OjE2OjA0WiIsImJ5IjoiY3VzdG9tZXIgY2FyZSIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGZsYXQgdHlyZSBmYXVsdCBvbiBiaWtlIDE4MTQgYXQgTWVuZGxvdm8gbsOhbcSbc3TDrS4iLCJ0eXBlIjoicmVxdWVzdCIsInF1b3RlIjoiS29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LiIsInNvdXJjZSI6ImFjdGl2aXR5XzAyNThmNjY1YTYwYzZkMmE4Y2E3In0seyJhdCI6IjIwMjYtMTAtMTJUMDk6MDA6MTlaIiwiYnkiOiJzZXJ2aWNlIHRlY2huaWNpYW4iLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIGRlcG90IGNvbmZpcm1lZCBhIGtpY2tzdGFuZCBmYXVsdCBvbiBiaWtlIDE4MjMgYXQgU3RhcsO9IEzDrXNrb3ZlYy4iLCJ0eXBlIjoiaW5mb3JtYXRpb24iLCJxdW90ZSI6IlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuIiwic291cmNlIjoiYWN0aXZpdHlfOTkxMWRhN2NhZDUyNzFlNWI4MTEifSx7ImF0IjoiMjAyNi0xMC0xNlQxMzo1NzowMVoiLCJieSI6ImN1c3RvbWVyIGNhcmUiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTYyMSBhdCBLb23DoXJvdi4iLCJ0eXBlIjoicmVxdWVzdCIsInF1b3RlIjoiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuIiwic291cmNlIjoiYWN0aXZpdHlfMzMxNWZhM2I0YmU0MThjYTNjZjIifSx7ImF0IjoiMjAyNi0xMC0wMVQxMDoxMDoyN1oiLCJieSI6InJpZGVyIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgZmxhdCB0eXJlIGZhdWx0IG9uIGJpa2UgMTA1NiBhdCBWw71zdGF2acWhdMSbLiIsInR5cGUiOiJyZXF1ZXN0IiwicXVvdGUiOiJLb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuIiwic291cmNlIjoiYWN0aXZpdHlfZDBkMWIzYzU2ODZiYmE2NDljZTYifSx7ImF0IjoiMjAyNi0xMC0wMlQwNzo1MzozM1oiLCJieSI6InNlcnZpY2UgdGVjaG5pY2lhbiIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGRpc3BsYXkgZmF1bHQgb24gYmlrZSAxODM0IGF0IMOadm96LiIsInR5cGUiOiJpbmZvcm1hdGlvbiIsInF1b3RlIjoiRMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLiIsInNvdXJjZSI6ImFjdGl2aXR5XzYwN2E5ZGFhMGQ5NDIyMDJiMTJhIn0seyJhdCI6IjIwMjYtMTAtMDRUMDg6MDA6MDhaIiwiYnkiOiJjdXN0b21lciBjYXJlIiwiZmFjdCI6IlRpY2tldCA5MjY6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBsb2NrIGZhdWx0IG9uIGJpa2UgMTM4MCBhdCBLcmF2w60gaG9yYS4iLCJ0eXBlIjoicmVxdWVzdCIsInF1b3RlIjoiUMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuIiwic291cmNlIjoiYWN0aXZpdHlfZGE2MDAwNTgyYmI2MTQ2YjJhZDcifSx7ImF0IjoiMjAyNi0xMC0yNVQwODo0MTowNloiLCJieSI6ImN1c3RvbWVyIGNhcmUiLCJmYWN0IjoiVGlja2V0IDkyNjogY3VzdG9tZXIgY2FyZSBwcm9taXNlZCBhIHNhZGRsZSBmYXVsdCBvbiBiaWtlIDEzMDQgYXQgU3RhcsO9IEzDrXNrb3ZlYy4iLCJ0eXBlIjoicHJvbWlzZSIsInF1b3RlIjoiU2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS4iLCJzb3VyY2UiOiJhY3Rpdml0eV8xMTg0NTM5MjQ5NjM3NzFhYmQwZCJ9LHsiYXQiOiIyMDI2LTEwLTI1VDE4OjM5OjIzWiIsImJ5IjoicmlkZXIiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTk3NCBhdCBNZW5kbG92byBuw6FtxJtzdMOtLiIsInR5cGUiOiJwcm9taXNlIiwicXVvdGUiOiJExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuIiwic291cmNlIjoiYWN0aXZpdHlfZmQ5MGFmMDJhMWU0YThhODMzYTkifSx7ImF0IjoiMjAyNi0xMC0xOFQxODo0Mzo1NFoiLCJieSI6ImN1c3RvbWVyIGNhcmUiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIHJpZGVyIHJlcG9ydGVkIGEga2lja3N0YW5kIGZhdWx0IG9uIGJpa2UgMTE3OSBhdCBOb3bDqSBzYWR5LiIsInR5cGUiOiJpbmZvcm1hdGlvbiIsInF1b3RlIjoiUHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuIiwic291cmNlIjoiYWN0aXZpdHlfNjQwNDhlNTU0NjQwNjRiY2UzNDQifSx7ImF0IjoiMjAyNi0xMC0wN1QyMDoxMToxNVoiLCJieSI6ImN1c3RvbWVyIGNhcmUiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIGRlcG90IGNvbmZpcm1lZCBhIGxvY2sgZmF1bHQgb24gYmlrZSAxODY1IGF0IEJ5c3RyYyBwxZnDrXN0YXZpxaF0xJsuIiwidHlwZSI6InJlcXVlc3QiLCJxdW90ZSI6Ik5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLiIsInNvdXJjZSI6ImFjdGl2aXR5X2YzYTJjOTBkMTJkZTFmNWE5NTU3In0seyJhdCI6IjIwMjYtMTAtMDRUMjE6NDg6MDJaIiwiYnkiOiJzZXJ2aWNlIHRlY2huaWNpYW4iLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIGRlcG90IGNvbmZpcm1lZCBhIGNoYWluIGZhdWx0IG9uIGJpa2UgMTc0NSBhdCBLcsOhbG92byBQb2xlLiIsInR5cGUiOiJwcm9taXNlIiwicXVvdGUiOiJQcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS4iLCJzb3VyY2UiOiJhY3Rpdml0eV9kYWVmN2UyMDU1NjFjN2RkY2UwNSJ9LHsiYXQiOiIyMDI2LTEwLTI3VDE5OjE3OjUzWiIsImJ5Ijoib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3QiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIGRlcG90IGNvbmZpcm1lZCBhIGJhdHRlcnkgZmF1bHQgb24gYmlrZSAxMDEwIGF0IEJ5c3RyYyBwxZnDrXN0YXZpxaF0xJsuIiwidHlwZSI6InByb21pc2UiLCJxdW90ZSI6IkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS4iLCJzb3VyY2UiOiJhY3Rpdml0eV9hY2QxNjlkNDFlZmRhMTU1ZWVmYSJ9LHsiYXQiOiIyMDI2LTEwLTEwVDEwOjIwOjA2WiIsImJ5Ijoic2VydmljZSB0ZWNobmljaWFuIiwiZmFjdCI6IlRpY2tldCA5MjY6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBraWNrc3RhbmQgZmF1bHQgb24gYmlrZSAxMzk1IGF0IE7DoW3Em3N0w60gTcOtcnUuIiwidHlwZSI6ImNvbXBsYWludCIsInF1b3RlIjoiUHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuIiwic291cmNlIjoiYWN0aXZpdHlfNWZkOTY4MjJmNDY0ZWZiOTY4ZDUifSx7ImF0IjoiMjAyNi0xMC0wNlQxMzowNDoyN1oiLCJieSI6Im9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90IiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSByaWRlciByZXBvcnRlZCBhIGNoYWluIGZhdWx0IG9uIGJpa2UgMTM1NSBhdCBMdcW+w6Fua3kuIiwidHlwZSI6ImluZm9ybWF0aW9uIiwicXVvdGUiOiJLb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuIiwic291cmNlIjoiYWN0aXZpdHlfM2QwM2U2ZDdjYzRlZGM4YThlY2QifSx7ImF0IjoiMjAyNi0xMC0yNFQxMDoxMToxNloiLCJieSI6InJpZGVyIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEga2lja3N0YW5kIGZhdWx0IG9uIGJpa2UgMTE3MyBhdCBTdGFyw70gTMOtc2tvdmVjLiIsInR5cGUiOiJpbmZvcm1hdGlvbiIsInF1b3RlIjoiRMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLiIsInNvdXJjZSI6ImFjdGl2aXR5XzNhZGNiMDIxZWM2ZWQ5NWUwZGNjIn0seyJhdCI6IjIwMjYtMTAtMjNUMTQ6Mjg6MzVaIiwiYnkiOiJzZXJ2aWNlIHRlY2huaWNpYW4iLCJmYWN0IjoiVGlja2V0IDkyNjogY3VzdG9tZXIgY2FyZSBwcm9taXNlZCBhIHNhZGRsZSBmYXVsdCBvbiBiaWtlIDE5NTMgYXQgVmHFiGtvdmthLiIsInR5cGUiOiJjb21wbGFpbnQiLCJxdW90ZSI6IlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuIiwic291cmNlIjoiYWN0aXZpdHlfZDNhNWY4ZjE1ZjVhMDNkNmY5MzcifSx7ImF0IjoiMjAyNi0xMC0wOFQxNDo0NjowOFoiLCJieSI6Im9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90IiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSByaWRlciByZXBvcnRlZCBhIGNoYWluIGZhdWx0IG9uIGJpa2UgMTgyMyBhdCBCeXN0cmMgcMWZw61zdGF2acWhdMSbLiIsInR5cGUiOiJwcm9taXNlIiwicXVvdGUiOiJTZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLiIsInNvdXJjZSI6ImFjdGl2aXR5XzhlMTJhY2M4ODk5YzU5YjY1NGI3In0seyJhdCI6IjIwMjYtMTAtMDhUMDk6Mjg6MDRaIiwiYnkiOiJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdCIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgcmlkZXIgcmVwb3J0ZWQgYSBjaGFpbiBmYXVsdCBvbiBiaWtlIDE3MTYgYXQgTW9yYXZza8OpIG7DoW3Em3N0w60uIiwidHlwZSI6InJlcXVlc3QiLCJxdW90ZSI6IlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuIiwic291cmNlIjoiYWN0aXZpdHlfMGM4NDZjNThlNjhiOWI4MjJmMmIifSx7ImF0IjoiMjAyNi0xMC0xNFQxOTo0MDowM1oiLCJieSI6Im9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90IiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSByaWRlciByZXBvcnRlZCBhIGxpZ2h0IGZhdWx0IG9uIGJpa2UgMTUzMSBhdCBNb3JhdnNrw6kgbsOhbcSbc3TDrS4iLCJ0eXBlIjoicmVxdWVzdCIsInF1b3RlIjoiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuIiwic291cmNlIjoiYWN0aXZpdHlfODBhYzNkM2RlNDRhZjEwYTAwYTAifSx7ImF0IjoiMjAyNi0xMC0wMVQxNToxODowN1oiLCJieSI6Im9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90IiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgc2FkZGxlIGZhdWx0IG9uIGJpa2UgMTQ2NiBhdCDDmnZvei4iLCJ0eXBlIjoiY29tcGxhaW50IiwicXVvdGUiOiJExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuIiwic291cmNlIjoiYWN0aXZpdHlfNGI3MWYyMjE5NzNkNThlZWYyYjQifSx7ImF0IjoiMjAyNi0xMC0xM1QwNjo0MjoyOVoiLCJieSI6ImN1c3RvbWVyIGNhcmUiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBmbGF0IHR5cmUgZmF1bHQgb24gYmlrZSAxNTkzIGF0IMW9YWJvdsWZZXNreS4iLCJ0eXBlIjoiY29tcGxhaW50IiwicXVvdGUiOiJExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuIiwic291cmNlIjoiYWN0aXZpdHlfMTYzZWY1ZjdkMjVmMjUxYzc5YjIifSx7ImF0IjoiMjAyNi0xMC0yMlQyMTowOTowNFoiLCJieSI6InJpZGVyIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSBkZXBvdCBjb25maXJtZWQgYSBsaWdodCBmYXVsdCBvbiBiaWtlIDE1NzAgYXQgVmHFiGtvdmthLiIsInR5cGUiOiJyZXF1ZXN0IiwicXVvdGUiOiJTZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLiIsInNvdXJjZSI6ImFjdGl2aXR5XzAzMTg2OTA3MDQ2YzVkOGI1MWMzIn0seyJhdCI6IjIwMjYtMTAtMTJUMTI6MDE6MDRaIiwiYnkiOiJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdCIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGJyYWtlIGZhdWx0IG9uIGJpa2UgMTA3OCBhdCBIbGF2bsOtIG7DoWRyYcW+w60uIiwidHlwZSI6ImNvbXBsYWludCIsInF1b3RlIjoiUHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuIiwic291cmNlIjoiYWN0aXZpdHlfYjZiZDJjZDJkMGJjZTRjYzZmZWEifSx7ImF0IjoiMjAyNi0xMC0xNFQxNToyNDozOFoiLCJieSI6InNlcnZpY2UgdGVjaG5pY2lhbiIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGZsYXQgdHlyZSBmYXVsdCBvbiBiaWtlIDExMDcgYXQgw5p2b3ouIiwidHlwZSI6InJlcXVlc3QiLCJxdW90ZSI6IlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS4iLCJzb3VyY2UiOiJhY3Rpdml0eV8zOGRiODIwNmMxZTEzYTYwNmYwYiJ9LHsiYXQiOiIyMDI2LTEwLTAzVDExOjU1OjQ1WiIsImJ5Ijoic2VydmljZSB0ZWNobmljaWFuIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgYmF0dGVyeSBmYXVsdCBvbiBiaWtlIDEwMzIgYXQgS29tw6Fyb3YuIiwidHlwZSI6ImNvbXBsYWludCIsInF1b3RlIjoiUHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuIiwic291cmNlIjoiYWN0aXZpdHlfZjlmZjFjNWZmNTQwYzllMTYyN2UifSx7ImF0IjoiMjAyNi0xMC0yNlQxOTo1MjozM1oiLCJieSI6InNlcnZpY2UgdGVjaG5pY2lhbiIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgcmlkZXIgcmVwb3J0ZWQgYSBraWNrc3RhbmQgZmF1bHQgb24gYmlrZSAxOTQxIGF0IMOadm96LiIsInR5cGUiOiJwcm9taXNlIiwicXVvdGUiOiJTZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLiIsInNvdXJjZSI6ImFjdGl2aXR5X2RhZmMxYzgxNWVhYjYzNGVhMmMzIn0seyJhdCI6IjIwMjYtMTAtMDJUMTE6MTM6MTVaIiwiYnkiOiJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdCIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgcmlkZXIgcmVwb3J0ZWQgYSBicmFrZSBmYXVsdCBvbiBiaWtlIDEyNzQgYXQgU3RhcsO9IEzDrXNrb3ZlYy4iLCJ0eXBlIjoiY29tcGxhaW50IiwicXVvdGUiOiJLb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuIiwic291cmNlIjoiYWN0aXZpdHlfMjExODQ2MzRmNzUyMTMyMTcyZjEifSx7ImF0IjoiMjAyNi0xMC0xOFQwNzoxNzoxNFoiLCJieSI6Im9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90IiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSBkZXBvdCBjb25maXJtZWQgYSBicmFrZSBmYXVsdCBvbiBiaWtlIDE2NTggYXQgQnlzdHJjIHDFmcOtc3RhdmnFoXTEmy4iLCJ0eXBlIjoiaW5mb3JtYXRpb24iLCJxdW90ZSI6IkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLiIsInNvdXJjZSI6ImFjdGl2aXR5X2U4MjYwYTFkZjRiMWNkMTgxN2QzIn0seyJhdCI6IjIwMjYtMTAtMDFUMTg6NTQ6NTRaIiwiYnkiOiJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdCIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgcmlkZXIgcmVwb3J0ZWQgYSBmbGF0IHR5cmUgZmF1bHQgb24gYmlrZSAxMjAxIGF0IFbDvXN0YXZpxaF0xJsuIiwidHlwZSI6ImluZm9ybWF0aW9uIiwicXVvdGUiOiJQcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS4iLCJzb3VyY2UiOiJhY3Rpdml0eV83M2I1ZjJmOWU0NWQzZGM0NWI4MSJ9LHsiYXQiOiIyMDI2LTEwLTI4VDE5OjAyOjA3WiIsImJ5Ijoic2VydmljZSB0ZWNobmljaWFuIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSByaWRlciByZXBvcnRlZCBhIGJyYWtlIGZhdWx0IG9uIGJpa2UgMTQzNyBhdCBOw6FtxJtzdMOtIE3DrXJ1LiIsInR5cGUiOiJyZXF1ZXN0IiwicXVvdGUiOiJOYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS4iLCJzb3VyY2UiOiJhY3Rpdml0eV9jNzk0OTQ2Nzg0MzhmOTQ5OTIwYiJ9LHsiYXQiOiIyMDI2LTEwLTA2VDEwOjMyOjAzWiIsImJ5IjoiY3VzdG9tZXIgY2FyZSIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgcmlkZXIgcmVwb3J0ZWQgYSBsb2NrIGZhdWx0IG9uIGJpa2UgMTYwNiBhdCBOb3bDqSBzYWR5LiIsInR5cGUiOiJwcm9taXNlIiwicXVvdGUiOiJQxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC4iLCJzb3VyY2UiOiJhY3Rpdml0eV9kMDIxYTE1MmYxYmE5YmJhNTcxOCJ9LHsiYXQiOiIyMDI2LTEwLTAyVDEyOjExOjEwWiIsImJ5Ijoic2VydmljZSB0ZWNobmljaWFuIiwiZmFjdCI6IlRpY2tldCA5MjY6IHRoZSByaWRlciByZXBvcnRlZCBhIGRpc3BsYXkgZmF1bHQgb24gYmlrZSAxOTE0IGF0IEtvbcOhcm92LiIsInR5cGUiOiJjb21wbGFpbnQiLCJxdW90ZSI6IkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS4iLCJzb3VyY2UiOiJhY3Rpdml0eV83Y2Y5ZDM1NjFjMmFhODVjMmM3MyJ9LHsiYXQiOiIyMDI2LTEwLTA5VDEyOjQ1OjI1WiIsImJ5Ijoib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3QiLCJmYWN0IjoiVGlja2V0IDkyNjogY3VzdG9tZXIgY2FyZSBwcm9taXNlZCBhIHNhZGRsZSBmYXVsdCBvbiBiaWtlIDEwNjQgYXQgTm92w6kgc2FkeS4iLCJ0eXBlIjoicHJvbWlzZSIsInF1b3RlIjoiRMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLiIsInNvdXJjZSI6ImFjdGl2aXR5XzNlMmFkMjc5YTAzNWIxY2M4YzdiIn0seyJhdCI6IjIwMjYtMTAtMTJUMDY6MTc6NTNaIiwiYnkiOiJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdCIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIHNhZGRsZSBmYXVsdCBvbiBiaWtlIDE1NTEgYXQgSGxhdm7DrSBuw6FkcmHFvsOtLiIsInR5cGUiOiJyZXF1ZXN0IiwicXVvdGUiOiJQxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC4iLCJzb3VyY2UiOiJhY3Rpdml0eV8yM2MwNzkzYjEzODgwZTZiNGM0NSJ9LHsiYXQiOiIyMDI2LTEwLTE1VDE5OjIwOjU2WiIsImJ5IjoicmlkZXIiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIHJpZGVyIHJlcG9ydGVkIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDEwNzAgYXQgS3LDoWxvdm8gUG9sZS4iLCJ0eXBlIjoicmVxdWVzdCIsInF1b3RlIjoiRMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLiIsInNvdXJjZSI6ImFjdGl2aXR5X2JhMWNkZjI2Y2ZhZGEzMTc2MDI5In0seyJhdCI6IjIwMjYtMTAtMTBUMDY6Mzk6MThaIiwiYnkiOiJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdCIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGZsYXQgdHlyZSBmYXVsdCBvbiBiaWtlIDExNTcgYXQgS29tw6Fyb3YuIiwidHlwZSI6InByb21pc2UiLCJxdW90ZSI6IkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS4iLCJzb3VyY2UiOiJhY3Rpdml0eV80ZmRmZDJiMDNkZWEyNzM5M2Y5ZCJ9LHsiYXQiOiIyMDI2LTEwLTI4VDE2OjUwOjA1WiIsImJ5IjoiY3VzdG9tZXIgY2FyZSIsImZhY3QiOiJUaWNrZXQgOTI2OiB0aGUgZGVwb3QgY29uZmlybWVkIGEgY2hhaW4gZmF1bHQgb24gYmlrZSAxNjc5IGF0IE5vdsOpIHNhZHkuIiwidHlwZSI6ImluZm9ybWF0aW9uIiwicXVvdGUiOiJLb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuIiwic291cmNlIjoiYWN0aXZpdHlfNjc4NmI3YzIwY2NkNGE0MTE0NzUifSx7ImF0IjoiMjAyNi0xMC0wNFQxMToyNzo1OFoiLCJieSI6ImN1c3RvbWVyIGNhcmUiLCJmYWN0IjoiVGlja2V0IDkyNjogdGhlIGRlcG90IGNvbmZpcm1lZCBhIHNhZGRsZSBmYXVsdCBvbiBiaWtlIDE1ODkgYXQgVsO9c3RhdmnFoXTEmy4iLCJ0eXBlIjoicHJvbWlzZSIsInF1b3RlIjoiWsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLiIsInNvdXJjZSI6ImFjdGl2aXR5X2FjM2U0MzBiMGY1MzE2MjA5YmRkIn1d') where id = 451;
```

_0 rows · 1.3 s_

## 10:33:10 · bikes-prod / bikeshare_prod (read-only) · rides and revenue per day

```sql
select date(started_at) day, count(*) rides, sum(price) revenue_czk from ride group by day order by day desc limit 24
```

| day | rides | revenue_czk |
|---|---|---|
| 2026-10-30 | 1175 | 32760.65 |
| 2026-10-29 | 1354 | 21398.30 |
| 2026-10-28 | 3942 | 34611.30 |
| 2026-10-27 | 2740 | 11948.47 |
| 2026-10-26 | 1081 | 7865.54 |
| 2026-10-25 | 1454 | 8074.77 |
| 2026-10-24 | 3569 | 13288.30 |
| 2026-10-23 | 1747 | 34034.78 |
| 2026-10-22 | 3398 | 34104.54 |
| 2026-10-21 | 3160 | 23821.05 |
| 2026-10-20 | 3828 | 20275.38 |
| 2026-10-19 | 1693 | 16154.31 |
| 2026-10-18 | 2677 | 6693.42 |
| 2026-10-17 | 1686 | 26374.78 |
| 2026-10-16 | 3173 | 21872.36 |
| 2026-10-15 | 2171 | 24445.36 |
| 2026-10-14 | 1541 | 21461.34 |
| 2026-10-13 | 4118 | 27858.96 |
| 2026-10-12 | 3909 | 17082.06 |

_19 rows · 1.2 s_

## 10:36:20 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1004 | flat tyre | 2026-10-27 |
| 1217 | battery | 2026-10-24 |
| 1798 | battery | 2026-10-17 |
| 1900 | bell | 2026-10-07 |
| 1792 | light | 2026-10-16 |
| 1149 | bell | 2026-10-29 |
| 1215 | flat tyre | 2026-10-06 |
| 1921 | bell | 2026-10-28 |
| 1398 | bell | 2026-10-17 |
| 1707 | flat tyre | 2026-10-13 |
| 1756 | saddle | 2026-10-15 |
| 1362 | bell | 2026-10-29 |
| 1871 | flat tyre | 2026-10-12 |
| 1318 | brake | 2026-10-23 |
| 1639 | saddle | 2026-10-14 |
| 1568 | flat tyre | 2026-10-30 |
| 1984 | kickstand | 2026-10-25 |
| 1965 | display | 2026-10-10 |

_18 rows · 2.5 s_

## 10:41:29 · bikes-prod / bikeshare_prod (read-only) · free docks per station

```sql
select s.name, count(*) free_docks
from dock d join station s on s.id = d.station_id
where d.bike_id is null group by s.name order by free_docks desc
```

| name | free_docks |
|---|---|
| Náměstí Míru | 5 |
| Hlavní nádraží | 2 |
| Výstaviště | 22 |
| Mendlovo náměstí | 19 |
| Lužánky | 9 |
| Královo Pole | 5 |
| Žabovřesky | 12 |
| Komárov | 4 |
| Starý Lískovec | 9 |

_9 rows · 1.4 s_

## 10:42:22 · bikes-prod / bikeshare_prod (read-only) · rides by hour of day

```sql
select hour(started_at) h, count(*) n from ride where started_at >= '2026-10-01' group by h order by h
```

| h | n |
|---|---|
| 0 | 2973 |
| 1 | 2072 |
| 2 | 3678 |
| 3 | 2661 |
| 4 | 1647 |
| 5 | 391 |
| 6 | 894 |
| 7 | 1108 |
| 8 | 1379 |
| 9 | 3154 |
| 10 | 860 |
| 11 | 2148 |
| 12 | 1373 |
| 13 | 1381 |
| 14 | 3959 |
| 15 | 582 |
| 16 | 3448 |
| 17 | 3687 |
| 18 | 1426 |
| 19 | 1034 |
| 20 | 2922 |
| 21 | 2934 |
| 22 | 1179 |
| 23 | 1116 |

_24 rows · 2.5 s_

## 10:47:56 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 209594 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/3602?tab=history"},{"type":"string","title":"Searched","value":"ride 114394: 1 found"},{"type":"multiline","title":"Ticket… |

_1 rows · 2.6 s_

## 10:49:37 · bikes-localhost / bikeshare (WRITE) · clone test ticket 1879 locally

```sql
set @g = convert(from_base64('eyJSaWRlcklkIjo4MDAsIkNpdHlJZCI6MywiU3ViamVjdCI6IlJFOiBqw616ZGEgMTkwMzcwIiwiRW1haWwiOiJyaWRlckBleGFtcGxlLmNvbSIsIkV4dGVybmFsSWQiOiIxODc5IiwiRXh0ZXJuYWxKc29uRGF0YSI6IntcImlkXCI6MTg3OSxcImNoYW5uZWxcIjpcImVtYWlsXCIsXCJzdGF0aW9uSGlzdG9yeVwiOlt7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAwNjowNVwiLFwiYmlrZVwiOjE0MDMsXCJiYXR0ZXJ5XCI6OTR9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEyIDExOjI1XCIsXCJiaWtlXCI6MTAxOSxcImJhdHRlcnlcIjo1OX0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMTc6MTNcIixcImJpa2VcIjoxOTY3LFwiYmF0dGVyeVwiOjEwMH0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI0IDE4OjExXCIsXCJiaWtlXCI6MTExOSxcImJhdHRlcnlcIjo1N30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xOCAxNjoyMVwiLFwiYmlrZVwiOjE4NzQsXCJiYXR0ZXJ5XCI6NDl9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjQgMTA6MDZcIixcImJpa2VcIjoxNzEyLFwiYmF0dGVyeVwiOjM0fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAwNjoxM1wiLFwiYmlrZVwiOjE4NTEsXCJiYXR0ZXJ5XCI6OTN9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMDcgMTE6MDdcIixcImJpa2VcIjoxNDM0LFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxMzozOFwiLFwiYmlrZVwiOjE2OTgsXCJiYXR0ZXJ5XCI6MjZ9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA5IDE4OjEwXCIsXCJiaWtlXCI6MTIzMSxcImJhdHRlcnlcIjozNH0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTA2IDA4OjEwXCIsXCJiaWtlXCI6MTEzNSxcImJhdHRlcnlcIjoxMX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTIxIDE0OjQ3XCIsXCJiaWtlXCI6MTg1OCxcImJhdHRlcnlcIjo5fSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAyMjo0N1wiLFwiYmlrZVwiOjExNzksXCJiYXR0ZXJ5XCI6NjR9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMTAgMTc6MTlcIixcImJpa2VcIjoxMTYyLFwiYmF0dGVyeVwiOjE3fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTE5IDEzOjEyXCIsXCJiaWtlXCI6MTM1MCxcImJhdHRlcnlcIjozNX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI1IDExOjUyXCIsXCJiaWtlXCI6MTk2NyxcImJhdHRlcnlcIjo2MX0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTk6MzhcIixcImJpa2VcIjoxODgyLFwiYmF0dGVyeVwiOjY4fSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTI0IDE1OjQwXCIsXCJiaWtlXCI6MTE3OSxcImJhdHRlcnlcIjo4fSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAxNDo1NFwiLFwiYmlrZVwiOjEzODIsXCJiYXR0ZXJ5XCI6NX0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTAyIDA2OjI2XCIsXCJiaWtlXCI6MTQwMCxcImJhdHRlcnlcIjozNH0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAxODo1NFwiLFwiYmlrZVwiOjE1MzksXCJiYXR0ZXJ5XCI6Nzd9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTAxIDE0OjI5XCIsXCJiaWtlXCI6MTQ3OSxcImJhdHRlcnlcIjo1NH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTE6MjBcIixcImJpa2VcIjoxNjI3LFwiYmF0dGVyeVwiOjl9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTI1IDE1OjUwXCIsXCJiaWtlXCI6MTMzNixcImJhdHRlcnlcIjo3N30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxMjo0MlwiLFwiYmlrZVwiOjEyMDYsXCJiYXR0ZXJ5XCI6NTJ9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI3IDE0OjQwXCIsXCJiaWtlXCI6MTMwNCxcImJhdHRlcnlcIjozOX0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTIyIDEwOjMzXCIsXCJiaWtlXCI6MTYwNCxcImJhdHRlcnlcIjoxMX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA0IDA2OjU4XCIsXCJiaWtlXCI6MTg1NSxcImJhdHRlcnlcIjoyNX0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMTcgMjA6MTVcIixcImJpa2VcIjoxOTkxLFwiYmF0dGVyeVwiOjEyfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0yMiAwOToxMFwiLFwiYmlrZVwiOjE0MDksXCJiYXR0ZXJ5XCI6Nn0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTIzIDE3OjE5XCIsXCJiaWtlXCI6MTg5MCxcImJhdHRlcnlcIjo4M30se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxOTo0NlwiLFwiYmlrZVwiOjEzNDgsXCJiYXR0ZXJ5XCI6MjZ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTIwIDE4OjI3XCIsXCJiaWtlXCI6MTE2OCxcImJhdHRlcnlcIjo5Nn0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxNTo0OVwiLFwiYmlrZVwiOjEwMjMsXCJiYXR0ZXJ5XCI6MzR9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMjA6MzlcIixcImJpa2VcIjoxODQ3LFwiYmF0dGVyeVwiOjMyfSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTA2IDIwOjE0XCIsXCJiaWtlXCI6MTgzMyxcImJhdHRlcnlcIjo2M30se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI4IDEyOjQ5XCIsXCJiaWtlXCI6MTYzNCxcImJhdHRlcnlcIjoxOX0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTA4IDEwOjQ1XCIsXCJiaWtlXCI6MTExNixcImJhdHRlcnlcIjo1MX0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMDMgMTI6MjBcIixcImJpa2VcIjoxMjc5LFwiYmF0dGVyeVwiOjY3fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDcgMTk6MTlcIixcImJpa2VcIjoxMTk4LFwiYmF0dGVyeVwiOjYxfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAxMTozNFwiLFwiYmlrZVwiOjE2MjMsXCJiYXR0ZXJ5XCI6MTAwfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAyMjoyOVwiLFwiYmlrZVwiOjEwODksXCJiYXR0ZXJ5XCI6NjF9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTI4IDExOjQ0XCIsXCJiaWtlXCI6MTc4NixcImJhdHRlcnlcIjo4M30se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA1IDA3OjM4XCIsXCJiaWtlXCI6MTM0OSxcImJhdHRlcnlcIjozMX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAwNjo0MVwiLFwiYmlrZVwiOjEyOTYsXCJiYXR0ZXJ5XCI6NTd9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTE2IDIxOjIyXCIsXCJiaWtlXCI6MTUwOSxcImJhdHRlcnlcIjo3OX0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTEzIDE2OjE5XCIsXCJiaWtlXCI6MTcwMyxcImJhdHRlcnlcIjo3MX0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAxMDo1MVwiLFwiYmlrZVwiOjE0OTAsXCJiYXR0ZXJ5XCI6NDd9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTA2IDA5OjU4XCIsXCJiaWtlXCI6MTMwMSxcImJhdHRlcnlcIjoyNn0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTAyIDE5OjE1XCIsXCJiaWtlXCI6MTM0NixcImJhdHRlcnlcIjo0NX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTIwIDEzOjQ5XCIsXCJiaWtlXCI6MTM5MyxcImJhdHRlcnlcIjo1OH0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xNSAyMDoxNVwiLFwiYmlrZVwiOjE5MDAsXCJiYXR0ZXJ5XCI6NzR9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTE6MDRcIixcImJpa2VcIjoxOTMwLFwiYmF0dGVyeVwiOjYyfSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAxMTozOFwiLFwiYmlrZVwiOjE2MzQsXCJiYXR0ZXJ5XCI6NjF9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAwNzoyMVwiLFwiYmlrZVwiOjE2MzMsXCJiYXR0ZXJ5XCI6NTZ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDUgMDY6NTBcIixcImJpa2VcIjoxNDgwLFwiYmF0dGVyeVwiOjEyfSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxMDowNlwiLFwiYmlrZVwiOjE1NzUsXCJiYXR0ZXJ5XCI6N30se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTI6MzlcIixcImJpa2VcIjoxMzE5LFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTc6MTJcIixcImJpa2VcIjoxMTU5LFwiYmF0dGVyeVwiOjk1fSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAxNDo0MFwiLFwiYmlrZVwiOjExODIsXCJiYXR0ZXJ5XCI6ODR9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMDc6MjBcIixcImJpa2VcIjoxMTcxLFwiYmF0dGVyeVwiOjgyfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTA6MTdcIixcImJpa2VcIjoxNTQ1LFwiYmF0dGVyeVwiOjkyfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMTc6MjJcIixcImJpa2VcIjoxOTExLFwiYmF0dGVyeVwiOjYwfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTM6MTJcIixcImJpa2VcIjoxODcwLFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxNjoxNFwiLFwiYmlrZVwiOjE1NjUsXCJiYXR0ZXJ5XCI6NzN9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMTg6NDZcIixcImJpa2VcIjoxMTUyLFwiYmF0dGVyeVwiOjMwfSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTE1IDA4OjA1XCIsXCJiaWtlXCI6MTIzOCxcImJhdHRlcnlcIjo5fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTA3IDE4OjAwXCIsXCJiaWtlXCI6MTg3NixcImJhdHRlcnlcIjoyNn0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTYgMTY6MzFcIixcImJpa2VcIjoxNjMzLFwiYmF0dGVyeVwiOjk3fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTEzIDExOjQ5XCIsXCJiaWtlXCI6MTU3MSxcImJhdHRlcnlcIjo0M30se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMjoxM1wiLFwiYmlrZVwiOjE4NTgsXCJiYXR0ZXJ5XCI6MzR9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI3IDE0OjE2XCIsXCJiaWtlXCI6MTM4MyxcImJhdHRlcnlcIjo0Mn0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAwODozNVwiLFwiYmlrZVwiOjExNDQsXCJiYXR0ZXJ5XCI6Mjh9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTExIDA2OjEwXCIsXCJiaWtlXCI6MTkyMixcImJhdHRlcnlcIjoyOX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI4IDE4OjIyXCIsXCJiaWtlXCI6MTg1OCxcImJhdHRlcnlcIjo3Nn0se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTAgMjE6NTJcIixcImJpa2VcIjoxNTc4LFwiYmF0dGVyeVwiOjIyfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOCAwODozN1wiLFwiYmlrZVwiOjEzNDgsXCJiYXR0ZXJ5XCI6MTl9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTA3IDE5OjI0XCIsXCJiaWtlXCI6MTQ4MSxcImJhdHRlcnlcIjoxMn0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xOCAwOToyNVwiLFwiYmlrZVwiOjEzNTMsXCJiYXR0ZXJ5XCI6NTl9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDUgMTU6MzdcIixcImJpa2VcIjoxMTQ5LFwiYmF0dGVyeVwiOjI4fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAxNDozOVwiLFwiYmlrZVwiOjEwNTIsXCJiYXR0ZXJ5XCI6NjF9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTEyIDIyOjA2XCIsXCJiaWtlXCI6MTEwNyxcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTI3IDA5OjU4XCIsXCJiaWtlXCI6MTE0OSxcImJhdHRlcnlcIjo4M30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0yNiAyMTozNFwiLFwiYmlrZVwiOjEwNTQsXCJiYXR0ZXJ5XCI6MzJ9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAxMzowOVwiLFwiYmlrZVwiOjExNzUsXCJiYXR0ZXJ5XCI6NDZ9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTE2IDExOjAyXCIsXCJiaWtlXCI6MTA3NCxcImJhdHRlcnlcIjo2fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxNDo1NVwiLFwiYmlrZVwiOjE3NjksXCJiYXR0ZXJ5XCI6MjJ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTA3IDEyOjI5XCIsXCJiaWtlXCI6MTc0MCxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTU6MTRcIixcImJpa2VcIjoxMDI3LFwiYmF0dGVyeVwiOjEwfSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAwODo1NFwiLFwiYmlrZVwiOjE2ODcsXCJiYXR0ZXJ5XCI6Mzh9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAyMToxNFwiLFwiYmlrZVwiOjE3NzYsXCJiYXR0ZXJ5XCI6ODl9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMTM6MzhcIixcImJpa2VcIjoxNzU4LFwiYmF0dGVyeVwiOjUwfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxMzo0M1wiLFwiYmlrZVwiOjE1NTIsXCJiYXR0ZXJ5XCI6MzF9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTA6MDVcIixcImJpa2VcIjoxNDAwLFwiYmF0dGVyeVwiOjc2fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMTA6MzZcIixcImJpa2VcIjoxNzI2LFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMzowNlwiLFwiYmlrZVwiOjE0ODUsXCJiYXR0ZXJ5XCI6Mjd9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0yNSAwNjo0NVwiLFwiYmlrZVwiOjE2MDIsXCJiYXR0ZXJ5XCI6OH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDIgMDY6MzRcIixcImJpa2VcIjoxMDc5LFwiYmF0dGVyeVwiOjU1fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAyMTo0MVwiLFwiYmlrZVwiOjEyMjEsXCJiYXR0ZXJ5XCI6NzB9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTAzIDE4OjUxXCIsXCJiaWtlXCI6MTA4NixcImJhdHRlcnlcIjo1MH0se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjE6MDlcIixcImJpa2VcIjoxMDE0LFwiYmF0dGVyeVwiOjczfSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAwODozM1wiLFwiYmlrZVwiOjE2NTAsXCJiYXR0ZXJ5XCI6NDd9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA3IDEwOjUyXCIsXCJiaWtlXCI6MTA0MixcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMjQgMDk6MzJcIixcImJpa2VcIjoxMTMyLFwiYmF0dGVyeVwiOjkwfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMTk6MThcIixcImJpa2VcIjoxNDUwLFwiYmF0dGVyeVwiOjIzfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMTUgMTA6NTdcIixcImJpa2VcIjoxNDUxLFwiYmF0dGVyeVwiOjd9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6MTdcIixcImJpa2VcIjoxODAyLFwiYmF0dGVyeVwiOjg2fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTI0IDExOjI0XCIsXCJiaWtlXCI6MTkzMixcImJhdHRlcnlcIjo1MX0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTI6MjhcIixcImJpa2VcIjoxNDgzLFwiYmF0dGVyeVwiOjQwfSx7XCJzdGF0aW9uXCI6XCJLb23DoXJvdlwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTI6MzRcIixcImJpa2VcIjoxNzgzLFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wMiAxNDoxNFwiLFwiYmlrZVwiOjExNDYsXCJiYXR0ZXJ5XCI6MTF9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMTUgMTg6MDhcIixcImJpa2VcIjoxMjc2LFwiYmF0dGVyeVwiOjk5fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMiAxMzowOFwiLFwiYmlrZVwiOjE1NDIsXCJiYXR0ZXJ5XCI6Mjl9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTE2IDE0OjAzXCIsXCJiaWtlXCI6MTkxNCxcImJhdHRlcnlcIjo2Mn0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTA5IDExOjAzXCIsXCJiaWtlXCI6MTg4NSxcImJhdHRlcnlcIjo2N30se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTI6MjJcIixcImJpa2VcIjoxNTk5LFwiYmF0dGVyeVwiOjcwfSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTEyIDE2OjA4XCIsXCJiaWtlXCI6MTM5NixcImJhdHRlcnlcIjo5NX0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTE4IDE1OjAzXCIsXCJiaWtlXCI6MTU4MixcImJhdHRlcnlcIjo3MX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI4IDE4OjQyXCIsXCJiaWtlXCI6MTIyMixcImJhdHRlcnlcIjoxNn0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMDk6NTdcIixcImJpa2VcIjoxNzgyLFwiYmF0dGVyeVwiOjMzfSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0yNiAxODo1OFwiLFwiYmlrZVwiOjE5MjYsXCJiYXR0ZXJ5XCI6OTR9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxNzo0OFwiLFwiYmlrZVwiOjEyNzEsXCJiYXR0ZXJ5XCI6MzJ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMTMgMTY6NDNcIixcImJpa2VcIjoxNDY2LFwiYmF0dGVyeVwiOjUxfSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTc6NDdcIixcImJpa2VcIjoxMDgzLFwiYmF0dGVyeVwiOjI2fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0yOCAxODo0M1wiLFwiYmlrZVwiOjE2NzYsXCJiYXR0ZXJ5XCI6MTh9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTIyIDIyOjU0XCIsXCJiaWtlXCI6MTU3OSxcImJhdHRlcnlcIjo1fSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMjE6NDdcIixcImJpa2VcIjoxODQwLFwiYmF0dGVyeVwiOjU3fSx7XCJzdGF0aW9uXCI6XCJMdcW+w6Fua3lcIixcImF0XCI6XCIyMDI2LTEwLTA2IDEwOjQ1XCIsXCJiaWtlXCI6MTMwMSxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMjA6MzlcIixcImJpa2VcIjoxMDkyLFwiYmF0dGVyeVwiOjYyfSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wMSAyMDowMFwiLFwiYmlrZVwiOjEzMjMsXCJiYXR0ZXJ5XCI6OX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI4IDE0OjA0XCIsXCJiaWtlXCI6MTEwOCxcImJhdHRlcnlcIjozOH0se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMDY6MjVcIixcImJpa2VcIjoxNjU1LFwiYmF0dGVyeVwiOjI5fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTA0IDE5OjMyXCIsXCJiaWtlXCI6MTU2NyxcImJhdHRlcnlcIjo1MX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTExIDA5OjMxXCIsXCJiaWtlXCI6MTU0NyxcImJhdHRlcnlcIjo2NX0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNSAwODoxM1wiLFwiYmlrZVwiOjEzMDksXCJiYXR0ZXJ5XCI6NDd9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTAzIDA3OjQxXCIsXCJiaWtlXCI6MTY4MixcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTU6MTJcIixcImJpa2VcIjoxMjU2LFwiYmF0dGVyeVwiOjQ0fSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTEwIDA4OjU2XCIsXCJiaWtlXCI6MTE4MixcImJhdHRlcnlcIjo0MX0se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTQ6MDdcIixcImJpa2VcIjoxODk1LFwiYmF0dGVyeVwiOjYyfSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAwODowM1wiLFwiYmlrZVwiOjEzNzcsXCJiYXR0ZXJ5XCI6MTJ9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAxMDozOFwiLFwiYmlrZVwiOjE3NDYsXCJiYXR0ZXJ5XCI6ODF9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxNjoxMlwiLFwiYmlrZVwiOjE4NDgsXCJiYXR0ZXJ5XCI6OTV9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAxODowNVwiLFwiYmlrZVwiOjEwMjUsXCJiYXR0ZXJ5XCI6MTV9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTA2IDEzOjMzXCIsXCJiaWtlXCI6MTE5OSxcImJhdHRlcnlcIjo4N30se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTIzIDE4OjQ4XCIsXCJiaWtlXCI6MTczMSxcImJhdHRlcnlcIjozNX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAxNDo1NFwiLFwiYmlrZVwiOjE5NDUsXCJiYXR0ZXJ5XCI6ODF9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEwIDEwOjA1XCIsXCJiaWtlXCI6MTI2OSxcImJhdHRlcnlcIjo3Nn0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMDcgMTE6NTBcIixcImJpa2VcIjoxOTM2LFwiYmF0dGVyeVwiOjY1fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAxMzowOVwiLFwiYmlrZVwiOjEyNzUsXCJiYXR0ZXJ5XCI6MzF9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAwOTozN1wiLFwiYmlrZVwiOjE2MzAsXCJiYXR0ZXJ5XCI6OTh9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMjE6MTVcIixcImJpa2VcIjoxNDUwLFwiYmF0dGVyeVwiOjd9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEzIDE2OjE4XCIsXCJiaWtlXCI6MTQ0OCxcImJhdHRlcnlcIjo2OX0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAwNjoxNFwiLFwiYmlrZVwiOjE0NjUsXCJiYXR0ZXJ5XCI6Mzl9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTA1IDExOjIyXCIsXCJiaWtlXCI6MTQ0NyxcImJhdHRlcnlcIjo4MX0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6NTVcIixcImJpa2VcIjoxMTk0LFwiYmF0dGVyeVwiOjk0fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTIxIDE4OjEwXCIsXCJiaWtlXCI6MTUwNCxcImJhdHRlcnlcIjo2Nn0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI2IDIyOjM0XCIsXCJiaWtlXCI6MTk5MixcImJhdHRlcnlcIjoxN30se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA1IDIyOjU4XCIsXCJiaWtlXCI6MTc0MyxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxMjozN1wiLFwiYmlrZVwiOjE0MzYsXCJiYXR0ZXJ5XCI6MTV9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTk6MzNcIixcImJpa2VcIjoxNzc5LFwiYmF0dGVyeVwiOjYzfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMDc6MTFcIixcImJpa2VcIjoxODMyLFwiYmF0dGVyeVwiOjc3fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTI0IDA5OjE1XCIsXCJiaWtlXCI6MTk3NSxcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMTQ6NTZcIixcImJpa2VcIjoxODk4LFwiYmF0dGVyeVwiOjg4fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTExIDExOjMxXCIsXCJiaWtlXCI6MTY2NSxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTE0IDE0OjI2XCIsXCJiaWtlXCI6MTA3OCxcImJhdHRlcnlcIjoyMH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTA6MTNcIixcImJpa2VcIjoxNDk0LFwiYmF0dGVyeVwiOjc4fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAwNjowNVwiLFwiYmlrZVwiOjE1MzIsXCJiYXR0ZXJ5XCI6OTF9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI2IDEzOjE5XCIsXCJiaWtlXCI6MTAxOCxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTQgMTU6MDdcIixcImJpa2VcIjoxMjEzLFwiYmF0dGVyeVwiOjZ9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxNzozOFwiLFwiYmlrZVwiOjEwMjMsXCJiYXR0ZXJ5XCI6ODV9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTE4IDEzOjI0XCIsXCJiaWtlXCI6MTY1NixcImJhdHRlcnlcIjo1fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAwNjo0N1wiLFwiYmlrZVwiOjE2NjcsXCJiYXR0ZXJ5XCI6NTN9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI1IDEwOjUwXCIsXCJiaWtlXCI6MTk3OCxcImJhdHRlcnlcIjo3fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxMToyNFwiLFwiYmlrZVwiOjE5MjksXCJiYXR0ZXJ5XCI6Njh9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTA4IDE3OjQ1XCIsXCJiaWtlXCI6MTYxNCxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAxMDozNVwiLFwiYmlrZVwiOjE1MDIsXCJiYXR0ZXJ5XCI6NTZ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTE5IDA5OjI3XCIsXCJiaWtlXCI6MTkwNyxcImJhdHRlcnlcIjo0MH0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxMjoxN1wiLFwiYmlrZVwiOjEwODEsXCJiYXR0ZXJ5XCI6MjB9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTc6MDFcIixcImJpa2VcIjoxOTM0LFwiYmF0dGVyeVwiOjE3fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxNTozM1wiLFwiYmlrZVwiOjEwMjAsXCJiYXR0ZXJ5XCI6MzV9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xNSAwOTo1MVwiLFwiYmlrZVwiOjE0NDksXCJiYXR0ZXJ5XCI6NTR9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTE3IDIyOjAzXCIsXCJiaWtlXCI6MTY3MixcImJhdHRlcnlcIjo3MH0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI2IDA5OjE2XCIsXCJiaWtlXCI6MTk4MSxcImJhdHRlcnlcIjo1Mn0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMjA6MjlcIixcImJpa2VcIjoxMjQ5LFwiYmF0dGVyeVwiOjQ1fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMzozM1wiLFwiYmlrZVwiOjEwMTEsXCJiYXR0ZXJ5XCI6NzB9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEwIDE3OjMxXCIsXCJiaWtlXCI6MTkxMSxcImJhdHRlcnlcIjo4N30se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTAzIDE4OjQ5XCIsXCJiaWtlXCI6MTExNixcImJhdHRlcnlcIjozM30se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTIwIDEzOjAzXCIsXCJiaWtlXCI6MTIzOSxcImJhdHRlcnlcIjoyN30se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAxMjowOFwiLFwiYmlrZVwiOjE5MDQsXCJiYXR0ZXJ5XCI6OTZ9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMTQgMDg6NDNcIixcImJpa2VcIjoxMTA4LFwiYmF0dGVyeVwiOjQwfSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAxOTo0MVwiLFwiYmlrZVwiOjE2NDQsXCJiYXR0ZXJ5XCI6ODR9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMDk6NTZcIixcImJpa2VcIjoxOTAyLFwiYmF0dGVyeVwiOjE5fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTU6MTFcIixcImJpa2VcIjoxNTM0LFwiYmF0dGVyeVwiOjQxfSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxMzoyN1wiLFwiYmlrZVwiOjE1MDYsXCJiYXR0ZXJ5XCI6MTAwfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTI6MzFcIixcImJpa2VcIjoxMzA1LFwiYmF0dGVyeVwiOjEwMH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTM6MTBcIixcImJpa2VcIjoxNjI5LFwiYmF0dGVyeVwiOjkzfSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMTM6MDZcIixcImJpa2VcIjoxMTk3LFwiYmF0dGVyeVwiOjY4fSx7XCJzdGF0aW9uXCI6XCJMdcW+w6Fua3lcIixcImF0XCI6XCIyMDI2LTEwLTAzIDExOjE1XCIsXCJiaWtlXCI6MTA0NSxcImJhdHRlcnlcIjoxMn0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAwNjozN1wiLFwiYmlrZVwiOjE2MzksXCJiYXR0ZXJ5XCI6Njl9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMTE6MjRcIixcImJpa2VcIjoxMDYxLFwiYmF0dGVyeVwiOjY2fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMjA6MzBcIixcImJpa2VcIjoxNzI4LFwiYmF0dGVyeVwiOjc5fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTI4IDE5OjQ5XCIsXCJiaWtlXCI6MTI3OCxcImJhdHRlcnlcIjo5OH0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTExIDE3OjQ4XCIsXCJiaWtlXCI6MTMxMCxcImJhdHRlcnlcIjo2M30se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMTIgMTU6NDhcIixcImJpa2VcIjoxMzE1LFwiYmF0dGVyeVwiOjc3fSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAyMjo0NVwiLFwiYmlrZVwiOjEyODgsXCJiYXR0ZXJ5XCI6NDR9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTI6MjBcIixcImJpa2VcIjoxMjAzLFwiYmF0dGVyeVwiOjI1fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0yOCAxNTozNlwiLFwiYmlrZVwiOjEwODksXCJiYXR0ZXJ5XCI6Nn0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6MjVcIixcImJpa2VcIjoxNDI1LFwiYmF0dGVyeVwiOjIzfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTI6MjdcIixcImJpa2VcIjoxNzc3LFwiYmF0dGVyeVwiOjU0fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxNTowM1wiLFwiYmlrZVwiOjE5MjIsXCJiYXR0ZXJ5XCI6NTR9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTIzIDExOjI1XCIsXCJiaWtlXCI6MTk2NixcImJhdHRlcnlcIjo0Mn0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAxODowM1wiLFwiYmlrZVwiOjE0MjgsXCJiYXR0ZXJ5XCI6NzZ9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA5IDA3OjEzXCIsXCJiaWtlXCI6MTAzNixcImJhdHRlcnlcIjo2fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTE2IDA3OjA2XCIsXCJiaWtlXCI6MTI2OSxcImJhdHRlcnlcIjoyOX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAwNzoyMlwiLFwiYmlrZVwiOjEzODMsXCJiYXR0ZXJ5XCI6MTd9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTE0IDE1OjIyXCIsXCJiaWtlXCI6MTg0NSxcImJhdHRlcnlcIjo1Nn0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAwNzowOFwiLFwiYmlrZVwiOjE4NTcsXCJiYXR0ZXJ5XCI6NTB9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAxNTo1N1wiLFwiYmlrZVwiOjE2MDcsXCJiYXR0ZXJ5XCI6Njd9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTIyIDExOjIwXCIsXCJiaWtlXCI6MTk3NSxcImJhdHRlcnlcIjo5Nn0se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTggMTI6NDFcIixcImJpa2VcIjoxNjc0LFwiYmF0dGVyeVwiOjc2fSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTE5IDEzOjQyXCIsXCJiaWtlXCI6MTMzNSxcImJhdHRlcnlcIjo2MH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTkgMDY6MjlcIixcImJpa2VcIjoxOTU3LFwiYmF0dGVyeVwiOjQ1fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMTMgMTE6MzhcIixcImJpa2VcIjoxMTc0LFwiYmF0dGVyeVwiOjI4fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTIwIDE0OjA5XCIsXCJiaWtlXCI6MTg5OCxcImJhdHRlcnlcIjo0OX0se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMTI6MjRcIixcImJpa2VcIjoxMjgyLFwiYmF0dGVyeVwiOjUyfSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAwNzoxOFwiLFwiYmlrZVwiOjE2MzUsXCJiYXR0ZXJ5XCI6NjZ9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTExIDEyOjM2XCIsXCJiaWtlXCI6MTg0MyxcImJhdHRlcnlcIjo0N30se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTA2IDA3OjAxXCIsXCJiaWtlXCI6MTI4NSxcImJhdHRlcnlcIjozOX0se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMjggMTM6MTBcIixcImJpa2VcIjoxNzg3LFwiYmF0dGVyeVwiOjcyfSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxNzozNlwiLFwiYmlrZVwiOjEyOTksXCJiYXR0ZXJ5XCI6Nzh9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTI2IDExOjM4XCIsXCJiaWtlXCI6MTkzNCxcImJhdHRlcnlcIjoyMX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAxNToxM1wiLFwiYmlrZVwiOjE4MzIsXCJiYXR0ZXJ5XCI6MTZ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDIgMTY6MDVcIixcImJpa2VcIjoxMTY0LFwiYmF0dGVyeVwiOjgzfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAwNjo0MlwiLFwiYmlrZVwiOjE3MTIsXCJiYXR0ZXJ5XCI6ODF9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTAyIDE0OjMzXCIsXCJiaWtlXCI6MTM1NixcImJhdHRlcnlcIjoxNX0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMTU6MzhcIixcImJpa2VcIjoxNjExLFwiYmF0dGVyeVwiOjcxfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0wOCAxNzowNFwiLFwiYmlrZVwiOjEyMDUsXCJiYXR0ZXJ5XCI6Nn0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAwNzoxOFwiLFwiYmlrZVwiOjE0MjksXCJiYXR0ZXJ5XCI6Mjh9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA5IDIxOjI5XCIsXCJiaWtlXCI6MTU4NyxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDggMDY6MzJcIixcImJpa2VcIjoxODcyLFwiYmF0dGVyeVwiOjYwfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMTY6MTFcIixcImJpa2VcIjoxNjY5LFwiYmF0dGVyeVwiOjk2fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMTY6MjNcIixcImJpa2VcIjoxODg4LFwiYmF0dGVyeVwiOjE0fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAxMTo1NVwiLFwiYmlrZVwiOjEzODcsXCJiYXR0ZXJ5XCI6ODB9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAwNjoxMlwiLFwiYmlrZVwiOjE3MzgsXCJiYXR0ZXJ5XCI6NTF9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6MDJcIixcImJpa2VcIjoxMzAwLFwiYmF0dGVyeVwiOjI5fSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDMgMTg6NTVcIixcImJpa2VcIjoxNzYwLFwiYmF0dGVyeVwiOjg2fSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxMDozMVwiLFwiYmlrZVwiOjE1MzksXCJiYXR0ZXJ5XCI6OTF9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTAyIDIyOjA1XCIsXCJiaWtlXCI6MTA3OCxcImJhdHRlcnlcIjo2MH0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTIyIDA2OjA2XCIsXCJiaWtlXCI6MTI0NSxcImJhdHRlcnlcIjo2OX0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAwODo1NFwiLFwiYmlrZVwiOjE0NjgsXCJiYXR0ZXJ5XCI6NzB9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yOCAxNDo0NVwiLFwiYmlrZVwiOjE3NzUsXCJiYXR0ZXJ5XCI6ODJ9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAwOTozMFwiLFwiYmlrZVwiOjE3NjksXCJiYXR0ZXJ5XCI6OTZ9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAwNjoyMVwiLFwiYmlrZVwiOjE2NzUsXCJiYXR0ZXJ5XCI6N30se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTIgMDg6MjdcIixcImJpa2VcIjoxODUxLFwiYmF0dGVyeVwiOjYzfSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAxMTowMlwiLFwiYmlrZVwiOjE0ODIsXCJiYXR0ZXJ5XCI6OTZ9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAxMzowMVwiLFwiYmlrZVwiOjE1MzAsXCJiYXR0ZXJ5XCI6NDZ9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTQ6MzhcIixcImJpa2VcIjoxNDM5LFwiYmF0dGVyeVwiOjUyfSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTAzIDExOjU0XCIsXCJiaWtlXCI6MTE2NixcImJhdHRlcnlcIjo5N30se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wOCAxMDoxMFwiLFwiYmlrZVwiOjE1MzMsXCJiYXR0ZXJ5XCI6OTJ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTY6MDZcIixcImJpa2VcIjoxMjYwLFwiYmF0dGVyeVwiOjQ0fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDUgMDY6NTRcIixcImJpa2VcIjoxMTAxLFwiYmF0dGVyeVwiOjExfSx7XCJzdGF0aW9uXCI6XCJLb23DoXJvdlwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMjE6MzNcIixcImJpa2VcIjoxMTMzLFwiYmF0dGVyeVwiOjUwfSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTAyIDIxOjM4XCIsXCJiaWtlXCI6MTA5NyxcImJhdHRlcnlcIjo5M30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0yMiAwODo0OVwiLFwiYmlrZVwiOjE2MzYsXCJiYXR0ZXJ5XCI6MTl9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTA1IDE4OjQ2XCIsXCJiaWtlXCI6MTA3MyxcImJhdHRlcnlcIjozOH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMjE6MDBcIixcImJpa2VcIjoxMzE1LFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTA5IDE3OjEyXCIsXCJiaWtlXCI6MTIwMixcImJhdHRlcnlcIjo1N30se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMDY6MTJcIixcImJpa2VcIjoxMDY5LFwiYmF0dGVyeVwiOjYxfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTY6NDFcIixcImJpa2VcIjoxNzMwLFwiYmF0dGVyeVwiOjUxfSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAwNjo0NlwiLFwiYmlrZVwiOjE0NjAsXCJiYXR0ZXJ5XCI6NDB9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxMDowOVwiLFwiYmlrZVwiOjE2MjUsXCJiYXR0ZXJ5XCI6OTB9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI0IDE3OjU5XCIsXCJiaWtlXCI6MTY4MyxcImJhdHRlcnlcIjoxNn0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTE6MzJcIixcImJpa2VcIjoxMjA4LFwiYmF0dGVyeVwiOjYxfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAxMjoyOFwiLFwiYmlrZVwiOjE3ODUsXCJiYXR0ZXJ5XCI6MzB9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAwNzo1M1wiLFwiYmlrZVwiOjExNDEsXCJiYXR0ZXJ5XCI6NjJ9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAwOToxOFwiLFwiYmlrZVwiOjExODMsXCJiYXR0ZXJ5XCI6NTJ9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAyMjowNlwiLFwiYmlrZVwiOjEzMjcsXCJiYXR0ZXJ5XCI6OTB9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMDY6MjhcIixcImJpa2VcIjoxNjA3LFwiYmF0dGVyeVwiOjkwfSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAxODoxNFwiLFwiYmlrZVwiOjEzNjUsXCJiYXR0ZXJ5XCI6MTJ9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTIwIDA2OjMyXCIsXCJiaWtlXCI6MTcxNyxcImJhdHRlcnlcIjozOH0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAxNzo0OFwiLFwiYmlrZVwiOjEyMTYsXCJiYXR0ZXJ5XCI6Mzd9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTIwIDE0OjIzXCIsXCJiaWtlXCI6MTQ4OSxcImJhdHRlcnlcIjo5Nn0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wMSAwODoxMlwiLFwiYmlrZVwiOjExOTgsXCJiYXR0ZXJ5XCI6Mjl9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTE1IDE3OjI3XCIsXCJiaWtlXCI6MTI0NyxcImJhdHRlcnlcIjo3M30se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMTIgMDk6NDRcIixcImJpa2VcIjoxODMzLFwiYmF0dGVyeVwiOjIyfSx7XCJzdGF0aW9uXCI6XCJMdcW+w6Fua3lcIixcImF0XCI6XCIyMDI2LTEwLTIyIDIxOjUyXCIsXCJiaWtlXCI6MTk0NCxcImJhdHRlcnlcIjo3OX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA1IDIxOjI1XCIsXCJiaWtlXCI6MTAyOSxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMDY6NTNcIixcImJpa2VcIjoxODc3LFwiYmF0dGVyeVwiOjE1fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMTM6MDJcIixcImJpa2VcIjoxNTU3LFwiYmF0dGVyeVwiOjczfSx7XCJzdGF0aW9uXCI6XCJLb23DoXJvdlwiLFwiYXRcIjpcIjIwMjYtMTAtMjAgMTc6MzBcIixcImJpa2VcIjoxNTA1LFwiYmF0dGVyeVwiOjc4fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxNzozNlwiLFwiYmlrZVwiOjExNzksXCJiYXR0ZXJ5XCI6ODh9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yMiAyMTo1M1wiLFwiYmlrZVwiOjE0MjMsXCJiYXR0ZXJ5XCI6NTl9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTY6MjJcIixcImJpa2VcIjoxNzUyLFwiYmF0dGVyeVwiOjI1fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTEwIDEyOjUzXCIsXCJiaWtlXCI6MTM0NCxcImJhdHRlcnlcIjo5MX0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxNjoxNFwiLFwiYmlrZVwiOjE5MzcsXCJiYXR0ZXJ5XCI6NzJ9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTAzIDEzOjI0XCIsXCJiaWtlXCI6MTQxMCxcImJhdHRlcnlcIjo4NH0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMTo0M1wiLFwiYmlrZVwiOjEzMTcsXCJiYXR0ZXJ5XCI6Mzh9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAyMjowMlwiLFwiYmlrZVwiOjEwMTIsXCJiYXR0ZXJ5XCI6MzR9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxMzo1NFwiLFwiYmlrZVwiOjE0NzIsXCJiYXR0ZXJ5XCI6Mzd9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAyMjowMFwiLFwiYmlrZVwiOjE5NDksXCJiYXR0ZXJ5XCI6Nzl9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTAzIDE4OjA0XCIsXCJiaWtlXCI6MTUyNCxcImJhdHRlcnlcIjo2fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxNToyNFwiLFwiYmlrZVwiOjE2NzMsXCJiYXR0ZXJ5XCI6NDB9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTEyIDE4OjA2XCIsXCJiaWtlXCI6MTIzMixcImJhdHRlcnlcIjoxMX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0yNSAwOToyMlwiLFwiYmlrZVwiOjE5NzIsXCJiYXR0ZXJ5XCI6ODV9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTExIDE2OjI5XCIsXCJiaWtlXCI6MTAxMixcImJhdHRlcnlcIjoyMn0se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMTcgMDk6MTFcIixcImJpa2VcIjoxNDY2LFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDMgMTQ6MzNcIixcImJpa2VcIjoxNjk4LFwiYmF0dGVyeVwiOjY4fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTI3IDIxOjA4XCIsXCJiaWtlXCI6MTI0NCxcImJhdHRlcnlcIjo1fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yMSAxMzowOFwiLFwiYmlrZVwiOjEyNDgsXCJiYXR0ZXJ5XCI6NzZ9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTIxIDEwOjIyXCIsXCJiaWtlXCI6MTA4NyxcImJhdHRlcnlcIjo0MX0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAyMToxN1wiLFwiYmlrZVwiOjE1NTIsXCJiYXR0ZXJ5XCI6MTR9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI0IDE1OjUzXCIsXCJiaWtlXCI6MTg1NixcImJhdHRlcnlcIjo3MH0se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTAgMTg6NDRcIixcImJpa2VcIjoxMTM1LFwiYmF0dGVyeVwiOjI5fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTI0IDIxOjM2XCIsXCJiaWtlXCI6MTM0NSxcImJhdHRlcnlcIjo2Mn0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAwNjoxNVwiLFwiYmlrZVwiOjE3OTMsXCJiYXR0ZXJ5XCI6MzF9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxNDozNlwiLFwiYmlrZVwiOjE5NTYsXCJiYXR0ZXJ5XCI6NTV9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTAyIDE1OjE2XCIsXCJiaWtlXCI6MTQ5OCxcImJhdHRlcnlcIjo3NX0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTI6MjZcIixcImJpa2VcIjoxMzMxLFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xOCAwNjoxN1wiLFwiYmlrZVwiOjExNzMsXCJiYXR0ZXJ5XCI6ODh9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTAxIDE1OjU3XCIsXCJiaWtlXCI6MTg1NyxcImJhdHRlcnlcIjoyOX0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTI0IDA2OjU5XCIsXCJiaWtlXCI6MTU3MCxcImJhdHRlcnlcIjozOX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAyMDoxM1wiLFwiYmlrZVwiOjEzNDEsXCJiYXR0ZXJ5XCI6MzZ9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAwODo0M1wiLFwiYmlrZVwiOjE5NTksXCJiYXR0ZXJ5XCI6MTZ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTA3IDIyOjIwXCIsXCJiaWtlXCI6MTI0MyxcImJhdHRlcnlcIjo2N30se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTI6MzVcIixcImJpa2VcIjoxNjI5LFwiYmF0dGVyeVwiOjYwfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAxMDoxMlwiLFwiYmlrZVwiOjE2NjUsXCJiYXR0ZXJ5XCI6NDl9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxOTo1NlwiLFwiYmlrZVwiOjE4MTQsXCJiYXR0ZXJ5XCI6MTR9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEzIDIwOjIwXCIsXCJiaWtlXCI6MTE1MyxcImJhdHRlcnlcIjo3Nn0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTE6MzFcIixcImJpa2VcIjoxNzM5LFwiYmF0dGVyeVwiOjM3fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMDg6MTVcIixcImJpa2VcIjoxNDc2LFwiYmF0dGVyeVwiOjk2fV19IiwiUmVjZWl2ZWRBdCI6IjIwMjYtMTAtMjAgMTE6MzM6NDIiLCJGYWN0cyI6Ilt7XCJhdFwiOlwiMjAyNi0xMC0xNFQyMjo1NjowM1pcIixcImJ5XCI6XCJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdFwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSBkZXBvdCBjb25maXJtZWQgYSBmbGF0IHR5cmUgZmF1bHQgb24gYmlrZSAxMDc3IGF0IE5vdsOpIHNhZHkuXCIsXCJ0eXBlXCI6XCJyZXF1ZXN0XCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2UyMmUwZGZlZjkzNmZhNTcyYTcyXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTI0VDE2OjU1OjU2WlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSBkZXBvdCBjb25maXJtZWQgYSBmbGF0IHR5cmUgZmF1bHQgb24gYmlrZSAxNTI1IGF0IEtvbcOhcm92LlwiLFwidHlwZVwiOlwicmVxdWVzdFwiLFwicXVvdGVcIjpcIlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV8zNWEzMjNjOTA5MjQzNDU2YTIyMlwifSx7XCJhdFwiOlwiMjAyNi0xMC0xMFQxMDoxNDowOFpcIixcImJ5XCI6XCJyaWRlclwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBsb2NrIGZhdWx0IG9uIGJpa2UgMTYwNiBhdCBLcsOhbG92byBQb2xlLlwiLFwidHlwZVwiOlwiY29tcGxhaW50XCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2YxM2IxZDYxZWNjOGE5Nzc5M2QwXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTIxVDA3OjA3OjE0WlwiLFwiYnlcIjpcImN1c3RvbWVyIGNhcmVcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDE5OTkgYXQgVsO9c3RhdmnFoXTEmy5cIixcInR5cGVcIjpcInByb21pc2VcIixcInF1b3RlXCI6XCJQxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfY2E4NmEwMjdlOWFkMzYyNWNlM2FcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTdUMTE6MjM6MjVaXCIsXCJieVwiOlwiY3VzdG9tZXIgY2FyZVwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTEwOCBhdCBLcsOhbG92byBQb2xlLlwiLFwidHlwZVwiOlwiY29tcGxhaW50XCIsXCJxdW90ZVwiOlwiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2Q2NmFiODc1OWE3Y2U1N2U3MWNhXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTE3VDA3OjI4OjIyWlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxNzE3IGF0IEhsYXZuw60gbsOhZHJhxb7DrS5cIixcInR5cGVcIjpcImluZm9ybWF0aW9uXCIsXCJxdW90ZVwiOlwiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2Q0ZTNhYjQ3NDkyOGQ0OTgxMDRiXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTExVDE0OjU5OjU0WlwiLFwiYnlcIjpcInJpZGVyXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHJpZGVyIHJlcG9ydGVkIGEgZGlzcGxheSBmYXVsdCBvbiBiaWtlIDE0NDIgYXQgQnlzdHJjIHDFmcOtc3RhdmnFoXTEmy5cIixcInR5cGVcIjpcImluZm9ybWF0aW9uXCIsXCJxdW90ZVwiOlwiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2RlY2I1OGMyZmQwZmUzOTM4MWJkXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTIwVDA5OjM0OjQyWlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTU1MyBhdCBLb23DoXJvdi5cIixcInR5cGVcIjpcImNvbXBsYWludFwiLFwicXVvdGVcIjpcIktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfODY0ZjUzZGI3NjE5MzRjNGM1YzFcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTFUMjE6MjY6NTZaXCIsXCJieVwiOlwib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3RcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDE0MTIgYXQgU3RhcsO9IEzDrXNrb3ZlYy5cIixcInR5cGVcIjpcInJlcXVlc3RcIixcInF1b3RlXCI6XCJQcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfNjA4MjQzMWFlMjVjM2ZmZTY4ZmRcIn0se1wiYXRcIjpcIjIwMjYtMTAtMjJUMTQ6MzE6MjNaXCIsXCJieVwiOlwic2VydmljZSB0ZWNobmljaWFuXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTk0MiBhdCBLcsOhbG92byBQb2xlLlwiLFwidHlwZVwiOlwicHJvbWlzZVwiLFwicXVvdGVcIjpcIkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfZDA1NzAzMzhkNzFkNjdmODE4ODRcIn0se1wiYXRcIjpcIjIwMjYtMTAtMDhUMTk6Mzg6NDNaXCIsXCJieVwiOlwiY3VzdG9tZXIgY2FyZVwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBraWNrc3RhbmQgZmF1bHQgb24gYmlrZSAxNDQwIGF0IEJ5c3RyYyBwxZnDrXN0YXZpxaF0xJsuXCIsXCJ0eXBlXCI6XCJjb21wbGFpbnRcIixcInF1b3RlXCI6XCJExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2NjYmZhYWJmNmJmNjJlMmVkM2ZhXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTE3VDE3OjMzOjEyWlwiLFwiYnlcIjpcImN1c3RvbWVyIGNhcmVcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxNzk0IGF0IEtvbcOhcm92LlwiLFwidHlwZVwiOlwicHJvbWlzZVwiLFwicXVvdGVcIjpcIktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfY2I4YWU4NWVlMDBhOTcxODNiZjlcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTJUMjE6MjQ6MzRaXCIsXCJieVwiOlwib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3RcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiB0aGUgZGVwb3QgY29uZmlybWVkIGEgc2FkZGxlIGZhdWx0IG9uIGJpa2UgMTM4MCBhdCBLcmF2w60gaG9yYS5cIixcInR5cGVcIjpcInJlcXVlc3RcIixcInF1b3RlXCI6XCJaw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2Q2NmRkMDIxZTc2N2Y0ZjFjN2NhXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTEwVDA4OjUwOjQzWlwiLFwiYnlcIjpcInJpZGVyXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHJpZGVyIHJlcG9ydGVkIGEgbG9jayBmYXVsdCBvbiBiaWtlIDE2NDkgYXQgS29tw6Fyb3YuXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV9mOGU3ZDk3Yjc4ZDJjNGUxYjhkNlwifSx7XCJhdFwiOlwiMjAyNi0xMC0wMlQxMTo0MTo1OFpcIixcImJ5XCI6XCJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdFwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDE1NTcgYXQgTm92w6kgc2FkeS5cIixcInR5cGVcIjpcInByb21pc2VcIixcInF1b3RlXCI6XCJTZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV8zNGI2YjU5YzFhMDUxNTY1ODgwOFwifSx7XCJhdFwiOlwiMjAyNi0xMC0yNlQyMToxNzo1MlpcIixcImJ5XCI6XCJzZXJ2aWNlIHRlY2huaWNpYW5cIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxNDQ1IGF0IEJ5c3RyYyBwxZnDrXN0YXZpxaF0xJsuXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfYTJkYTc1ZWVlMzI3MTYxNDI1NDRcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTdUMDk6MjI6MzBaXCIsXCJieVwiOlwic2VydmljZSB0ZWNobmljaWFuXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogY3VzdG9tZXIgY2FyZSBwcm9taXNlZCBhIGxvY2sgZmF1bHQgb24gYmlrZSAxMjM0IGF0IE5vdsOpIHNhZHkuXCIsXCJ0eXBlXCI6XCJyZXF1ZXN0XCIsXCJxdW90ZVwiOlwiU2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfZDVhYzFmYWVkYWNjNjkxZjlmOWFcIn0se1wiYXRcIjpcIjIwMjYtMTAtMjRUMTA6MjI6NDhaXCIsXCJieVwiOlwib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3RcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGRpc3BsYXkgZmF1bHQgb24gYmlrZSAxMjgyIGF0IEtyw6Fsb3ZvIFBvbGUuXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV9kMTMwNmIyN2I0ODcwYzFmMWQ0YVwifSx7XCJhdFwiOlwiMjAyNi0xMC0wMlQxNzoxNjoxMVpcIixcImJ5XCI6XCJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdFwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBzYWRkbGUgZmF1bHQgb24gYmlrZSAxODk0IGF0IE7DoW3Em3N0w60gTcOtcnUuXCIsXCJ0eXBlXCI6XCJwcm9taXNlXCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5Xzc5ZDc4M2FjMDAxMjVhYzFlZWFmXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTI1VDEzOjEyOjU1WlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgY2hhaW4gZmF1bHQgb24gYmlrZSAxMTg1IGF0IE7DoW3Em3N0w60gTcOtcnUuXCIsXCJ0eXBlXCI6XCJwcm9taXNlXCIsXCJxdW90ZVwiOlwiUHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5XzcwZWYzMTAyYjBlZDIxOTgzOTU0XCJ9LHtcImF0XCI6XCIyMDI2LTEwLTIzVDIxOjU4OjEyWlwiLFwiYnlcIjpcIm9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90XCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBjaGFpbiBmYXVsdCBvbiBiaWtlIDEzNzUgYXQgS3JhdsOtIGhvcmEuXCIsXCJ0eXBlXCI6XCJyZXF1ZXN0XCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5Xzk0ZjI3MWY4YTE0ODBmMWZjM2Y3XCJ9LHtcImF0XCI6XCIyMDI2LTEwLTI0VDExOjEwOjI1WlwiLFwiYnlcIjpcIm9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90XCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBsaWdodCBmYXVsdCBvbiBiaWtlIDE3NjkgYXQgw5p2b3ouXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfNmUwMDJiOWMwYTUwYzQwMmUxYzhcIn1dIn0=') using utf8mb4);
set @n = convert(from_base64('eyJFeHRlcm5hbElkIjoiYWN0aXZpdHlfZjJjZDUzNDJiYjlhZTFkNTA2MTciLCJSZXBseUV4dGVybmFsSWQiOm51bGwsIlN0YXR1c0lkIjo0LCJMb2NrZWRVbnRpbCI6bnVsbCwiSW5jb21pbmdNZXNzYWdlVGV4dCI6IjxkaXYgbGFuZz1cImNzXCI+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxibG9ja3F1b3RlPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L2Jsb2NrcXVvdGU+PC9kaXY+IiwiU3VnZ2VzdGVkUmVwbHlUZXh0IjoiPHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+IiwiU2lnbmF0dXJlIjoiWsOha2F6bmlja8OhIHBvZHBvcmEgwrcgdGVsLjogMDM3MyA4MDYgNzAzIMK3IEUtbWFpbDogcG9kcG9yYUBleGFtcGxlLmNvbSJ9') using utf8mb4);
set @ticketId = (select max(id) + 1 from ticket);
set @noteId = (select max(id) + 1 from ticket_note);

insert into ticket (id, rider_id, city_id, subject, email, external_id, external_json, received_at, facts)
select @ticketId, json_value(@g, '$.RiderId'), json_value(@g, '$.CityId'), json_value(@g, '$.Subject'), json_value(@g, '$.Email'), json_value(@g, '$.ExternalId'), json_value(@g, '$.ExternalJsonData'), json_value(@g, '$.ReceivedAt'), json_value(@g, '$.Facts');

insert into ticket_note (id, ticket_id, external_id, status_id, incoming_text, suggested_text)
select @noteId, @ticketId, json_value(@n, '$.ExternalId'), json_value(@n, '$.StatusId'), json_value(@n, '$.IncomingMessageText'), json_value(@n, '$.SuggestedReplyText');

select @ticketId ticket_id, @noteId note_id; -- clone of test ticket 1879
```

> **Error:** SQL Error [1906] [HY000]: (conn=122) The value specified for generated column 'has_photo' in table 'ticket' has been ignored

_0 rows · 0.4 s_

## 10:55:51 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 202220 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/7382?tab=history"},{"type":"string","title":"Searched","value":"ride 194918: 1 found"},{"type":"multiline","title":"Ticket… |

_1 rows · 0.9 s_

## 10:58:36 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1202 | light | 2026-10-23 |
| 1262 | bell | 2026-10-06 |
| 1936 | brake | 2026-10-08 |
| 1581 | chain | 2026-10-17 |
| 1716 | lock | 2026-10-04 |
| 1672 | lock | 2026-10-27 |
| 1942 | battery | 2026-10-07 |
| 1888 | brake | 2026-10-04 |
| 1330 | bell | 2026-10-04 |
| 1853 | chain | 2026-10-05 |
| 1423 | kickstand | 2026-10-06 |
| 1884 | lock | 2026-10-08 |
| 1342 | saddle | 2026-10-08 |
| 1667 | lock | 2026-10-28 |
| 1642 | battery | 2026-10-08 |
| 1987 | light | 2026-10-28 |
| 1839 | kickstand | 2026-10-05 |
| 1067 | light | 2026-10-10 |
| 1441 | saddle | 2026-10-05 |
| 1968 | display | 2026-10-26 |
| 1858 | flat tyre | 2026-10-04 |
| 1907 | display | 2026-10-21 |
| 1397 | brake | 2026-10-13 |
| 1712 | display | 2026-10-30 |
| 1399 | battery | 2026-10-20 |
| 1660 | kickstand | 2026-10-21 |
| 1909 | bell | 2026-10-24 |
| 1025 | kickstand | 2026-10-01 |
| 1804 | saddle | 2026-10-14 |
| 1146 | light | 2026-10-29 |
| 1676 | brake | 2026-10-18 |
| 1310 | saddle | 2026-10-25 |
| 1126 | battery | 2026-10-18 |
| 1465 | brake | 2026-10-30 |
| 1845 | bell | 2026-10-24 |
| 1275 | lock | 2026-10-02 |

_36 rows · 0.5 s_

## 11:03:14 · bikes-localhost / bikeshare (read-write) · local tickets with facts

```sql
select count(*) from ticket_note where facts is not null
```

| count(*) |
|---|
| 32 |

_1 rows · 1.1 s_

## 11:09:27 · bikes-prod / bikeshare_prod (read-only) · free docks per station

```sql
select s.name, count(*) free_docks
from dock d join station s on s.id = d.station_id
where d.bike_id is null group by s.name order by free_docks desc
```

| name | free_docks |
|---|---|
| Náměstí Míru | 15 |
| Hlavní nádraží | 4 |
| Výstaviště | 1 |
| Mendlovo náměstí | 17 |
| Lužánky | 12 |
| Královo Pole | 15 |
| Žabovřesky | 8 |
| Komárov | 20 |
| Starý Lískovec | 14 |
| Bystrc přístaviště | 10 |
| Kraví hora | 3 |
| Vaňkovka | 23 |
| Úvoz | 9 |
| Moravské náměstí | 20 |
| Nové sady | 14 |

_15 rows · 1.4 s_

## 11:13:57 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Ondřej Marek | senior |
| Tomáš Král | senior |
| Lucie Benešová | senior |
| Jakub Fiala | senior |
| Eva Horáková | senior |
| Martin Procházka | student |
| Tomáš Král | company |
| Tomáš Král | company |
| Martin Procházka | student |
| Jana Dvořáková | company |
| Tomáš Král | senior |
| Ondřej Marek | senior |

_12 rows · 0.8 s_

## 11:14:22 · bikes-localhost / bikeshare (read-write) · generated columns on ticket tables

```sql
select column_name, generation_expression from information_schema.columns where table_name in ('ticket','ticket_note') and generation_expression is not null
```

| column_name | generation_expression |
|---|---|
| has_photo | json_contains_path(`external_json`,'one','$.photos') |

_1 rows · 2.6 s_

## 11:15:21 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Eva Horáková | senior |
| Jakub Fiala | company |
| Jana Dvořáková | senior |
| Eva Horáková | student |
| Jakub Fiala | company |
| Petr Novotný | senior |
| Jakub Fiala | student |

_7 rows · 0.7 s_

## 11:19:12 · bikes-test / bikeshare_test (read-only) · select id, meta from station where meta is not null limit 5

```sql
select id, meta from station where meta is not null limit 5
```

| id | meta |
|---|---|
| 95 | {"station":"Výstaviště","docks":20,"lat":49.20582,"lon":16.62588,"notes":"Prosím o vrácení poplatku 49 Kč za nedokončenou jízdu.","contacts":["Petr Novotný","Zuzana Pokorná"]} |
| 100 | {"station":"Královo Pole","docks":30,"lat":49.19707,"lon":16.61033,"notes":"Děkuji za rychlé vyřízení, kredit jsem dostala.","contacts":["Jana Dvořáková","Ondřej Marek"]} |
| 107 | {"station":"Hlavní nádraží","docks":16,"lat":49.19958,"lon":16.60741,"notes":"Kolo na stanici Lužánky má prasklou pneumatiku, prosím o výměnu.","contacts":["Tomáš Král","Petr Novotný"]} |
| 51 | {"station":"Mendlovo náměstí","docks":24,"lat":49.20743,"lon":16.6408,"notes":"Zámek se neodemkl ani na třetí pokus, jízda se mi přesto účtovala.","contacts":["Zuzana Pokorná","Petr Novotný"]} |

_4 rows · 0.2 s_

## 11:23:04 · bikes-localhost / bikeshare (read-write) · local tickets with facts

```sql
select count(*) from ticket_note where facts is not null
```

| count(*) |
|---|
| 1 |

_1 rows · 0.8 s_

## 11:24:47 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 203726 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/1776?tab=history"},{"type":"string","title":"Searched","value":"ride 145225: 1 found"},{"type":"multiline","title":"Ticket… |
| 202494 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/5758?tab=history"},{"type":"string","title":"Searched","value":"ride 135932: 1 found"},{"type":"multiline","title":"Ticket… |
| 207481 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/1848?tab=history"},{"type":"string","title":"Searched","value":"ride 177322: 1 found"},{"type":"multiline","title":"Ticket… |

_3 rows · 2.2 s_

## 11:27:41 · bikes-prod / bikeshare_prod (read-only) · rides by hour of day

```sql
select hour(started_at) h, count(*) n from ride where started_at >= '2026-10-01' group by h order by h
```

| h | n |
|---|---|
| 0 | 1064 |
| 1 | 189 |
| 2 | 903 |
| 3 | 3957 |
| 4 | 357 |
| 5 | 2945 |
| 6 | 1303 |
| 7 | 921 |
| 8 | 1250 |
| 9 | 400 |
| 10 | 961 |
| 11 | 1782 |
| 12 | 867 |
| 13 | 1414 |
| 14 | 2888 |
| 15 | 2646 |
| 16 | 3795 |
| 17 | 3331 |
| 18 | 3440 |
| 19 | 3058 |
| 20 | 1014 |
| 21 | 2717 |
| 22 | 1886 |
| 23 | 408 |

_24 rows · 1.0 s_

## 11:31:53 · bikes-localhost / bikeshare (WRITE) · clone test ticket 1879 locally

```sql
set @g = convert(from_base64('eyJSaWRlcklkIjo4MDAsIkNpdHlJZCI6MywiU3ViamVjdCI6IlJFOiBqw616ZGEgMTkwMzcwIiwiRW1haWwiOiJyaWRlckBleGFtcGxlLmNvbSIsIkV4dGVybmFsSWQiOiIxODc5IiwiRXh0ZXJuYWxKc29uRGF0YSI6IntcImlkXCI6MTg3OSxcImNoYW5uZWxcIjpcImVtYWlsXCIsXCJzdGF0aW9uSGlzdG9yeVwiOlt7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAwNjowNVwiLFwiYmlrZVwiOjE0MDMsXCJiYXR0ZXJ5XCI6OTR9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEyIDExOjI1XCIsXCJiaWtlXCI6MTAxOSxcImJhdHRlcnlcIjo1OX0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMTc6MTNcIixcImJpa2VcIjoxOTY3LFwiYmF0dGVyeVwiOjEwMH0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI0IDE4OjExXCIsXCJiaWtlXCI6MTExOSxcImJhdHRlcnlcIjo1N30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xOCAxNjoyMVwiLFwiYmlrZVwiOjE4NzQsXCJiYXR0ZXJ5XCI6NDl9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjQgMTA6MDZcIixcImJpa2VcIjoxNzEyLFwiYmF0dGVyeVwiOjM0fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAwNjoxM1wiLFwiYmlrZVwiOjE4NTEsXCJiYXR0ZXJ5XCI6OTN9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMDcgMTE6MDdcIixcImJpa2VcIjoxNDM0LFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxMzozOFwiLFwiYmlrZVwiOjE2OTgsXCJiYXR0ZXJ5XCI6MjZ9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA5IDE4OjEwXCIsXCJiaWtlXCI6MTIzMSxcImJhdHRlcnlcIjozNH0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTA2IDA4OjEwXCIsXCJiaWtlXCI6MTEzNSxcImJhdHRlcnlcIjoxMX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTIxIDE0OjQ3XCIsXCJiaWtlXCI6MTg1OCxcImJhdHRlcnlcIjo5fSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAyMjo0N1wiLFwiYmlrZVwiOjExNzksXCJiYXR0ZXJ5XCI6NjR9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMTAgMTc6MTlcIixcImJpa2VcIjoxMTYyLFwiYmF0dGVyeVwiOjE3fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTE5IDEzOjEyXCIsXCJiaWtlXCI6MTM1MCxcImJhdHRlcnlcIjozNX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI1IDExOjUyXCIsXCJiaWtlXCI6MTk2NyxcImJhdHRlcnlcIjo2MX0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTk6MzhcIixcImJpa2VcIjoxODgyLFwiYmF0dGVyeVwiOjY4fSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTI0IDE1OjQwXCIsXCJiaWtlXCI6MTE3OSxcImJhdHRlcnlcIjo4fSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAxNDo1NFwiLFwiYmlrZVwiOjEzODIsXCJiYXR0ZXJ5XCI6NX0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTAyIDA2OjI2XCIsXCJiaWtlXCI6MTQwMCxcImJhdHRlcnlcIjozNH0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAxODo1NFwiLFwiYmlrZVwiOjE1MzksXCJiYXR0ZXJ5XCI6Nzd9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTAxIDE0OjI5XCIsXCJiaWtlXCI6MTQ3OSxcImJhdHRlcnlcIjo1NH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTE6MjBcIixcImJpa2VcIjoxNjI3LFwiYmF0dGVyeVwiOjl9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTI1IDE1OjUwXCIsXCJiaWtlXCI6MTMzNixcImJhdHRlcnlcIjo3N30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxMjo0MlwiLFwiYmlrZVwiOjEyMDYsXCJiYXR0ZXJ5XCI6NTJ9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI3IDE0OjQwXCIsXCJiaWtlXCI6MTMwNCxcImJhdHRlcnlcIjozOX0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTIyIDEwOjMzXCIsXCJiaWtlXCI6MTYwNCxcImJhdHRlcnlcIjoxMX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA0IDA2OjU4XCIsXCJiaWtlXCI6MTg1NSxcImJhdHRlcnlcIjoyNX0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMTcgMjA6MTVcIixcImJpa2VcIjoxOTkxLFwiYmF0dGVyeVwiOjEyfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0yMiAwOToxMFwiLFwiYmlrZVwiOjE0MDksXCJiYXR0ZXJ5XCI6Nn0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTIzIDE3OjE5XCIsXCJiaWtlXCI6MTg5MCxcImJhdHRlcnlcIjo4M30se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxOTo0NlwiLFwiYmlrZVwiOjEzNDgsXCJiYXR0ZXJ5XCI6MjZ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTIwIDE4OjI3XCIsXCJiaWtlXCI6MTE2OCxcImJhdHRlcnlcIjo5Nn0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxNTo0OVwiLFwiYmlrZVwiOjEwMjMsXCJiYXR0ZXJ5XCI6MzR9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMjA6MzlcIixcImJpa2VcIjoxODQ3LFwiYmF0dGVyeVwiOjMyfSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTA2IDIwOjE0XCIsXCJiaWtlXCI6MTgzMyxcImJhdHRlcnlcIjo2M30se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI4IDEyOjQ5XCIsXCJiaWtlXCI6MTYzNCxcImJhdHRlcnlcIjoxOX0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTA4IDEwOjQ1XCIsXCJiaWtlXCI6MTExNixcImJhdHRlcnlcIjo1MX0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMDMgMTI6MjBcIixcImJpa2VcIjoxMjc5LFwiYmF0dGVyeVwiOjY3fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDcgMTk6MTlcIixcImJpa2VcIjoxMTk4LFwiYmF0dGVyeVwiOjYxfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAxMTozNFwiLFwiYmlrZVwiOjE2MjMsXCJiYXR0ZXJ5XCI6MTAwfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAyMjoyOVwiLFwiYmlrZVwiOjEwODksXCJiYXR0ZXJ5XCI6NjF9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTI4IDExOjQ0XCIsXCJiaWtlXCI6MTc4NixcImJhdHRlcnlcIjo4M30se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA1IDA3OjM4XCIsXCJiaWtlXCI6MTM0OSxcImJhdHRlcnlcIjozMX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAwNjo0MVwiLFwiYmlrZVwiOjEyOTYsXCJiYXR0ZXJ5XCI6NTd9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTE2IDIxOjIyXCIsXCJiaWtlXCI6MTUwOSxcImJhdHRlcnlcIjo3OX0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTEzIDE2OjE5XCIsXCJiaWtlXCI6MTcwMyxcImJhdHRlcnlcIjo3MX0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAxMDo1MVwiLFwiYmlrZVwiOjE0OTAsXCJiYXR0ZXJ5XCI6NDd9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTA2IDA5OjU4XCIsXCJiaWtlXCI6MTMwMSxcImJhdHRlcnlcIjoyNn0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTAyIDE5OjE1XCIsXCJiaWtlXCI6MTM0NixcImJhdHRlcnlcIjo0NX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTIwIDEzOjQ5XCIsXCJiaWtlXCI6MTM5MyxcImJhdHRlcnlcIjo1OH0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xNSAyMDoxNVwiLFwiYmlrZVwiOjE5MDAsXCJiYXR0ZXJ5XCI6NzR9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTE6MDRcIixcImJpa2VcIjoxOTMwLFwiYmF0dGVyeVwiOjYyfSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAxMTozOFwiLFwiYmlrZVwiOjE2MzQsXCJiYXR0ZXJ5XCI6NjF9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAwNzoyMVwiLFwiYmlrZVwiOjE2MzMsXCJiYXR0ZXJ5XCI6NTZ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDUgMDY6NTBcIixcImJpa2VcIjoxNDgwLFwiYmF0dGVyeVwiOjEyfSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxMDowNlwiLFwiYmlrZVwiOjE1NzUsXCJiYXR0ZXJ5XCI6N30se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTI6MzlcIixcImJpa2VcIjoxMzE5LFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTc6MTJcIixcImJpa2VcIjoxMTU5LFwiYmF0dGVyeVwiOjk1fSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAxNDo0MFwiLFwiYmlrZVwiOjExODIsXCJiYXR0ZXJ5XCI6ODR9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMDc6MjBcIixcImJpa2VcIjoxMTcxLFwiYmF0dGVyeVwiOjgyfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTA6MTdcIixcImJpa2VcIjoxNTQ1LFwiYmF0dGVyeVwiOjkyfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMTc6MjJcIixcImJpa2VcIjoxOTExLFwiYmF0dGVyeVwiOjYwfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTM6MTJcIixcImJpa2VcIjoxODcwLFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxNjoxNFwiLFwiYmlrZVwiOjE1NjUsXCJiYXR0ZXJ5XCI6NzN9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMTg6NDZcIixcImJpa2VcIjoxMTUyLFwiYmF0dGVyeVwiOjMwfSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTE1IDA4OjA1XCIsXCJiaWtlXCI6MTIzOCxcImJhdHRlcnlcIjo5fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTA3IDE4OjAwXCIsXCJiaWtlXCI6MTg3NixcImJhdHRlcnlcIjoyNn0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTYgMTY6MzFcIixcImJpa2VcIjoxNjMzLFwiYmF0dGVyeVwiOjk3fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTEzIDExOjQ5XCIsXCJiaWtlXCI6MTU3MSxcImJhdHRlcnlcIjo0M30se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMjoxM1wiLFwiYmlrZVwiOjE4NTgsXCJiYXR0ZXJ5XCI6MzR9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI3IDE0OjE2XCIsXCJiaWtlXCI6MTM4MyxcImJhdHRlcnlcIjo0Mn0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAwODozNVwiLFwiYmlrZVwiOjExNDQsXCJiYXR0ZXJ5XCI6Mjh9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTExIDA2OjEwXCIsXCJiaWtlXCI6MTkyMixcImJhdHRlcnlcIjoyOX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI4IDE4OjIyXCIsXCJiaWtlXCI6MTg1OCxcImJhdHRlcnlcIjo3Nn0se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTAgMjE6NTJcIixcImJpa2VcIjoxNTc4LFwiYmF0dGVyeVwiOjIyfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOCAwODozN1wiLFwiYmlrZVwiOjEzNDgsXCJiYXR0ZXJ5XCI6MTl9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTA3IDE5OjI0XCIsXCJiaWtlXCI6MTQ4MSxcImJhdHRlcnlcIjoxMn0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xOCAwOToyNVwiLFwiYmlrZVwiOjEzNTMsXCJiYXR0ZXJ5XCI6NTl9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDUgMTU6MzdcIixcImJpa2VcIjoxMTQ5LFwiYmF0dGVyeVwiOjI4fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAxNDozOVwiLFwiYmlrZVwiOjEwNTIsXCJiYXR0ZXJ5XCI6NjF9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTEyIDIyOjA2XCIsXCJiaWtlXCI6MTEwNyxcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTI3IDA5OjU4XCIsXCJiaWtlXCI6MTE0OSxcImJhdHRlcnlcIjo4M30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0yNiAyMTozNFwiLFwiYmlrZVwiOjEwNTQsXCJiYXR0ZXJ5XCI6MzJ9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAxMzowOVwiLFwiYmlrZVwiOjExNzUsXCJiYXR0ZXJ5XCI6NDZ9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTE2IDExOjAyXCIsXCJiaWtlXCI6MTA3NCxcImJhdHRlcnlcIjo2fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxNDo1NVwiLFwiYmlrZVwiOjE3NjksXCJiYXR0ZXJ5XCI6MjJ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTA3IDEyOjI5XCIsXCJiaWtlXCI6MTc0MCxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTU6MTRcIixcImJpa2VcIjoxMDI3LFwiYmF0dGVyeVwiOjEwfSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAwODo1NFwiLFwiYmlrZVwiOjE2ODcsXCJiYXR0ZXJ5XCI6Mzh9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAyMToxNFwiLFwiYmlrZVwiOjE3NzYsXCJiYXR0ZXJ5XCI6ODl9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMTM6MzhcIixcImJpa2VcIjoxNzU4LFwiYmF0dGVyeVwiOjUwfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxMzo0M1wiLFwiYmlrZVwiOjE1NTIsXCJiYXR0ZXJ5XCI6MzF9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTA6MDVcIixcImJpa2VcIjoxNDAwLFwiYmF0dGVyeVwiOjc2fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMTA6MzZcIixcImJpa2VcIjoxNzI2LFwiYmF0dGVyeVwiOjQ3fSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMzowNlwiLFwiYmlrZVwiOjE0ODUsXCJiYXR0ZXJ5XCI6Mjd9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0yNSAwNjo0NVwiLFwiYmlrZVwiOjE2MDIsXCJiYXR0ZXJ5XCI6OH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDIgMDY6MzRcIixcImJpa2VcIjoxMDc5LFwiYmF0dGVyeVwiOjU1fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAyMTo0MVwiLFwiYmlrZVwiOjEyMjEsXCJiYXR0ZXJ5XCI6NzB9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTAzIDE4OjUxXCIsXCJiaWtlXCI6MTA4NixcImJhdHRlcnlcIjo1MH0se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjE6MDlcIixcImJpa2VcIjoxMDE0LFwiYmF0dGVyeVwiOjczfSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAwODozM1wiLFwiYmlrZVwiOjE2NTAsXCJiYXR0ZXJ5XCI6NDd9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA3IDEwOjUyXCIsXCJiaWtlXCI6MTA0MixcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMjQgMDk6MzJcIixcImJpa2VcIjoxMTMyLFwiYmF0dGVyeVwiOjkwfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMTk6MThcIixcImJpa2VcIjoxNDUwLFwiYmF0dGVyeVwiOjIzfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMTUgMTA6NTdcIixcImJpa2VcIjoxNDUxLFwiYmF0dGVyeVwiOjd9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6MTdcIixcImJpa2VcIjoxODAyLFwiYmF0dGVyeVwiOjg2fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTI0IDExOjI0XCIsXCJiaWtlXCI6MTkzMixcImJhdHRlcnlcIjo1MX0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTI6MjhcIixcImJpa2VcIjoxNDgzLFwiYmF0dGVyeVwiOjQwfSx7XCJzdGF0aW9uXCI6XCJLb23DoXJvdlwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTI6MzRcIixcImJpa2VcIjoxNzgzLFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wMiAxNDoxNFwiLFwiYmlrZVwiOjExNDYsXCJiYXR0ZXJ5XCI6MTF9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMTUgMTg6MDhcIixcImJpa2VcIjoxMjc2LFwiYmF0dGVyeVwiOjk5fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0wMiAxMzowOFwiLFwiYmlrZVwiOjE1NDIsXCJiYXR0ZXJ5XCI6Mjl9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTE2IDE0OjAzXCIsXCJiaWtlXCI6MTkxNCxcImJhdHRlcnlcIjo2Mn0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTA5IDExOjAzXCIsXCJiaWtlXCI6MTg4NSxcImJhdHRlcnlcIjo2N30se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTI6MjJcIixcImJpa2VcIjoxNTk5LFwiYmF0dGVyeVwiOjcwfSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTEyIDE2OjA4XCIsXCJiaWtlXCI6MTM5NixcImJhdHRlcnlcIjo5NX0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTE4IDE1OjAzXCIsXCJiaWtlXCI6MTU4MixcImJhdHRlcnlcIjo3MX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI4IDE4OjQyXCIsXCJiaWtlXCI6MTIyMixcImJhdHRlcnlcIjoxNn0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMDk6NTdcIixcImJpa2VcIjoxNzgyLFwiYmF0dGVyeVwiOjMzfSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0yNiAxODo1OFwiLFwiYmlrZVwiOjE5MjYsXCJiYXR0ZXJ5XCI6OTR9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxNzo0OFwiLFwiYmlrZVwiOjEyNzEsXCJiYXR0ZXJ5XCI6MzJ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMTMgMTY6NDNcIixcImJpa2VcIjoxNDY2LFwiYmF0dGVyeVwiOjUxfSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTc6NDdcIixcImJpa2VcIjoxMDgzLFwiYmF0dGVyeVwiOjI2fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0yOCAxODo0M1wiLFwiYmlrZVwiOjE2NzYsXCJiYXR0ZXJ5XCI6MTh9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTIyIDIyOjU0XCIsXCJiaWtlXCI6MTU3OSxcImJhdHRlcnlcIjo1fSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMjE6NDdcIixcImJpa2VcIjoxODQwLFwiYmF0dGVyeVwiOjU3fSx7XCJzdGF0aW9uXCI6XCJMdcW+w6Fua3lcIixcImF0XCI6XCIyMDI2LTEwLTA2IDEwOjQ1XCIsXCJiaWtlXCI6MTMwMSxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMjA6MzlcIixcImJpa2VcIjoxMDkyLFwiYmF0dGVyeVwiOjYyfSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wMSAyMDowMFwiLFwiYmlrZVwiOjEzMjMsXCJiYXR0ZXJ5XCI6OX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI4IDE0OjA0XCIsXCJiaWtlXCI6MTEwOCxcImJhdHRlcnlcIjozOH0se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMDY6MjVcIixcImJpa2VcIjoxNjU1LFwiYmF0dGVyeVwiOjI5fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTA0IDE5OjMyXCIsXCJiaWtlXCI6MTU2NyxcImJhdHRlcnlcIjo1MX0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTExIDA5OjMxXCIsXCJiaWtlXCI6MTU0NyxcImJhdHRlcnlcIjo2NX0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNSAwODoxM1wiLFwiYmlrZVwiOjEzMDksXCJiYXR0ZXJ5XCI6NDd9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTAzIDA3OjQxXCIsXCJiaWtlXCI6MTY4MixcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTU6MTJcIixcImJpa2VcIjoxMjU2LFwiYmF0dGVyeVwiOjQ0fSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTEwIDA4OjU2XCIsXCJiaWtlXCI6MTE4MixcImJhdHRlcnlcIjo0MX0se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTQ6MDdcIixcImJpa2VcIjoxODk1LFwiYmF0dGVyeVwiOjYyfSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAwODowM1wiLFwiYmlrZVwiOjEzNzcsXCJiYXR0ZXJ5XCI6MTJ9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAxMDozOFwiLFwiYmlrZVwiOjE3NDYsXCJiYXR0ZXJ5XCI6ODF9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxNjoxMlwiLFwiYmlrZVwiOjE4NDgsXCJiYXR0ZXJ5XCI6OTV9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAxODowNVwiLFwiYmlrZVwiOjEwMjUsXCJiYXR0ZXJ5XCI6MTV9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTA2IDEzOjMzXCIsXCJiaWtlXCI6MTE5OSxcImJhdHRlcnlcIjo4N30se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTIzIDE4OjQ4XCIsXCJiaWtlXCI6MTczMSxcImJhdHRlcnlcIjozNX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAxNDo1NFwiLFwiYmlrZVwiOjE5NDUsXCJiYXR0ZXJ5XCI6ODF9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEwIDEwOjA1XCIsXCJiaWtlXCI6MTI2OSxcImJhdHRlcnlcIjo3Nn0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMDcgMTE6NTBcIixcImJpa2VcIjoxOTM2LFwiYmF0dGVyeVwiOjY1fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAxMzowOVwiLFwiYmlrZVwiOjEyNzUsXCJiYXR0ZXJ5XCI6MzF9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAwOTozN1wiLFwiYmlrZVwiOjE2MzAsXCJiYXR0ZXJ5XCI6OTh9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMjE6MTVcIixcImJpa2VcIjoxNDUwLFwiYmF0dGVyeVwiOjd9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEzIDE2OjE4XCIsXCJiaWtlXCI6MTQ0OCxcImJhdHRlcnlcIjo2OX0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAwNjoxNFwiLFwiYmlrZVwiOjE0NjUsXCJiYXR0ZXJ5XCI6Mzl9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTA1IDExOjIyXCIsXCJiaWtlXCI6MTQ0NyxcImJhdHRlcnlcIjo4MX0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6NTVcIixcImJpa2VcIjoxMTk0LFwiYmF0dGVyeVwiOjk0fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTIxIDE4OjEwXCIsXCJiaWtlXCI6MTUwNCxcImJhdHRlcnlcIjo2Nn0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI2IDIyOjM0XCIsXCJiaWtlXCI6MTk5MixcImJhdHRlcnlcIjoxN30se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA1IDIyOjU4XCIsXCJiaWtlXCI6MTc0MyxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxMjozN1wiLFwiYmlrZVwiOjE0MzYsXCJiYXR0ZXJ5XCI6MTV9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTk6MzNcIixcImJpa2VcIjoxNzc5LFwiYmF0dGVyeVwiOjYzfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMDc6MTFcIixcImJpa2VcIjoxODMyLFwiYmF0dGVyeVwiOjc3fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTI0IDA5OjE1XCIsXCJiaWtlXCI6MTk3NSxcImJhdHRlcnlcIjo3NH0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMTQ6NTZcIixcImJpa2VcIjoxODk4LFwiYmF0dGVyeVwiOjg4fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTExIDExOjMxXCIsXCJiaWtlXCI6MTY2NSxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTE0IDE0OjI2XCIsXCJiaWtlXCI6MTA3OCxcImJhdHRlcnlcIjoyMH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTA6MTNcIixcImJpa2VcIjoxNDk0LFwiYmF0dGVyeVwiOjc4fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAwNjowNVwiLFwiYmlrZVwiOjE1MzIsXCJiYXR0ZXJ5XCI6OTF9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI2IDEzOjE5XCIsXCJiaWtlXCI6MTAxOCxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTQgMTU6MDdcIixcImJpa2VcIjoxMjEzLFwiYmF0dGVyeVwiOjZ9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxNzozOFwiLFwiYmlrZVwiOjEwMjMsXCJiYXR0ZXJ5XCI6ODV9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTE4IDEzOjI0XCIsXCJiaWtlXCI6MTY1NixcImJhdHRlcnlcIjo1fSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAwNjo0N1wiLFwiYmlrZVwiOjE2NjcsXCJiYXR0ZXJ5XCI6NTN9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI1IDEwOjUwXCIsXCJiaWtlXCI6MTk3OCxcImJhdHRlcnlcIjo3fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxMToyNFwiLFwiYmlrZVwiOjE5MjksXCJiYXR0ZXJ5XCI6Njh9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTA4IDE3OjQ1XCIsXCJiaWtlXCI6MTYxNCxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAxMDozNVwiLFwiYmlrZVwiOjE1MDIsXCJiYXR0ZXJ5XCI6NTZ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTE5IDA5OjI3XCIsXCJiaWtlXCI6MTkwNyxcImJhdHRlcnlcIjo0MH0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxMjoxN1wiLFwiYmlrZVwiOjEwODEsXCJiYXR0ZXJ5XCI6MjB9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTc6MDFcIixcImJpa2VcIjoxOTM0LFwiYmF0dGVyeVwiOjE3fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxNTozM1wiLFwiYmlrZVwiOjEwMjAsXCJiYXR0ZXJ5XCI6MzV9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xNSAwOTo1MVwiLFwiYmlrZVwiOjE0NDksXCJiYXR0ZXJ5XCI6NTR9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTE3IDIyOjAzXCIsXCJiaWtlXCI6MTY3MixcImJhdHRlcnlcIjo3MH0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTI2IDA5OjE2XCIsXCJiaWtlXCI6MTk4MSxcImJhdHRlcnlcIjo1Mn0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMjA6MjlcIixcImJpa2VcIjoxMjQ5LFwiYmF0dGVyeVwiOjQ1fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMzozM1wiLFwiYmlrZVwiOjEwMTEsXCJiYXR0ZXJ5XCI6NzB9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEwIDE3OjMxXCIsXCJiaWtlXCI6MTkxMSxcImJhdHRlcnlcIjo4N30se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTAzIDE4OjQ5XCIsXCJiaWtlXCI6MTExNixcImJhdHRlcnlcIjozM30se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTIwIDEzOjAzXCIsXCJiaWtlXCI6MTIzOSxcImJhdHRlcnlcIjoyN30se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAxMjowOFwiLFwiYmlrZVwiOjE5MDQsXCJiYXR0ZXJ5XCI6OTZ9LHtcInN0YXRpb25cIjpcIkx1xb7DoW5reVwiLFwiYXRcIjpcIjIwMjYtMTAtMTQgMDg6NDNcIixcImJpa2VcIjoxMTA4LFwiYmF0dGVyeVwiOjQwfSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAxOTo0MVwiLFwiYmlrZVwiOjE2NDQsXCJiYXR0ZXJ5XCI6ODR9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMDk6NTZcIixcImJpa2VcIjoxOTAyLFwiYmF0dGVyeVwiOjE5fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjYgMTU6MTFcIixcImJpa2VcIjoxNTM0LFwiYmF0dGVyeVwiOjQxfSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxMzoyN1wiLFwiYmlrZVwiOjE1MDYsXCJiYXR0ZXJ5XCI6MTAwfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTI6MzFcIixcImJpa2VcIjoxMzA1LFwiYmF0dGVyeVwiOjEwMH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTM6MTBcIixcImJpa2VcIjoxNjI5LFwiYmF0dGVyeVwiOjkzfSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMTM6MDZcIixcImJpa2VcIjoxMTk3LFwiYmF0dGVyeVwiOjY4fSx7XCJzdGF0aW9uXCI6XCJMdcW+w6Fua3lcIixcImF0XCI6XCIyMDI2LTEwLTAzIDExOjE1XCIsXCJiaWtlXCI6MTA0NSxcImJhdHRlcnlcIjoxMn0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAwNjozN1wiLFwiYmlrZVwiOjE2MzksXCJiYXR0ZXJ5XCI6Njl9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMTE6MjRcIixcImJpa2VcIjoxMDYxLFwiYmF0dGVyeVwiOjY2fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDYgMjA6MzBcIixcImJpa2VcIjoxNzI4LFwiYmF0dGVyeVwiOjc5fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTI4IDE5OjQ5XCIsXCJiaWtlXCI6MTI3OCxcImJhdHRlcnlcIjo5OH0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTExIDE3OjQ4XCIsXCJiaWtlXCI6MTMxMCxcImJhdHRlcnlcIjo2M30se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMTIgMTU6NDhcIixcImJpa2VcIjoxMzE1LFwiYmF0dGVyeVwiOjc3fSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAyMjo0NVwiLFwiYmlrZVwiOjEyODgsXCJiYXR0ZXJ5XCI6NDR9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTI6MjBcIixcImJpa2VcIjoxMjAzLFwiYmF0dGVyeVwiOjI1fSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0yOCAxNTozNlwiLFwiYmlrZVwiOjEwODksXCJiYXR0ZXJ5XCI6Nn0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6MjVcIixcImJpa2VcIjoxNDI1LFwiYmF0dGVyeVwiOjIzfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTI6MjdcIixcImJpa2VcIjoxNzc3LFwiYmF0dGVyeVwiOjU0fSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxNTowM1wiLFwiYmlrZVwiOjE5MjIsXCJiYXR0ZXJ5XCI6NTR9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTIzIDExOjI1XCIsXCJiaWtlXCI6MTk2NixcImJhdHRlcnlcIjo0Mn0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAxODowM1wiLFwiYmlrZVwiOjE0MjgsXCJiYXR0ZXJ5XCI6NzZ9LHtcInN0YXRpb25cIjpcIkJ5c3RyYyBwxZnDrXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA5IDA3OjEzXCIsXCJiaWtlXCI6MTAzNixcImJhdHRlcnlcIjo2fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTE2IDA3OjA2XCIsXCJiaWtlXCI6MTI2OSxcImJhdHRlcnlcIjoyOX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAwNzoyMlwiLFwiYmlrZVwiOjEzODMsXCJiYXR0ZXJ5XCI6MTd9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTE0IDE1OjIyXCIsXCJiaWtlXCI6MTg0NSxcImJhdHRlcnlcIjo1Nn0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAwNzowOFwiLFwiYmlrZVwiOjE4NTcsXCJiYXR0ZXJ5XCI6NTB9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAxNTo1N1wiLFwiYmlrZVwiOjE2MDcsXCJiYXR0ZXJ5XCI6Njd9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTIyIDExOjIwXCIsXCJiaWtlXCI6MTk3NSxcImJhdHRlcnlcIjo5Nn0se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTggMTI6NDFcIixcImJpa2VcIjoxNjc0LFwiYmF0dGVyeVwiOjc2fSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTE5IDEzOjQyXCIsXCJiaWtlXCI6MTMzNSxcImJhdHRlcnlcIjo2MH0se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTkgMDY6MjlcIixcImJpa2VcIjoxOTU3LFwiYmF0dGVyeVwiOjQ1fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMTMgMTE6MzhcIixcImJpa2VcIjoxMTc0LFwiYmF0dGVyeVwiOjI4fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTIwIDE0OjA5XCIsXCJiaWtlXCI6MTg5OCxcImJhdHRlcnlcIjo0OX0se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMTI6MjRcIixcImJpa2VcIjoxMjgyLFwiYmF0dGVyeVwiOjUyfSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAwNzoxOFwiLFwiYmlrZVwiOjE2MzUsXCJiYXR0ZXJ5XCI6NjZ9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTExIDEyOjM2XCIsXCJiaWtlXCI6MTg0MyxcImJhdHRlcnlcIjo0N30se1wic3RhdGlvblwiOlwiTW9yYXZza8OpIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTA2IDA3OjAxXCIsXCJiaWtlXCI6MTI4NSxcImJhdHRlcnlcIjozOX0se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMjggMTM6MTBcIixcImJpa2VcIjoxNzg3LFwiYmF0dGVyeVwiOjcyfSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAxNzozNlwiLFwiYmlrZVwiOjEyOTksXCJiYXR0ZXJ5XCI6Nzh9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTI2IDExOjM4XCIsXCJiaWtlXCI6MTkzNCxcImJhdHRlcnlcIjoyMX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAxNToxM1wiLFwiYmlrZVwiOjE4MzIsXCJiYXR0ZXJ5XCI6MTZ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDIgMTY6MDVcIixcImJpa2VcIjoxMTY0LFwiYmF0dGVyeVwiOjgzfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAwNjo0MlwiLFwiYmlrZVwiOjE3MTIsXCJiYXR0ZXJ5XCI6ODF9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTAyIDE0OjMzXCIsXCJiaWtlXCI6MTM1NixcImJhdHRlcnlcIjoxNX0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMjUgMTU6MzhcIixcImJpa2VcIjoxNjExLFwiYmF0dGVyeVwiOjcxfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0wOCAxNzowNFwiLFwiYmlrZVwiOjEyMDUsXCJiYXR0ZXJ5XCI6Nn0se1wic3RhdGlvblwiOlwiSGxhdm7DrSBuw6FkcmHFvsOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMCAwNzoxOFwiLFwiYmlrZVwiOjE0MjksXCJiYXR0ZXJ5XCI6Mjh9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTA5IDIxOjI5XCIsXCJiaWtlXCI6MTU4NyxcImJhdHRlcnlcIjoyM30se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDggMDY6MzJcIixcImJpa2VcIjoxODcyLFwiYmF0dGVyeVwiOjYwfSx7XCJzdGF0aW9uXCI6XCLDmnZvelwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMTY6MTFcIixcImJpa2VcIjoxNjY5LFwiYmF0dGVyeVwiOjk2fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMTY6MjNcIixcImJpa2VcIjoxODg4LFwiYmF0dGVyeVwiOjE0fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wNiAxMTo1NVwiLFwiYmlrZVwiOjEzODcsXCJiYXR0ZXJ5XCI6ODB9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAwNjoxMlwiLFwiYmlrZVwiOjE3MzgsXCJiYXR0ZXJ5XCI6NTF9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDEgMjA6MDJcIixcImJpa2VcIjoxMzAwLFwiYmF0dGVyeVwiOjI5fSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDMgMTg6NTVcIixcImJpa2VcIjoxNzYwLFwiYmF0dGVyeVwiOjg2fSx7XCJzdGF0aW9uXCI6XCJOb3bDqSBzYWR5XCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxMDozMVwiLFwiYmlrZVwiOjE1MzksXCJiYXR0ZXJ5XCI6OTF9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTAyIDIyOjA1XCIsXCJiaWtlXCI6MTA3OCxcImJhdHRlcnlcIjo2MH0se1wic3RhdGlvblwiOlwiS29tw6Fyb3ZcIixcImF0XCI6XCIyMDI2LTEwLTIyIDA2OjA2XCIsXCJiaWtlXCI6MTI0NSxcImJhdHRlcnlcIjo2OX0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAwODo1NFwiLFwiYmlrZVwiOjE0NjgsXCJiYXR0ZXJ5XCI6NzB9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yOCAxNDo0NVwiLFwiYmlrZVwiOjE3NzUsXCJiYXR0ZXJ5XCI6ODJ9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAwOTozMFwiLFwiYmlrZVwiOjE3NjksXCJiYXR0ZXJ5XCI6OTZ9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAwNjoyMVwiLFwiYmlrZVwiOjE2NzUsXCJiYXR0ZXJ5XCI6N30se1wic3RhdGlvblwiOlwiTsOhbcSbc3TDrSBNw61ydVwiLFwiYXRcIjpcIjIwMjYtMTAtMTIgMDg6MjdcIixcImJpa2VcIjoxODUxLFwiYmF0dGVyeVwiOjYzfSx7XCJzdGF0aW9uXCI6XCJTdGFyw70gTMOtc2tvdmVjXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAxMTowMlwiLFwiYmlrZVwiOjE0ODIsXCJiYXR0ZXJ5XCI6OTZ9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMSAxMzowMVwiLFwiYmlrZVwiOjE1MzAsXCJiYXR0ZXJ5XCI6NDZ9LHtcInN0YXRpb25cIjpcIlZhxYhrb3ZrYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMTQ6MzhcIixcImJpa2VcIjoxNDM5LFwiYmF0dGVyeVwiOjUyfSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTAzIDExOjU0XCIsXCJiaWtlXCI6MTE2NixcImJhdHRlcnlcIjo5N30se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wOCAxMDoxMFwiLFwiYmlrZVwiOjE1MzMsXCJiYXR0ZXJ5XCI6OTJ9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTY6MDZcIixcImJpa2VcIjoxMjYwLFwiYmF0dGVyeVwiOjQ0fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDUgMDY6NTRcIixcImJpa2VcIjoxMTAxLFwiYmF0dGVyeVwiOjExfSx7XCJzdGF0aW9uXCI6XCJLb23DoXJvdlwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMjE6MzNcIixcImJpa2VcIjoxMTMzLFwiYmF0dGVyeVwiOjUwfSx7XCJzdGF0aW9uXCI6XCJWYcWIa292a2FcIixcImF0XCI6XCIyMDI2LTEwLTAyIDIxOjM4XCIsXCJiaWtlXCI6MTA5NyxcImJhdHRlcnlcIjo5M30se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0yMiAwODo0OVwiLFwiYmlrZVwiOjE2MzYsXCJiYXR0ZXJ5XCI6MTl9LHtcInN0YXRpb25cIjpcIk5vdsOpIHNhZHlcIixcImF0XCI6XCIyMDI2LTEwLTA1IDE4OjQ2XCIsXCJiaWtlXCI6MTA3MyxcImJhdHRlcnlcIjozOH0se1wic3RhdGlvblwiOlwiU3RhcsO9IEzDrXNrb3ZlY1wiLFwiYXRcIjpcIjIwMjYtMTAtMjMgMjE6MDBcIixcImJpa2VcIjoxMzE1LFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTA5IDE3OjEyXCIsXCJiaWtlXCI6MTIwMixcImJhdHRlcnlcIjo1N30se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMDY6MTJcIixcImJpa2VcIjoxMDY5LFwiYmF0dGVyeVwiOjYxfSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDQgMTY6NDFcIixcImJpa2VcIjoxNzMwLFwiYmF0dGVyeVwiOjUxfSx7XCJzdGF0aW9uXCI6XCJCeXN0cmMgcMWZw61zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAwNjo0NlwiLFwiYmlrZVwiOjE0NjAsXCJiYXR0ZXJ5XCI6NDB9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0wNyAxMDowOVwiLFwiYmlrZVwiOjE2MjUsXCJiYXR0ZXJ5XCI6OTB9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTI0IDE3OjU5XCIsXCJiaWtlXCI6MTY4MyxcImJhdHRlcnlcIjoxNn0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTE6MzJcIixcImJpa2VcIjoxMjA4LFwiYmF0dGVyeVwiOjYxfSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAxMjoyOFwiLFwiYmlrZVwiOjE3ODUsXCJiYXR0ZXJ5XCI6MzB9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAwNzo1M1wiLFwiYmlrZVwiOjExNDEsXCJiYXR0ZXJ5XCI6NjJ9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yNyAwOToxOFwiLFwiYmlrZVwiOjExODMsXCJiYXR0ZXJ5XCI6NTJ9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0wNSAyMjowNlwiLFwiYmlrZVwiOjEzMjcsXCJiYXR0ZXJ5XCI6OTB9LHtcInN0YXRpb25cIjpcIkhsYXZuw60gbsOhZHJhxb7DrVwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMDY6MjhcIixcImJpa2VcIjoxNjA3LFwiYmF0dGVyeVwiOjkwfSx7XCJzdGF0aW9uXCI6XCJLcsOhbG92byBQb2xlXCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAxODoxNFwiLFwiYmlrZVwiOjEzNjUsXCJiYXR0ZXJ5XCI6MTJ9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTIwIDA2OjMyXCIsXCJiaWtlXCI6MTcxNyxcImJhdHRlcnlcIjozOH0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xNyAxNzo0OFwiLFwiYmlrZVwiOjEyMTYsXCJiYXR0ZXJ5XCI6Mzd9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTIwIDE0OjIzXCIsXCJiaWtlXCI6MTQ4OSxcImJhdHRlcnlcIjo5Nn0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0wMSAwODoxMlwiLFwiYmlrZVwiOjExOTgsXCJiYXR0ZXJ5XCI6Mjl9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTE1IDE3OjI3XCIsXCJiaWtlXCI6MTI0NyxcImJhdHRlcnlcIjo3M30se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMTIgMDk6NDRcIixcImJpa2VcIjoxODMzLFwiYmF0dGVyeVwiOjIyfSx7XCJzdGF0aW9uXCI6XCJMdcW+w6Fua3lcIixcImF0XCI6XCIyMDI2LTEwLTIyIDIxOjUyXCIsXCJiaWtlXCI6MTk0NCxcImJhdHRlcnlcIjo3OX0se1wic3RhdGlvblwiOlwiw5p2b3pcIixcImF0XCI6XCIyMDI2LTEwLTA1IDIxOjI1XCIsXCJiaWtlXCI6MTAyOSxcImJhdHRlcnlcIjo3OH0se1wic3RhdGlvblwiOlwiS3LDoWxvdm8gUG9sZVwiLFwiYXRcIjpcIjIwMjYtMTAtMTggMDY6NTNcIixcImJpa2VcIjoxODc3LFwiYmF0dGVyeVwiOjE1fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMjggMTM6MDJcIixcImJpa2VcIjoxNTU3LFwiYmF0dGVyeVwiOjczfSx7XCJzdGF0aW9uXCI6XCJLb23DoXJvdlwiLFwiYXRcIjpcIjIwMjYtMTAtMjAgMTc6MzBcIixcImJpa2VcIjoxNTA1LFwiYmF0dGVyeVwiOjc4fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wOSAxNzozNlwiLFwiYmlrZVwiOjExNzksXCJiYXR0ZXJ5XCI6ODh9LHtcInN0YXRpb25cIjpcIsOadm96XCIsXCJhdFwiOlwiMjAyNi0xMC0yMiAyMTo1M1wiLFwiYmlrZVwiOjE0MjMsXCJiYXR0ZXJ5XCI6NTl9LHtcInN0YXRpb25cIjpcIsW9YWJvdsWZZXNreVwiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTY6MjJcIixcImJpa2VcIjoxNzUyLFwiYmF0dGVyeVwiOjI1fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTEwIDEyOjUzXCIsXCJiaWtlXCI6MTM0NCxcImJhdHRlcnlcIjo5MX0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxNjoxNFwiLFwiYmlrZVwiOjE5MzcsXCJiYXR0ZXJ5XCI6NzJ9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTAzIDEzOjI0XCIsXCJiaWtlXCI6MTQxMCxcImJhdHRlcnlcIjo4NH0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxMTo0M1wiLFwiYmlrZVwiOjEzMTcsXCJiYXR0ZXJ5XCI6Mzh9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAyMjowMlwiLFwiYmlrZVwiOjEwMTIsXCJiYXR0ZXJ5XCI6MzR9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0wNCAxMzo1NFwiLFwiYmlrZVwiOjE0NzIsXCJiYXR0ZXJ5XCI6Mzd9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yMyAyMjowMFwiLFwiYmlrZVwiOjE5NDksXCJiYXR0ZXJ5XCI6Nzl9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTAzIDE4OjA0XCIsXCJiaWtlXCI6MTUyNCxcImJhdHRlcnlcIjo2fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0xMiAxNToyNFwiLFwiYmlrZVwiOjE2NzMsXCJiYXR0ZXJ5XCI6NDB9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTEyIDE4OjA2XCIsXCJiaWtlXCI6MTIzMixcImJhdHRlcnlcIjoxMX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0yNSAwOToyMlwiLFwiYmlrZVwiOjE5NzIsXCJiYXR0ZXJ5XCI6ODV9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTExIDE2OjI5XCIsXCJiaWtlXCI6MTAxMixcImJhdHRlcnlcIjoyMn0se1wic3RhdGlvblwiOlwiTm92w6kgc2FkeVwiLFwiYXRcIjpcIjIwMjYtMTAtMTcgMDk6MTFcIixcImJpa2VcIjoxNDY2LFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJNb3JhdnNrw6kgbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMDMgMTQ6MzNcIixcImJpa2VcIjoxNjk4LFwiYmF0dGVyeVwiOjY4fSx7XCJzdGF0aW9uXCI6XCJIbGF2bsOtIG7DoWRyYcW+w61cIixcImF0XCI6XCIyMDI2LTEwLTI3IDIxOjA4XCIsXCJiaWtlXCI6MTI0NCxcImJhdHRlcnlcIjo1fSx7XCJzdGF0aW9uXCI6XCJNZW5kbG92byBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0yMSAxMzowOFwiLFwiYmlrZVwiOjEyNDgsXCJiYXR0ZXJ5XCI6NzZ9LHtcInN0YXRpb25cIjpcIk7DoW3Em3N0w60gTcOtcnVcIixcImF0XCI6XCIyMDI2LTEwLTIxIDEwOjIyXCIsXCJiaWtlXCI6MTA4NyxcImJhdHRlcnlcIjo0MX0se1wic3RhdGlvblwiOlwixb1hYm92xZllc2t5XCIsXCJhdFwiOlwiMjAyNi0xMC0yMCAyMToxN1wiLFwiYmlrZVwiOjE1NTIsXCJiYXR0ZXJ5XCI6MTR9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTI0IDE1OjUzXCIsXCJiaWtlXCI6MTg1NixcImJhdHRlcnlcIjo3MH0se1wic3RhdGlvblwiOlwiVsO9c3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMTAgMTg6NDRcIixcImJpa2VcIjoxMTM1LFwiYmF0dGVyeVwiOjI5fSx7XCJzdGF0aW9uXCI6XCLFvWFib3bFmWVza3lcIixcImF0XCI6XCIyMDI2LTEwLTI0IDIxOjM2XCIsXCJiaWtlXCI6MTM0NSxcImJhdHRlcnlcIjo2Mn0se1wic3RhdGlvblwiOlwiTHXFvsOhbmt5XCIsXCJhdFwiOlwiMjAyNi0xMC0xNiAwNjoxNVwiLFwiYmlrZVwiOjE3OTMsXCJiYXR0ZXJ5XCI6MzF9LHtcInN0YXRpb25cIjpcIktvbcOhcm92XCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAxNDozNlwiLFwiYmlrZVwiOjE5NTYsXCJiYXR0ZXJ5XCI6NTV9LHtcInN0YXRpb25cIjpcIktyw6Fsb3ZvIFBvbGVcIixcImF0XCI6XCIyMDI2LTEwLTAyIDE1OjE2XCIsXCJiaWtlXCI6MTQ5OCxcImJhdHRlcnlcIjo3NX0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjcgMTI6MjZcIixcImJpa2VcIjoxMzMxLFwiYmF0dGVyeVwiOjg3fSx7XCJzdGF0aW9uXCI6XCJWw71zdGF2acWhdMSbXCIsXCJhdFwiOlwiMjAyNi0xMC0xOCAwNjoxN1wiLFwiYmlrZVwiOjExNzMsXCJiYXR0ZXJ5XCI6ODh9LHtcInN0YXRpb25cIjpcIk1lbmRsb3ZvIG7DoW3Em3N0w61cIixcImF0XCI6XCIyMDI2LTEwLTAxIDE1OjU3XCIsXCJiaWtlXCI6MTg1NyxcImJhdHRlcnlcIjoyOX0se1wic3RhdGlvblwiOlwiS3JhdsOtIGhvcmFcIixcImF0XCI6XCIyMDI2LTEwLTI0IDA2OjU5XCIsXCJiaWtlXCI6MTU3MCxcImJhdHRlcnlcIjozOX0se1wic3RhdGlvblwiOlwiVmHFiGtvdmthXCIsXCJhdFwiOlwiMjAyNi0xMC0xMyAyMDoxM1wiLFwiYmlrZVwiOjEzNDEsXCJiYXR0ZXJ5XCI6MzZ9LHtcInN0YXRpb25cIjpcIk1vcmF2c2vDqSBuw6FtxJtzdMOtXCIsXCJhdFwiOlwiMjAyNi0xMC0wMyAwODo0M1wiLFwiYmlrZVwiOjE5NTksXCJiYXR0ZXJ5XCI6MTZ9LHtcInN0YXRpb25cIjpcIlN0YXLDvSBMw61za292ZWNcIixcImF0XCI6XCIyMDI2LTEwLTA3IDIyOjIwXCIsXCJiaWtlXCI6MTI0MyxcImJhdHRlcnlcIjo2N30se1wic3RhdGlvblwiOlwiQnlzdHJjIHDFmcOtc3RhdmnFoXTEm1wiLFwiYXRcIjpcIjIwMjYtMTAtMDggMTI6MzVcIixcImJpa2VcIjoxNjI5LFwiYmF0dGVyeVwiOjYwfSx7XCJzdGF0aW9uXCI6XCJOw6FtxJtzdMOtIE3DrXJ1XCIsXCJhdFwiOlwiMjAyNi0xMC0yNCAxMDoxMlwiLFwiYmlrZVwiOjE2NjUsXCJiYXR0ZXJ5XCI6NDl9LHtcInN0YXRpb25cIjpcIktyYXbDrSBob3JhXCIsXCJhdFwiOlwiMjAyNi0xMC0xNCAxOTo1NlwiLFwiYmlrZVwiOjE4MTQsXCJiYXR0ZXJ5XCI6MTR9LHtcInN0YXRpb25cIjpcIlbDvXN0YXZpxaF0xJtcIixcImF0XCI6XCIyMDI2LTEwLTEzIDIwOjIwXCIsXCJiaWtlXCI6MTE1MyxcImJhdHRlcnlcIjo3Nn0se1wic3RhdGlvblwiOlwiTWVuZGxvdm8gbsOhbcSbc3TDrVwiLFwiYXRcIjpcIjIwMjYtMTAtMjEgMTE6MzFcIixcImJpa2VcIjoxNzM5LFwiYmF0dGVyeVwiOjM3fSx7XCJzdGF0aW9uXCI6XCJLcmF2w60gaG9yYVwiLFwiYXRcIjpcIjIwMjYtMTAtMDkgMDg6MTVcIixcImJpa2VcIjoxNDc2LFwiYmF0dGVyeVwiOjk2fV19IiwiUmVjZWl2ZWRBdCI6IjIwMjYtMTAtMjAgMTE6MzM6NDIiLCJGYWN0cyI6Ilt7XCJhdFwiOlwiMjAyNi0xMC0xNFQyMjo1NjowM1pcIixcImJ5XCI6XCJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdFwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSBkZXBvdCBjb25maXJtZWQgYSBmbGF0IHR5cmUgZmF1bHQgb24gYmlrZSAxMDc3IGF0IE5vdsOpIHNhZHkuXCIsXCJ0eXBlXCI6XCJyZXF1ZXN0XCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2UyMmUwZGZlZjkzNmZhNTcyYTcyXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTI0VDE2OjU1OjU2WlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSBkZXBvdCBjb25maXJtZWQgYSBmbGF0IHR5cmUgZmF1bHQgb24gYmlrZSAxNTI1IGF0IEtvbcOhcm92LlwiLFwidHlwZVwiOlwicmVxdWVzdFwiLFwicXVvdGVcIjpcIlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV8zNWEzMjNjOTA5MjQzNDU2YTIyMlwifSx7XCJhdFwiOlwiMjAyNi0xMC0xMFQxMDoxNDowOFpcIixcImJ5XCI6XCJyaWRlclwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBsb2NrIGZhdWx0IG9uIGJpa2UgMTYwNiBhdCBLcsOhbG92byBQb2xlLlwiLFwidHlwZVwiOlwiY29tcGxhaW50XCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2YxM2IxZDYxZWNjOGE5Nzc5M2QwXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTIxVDA3OjA3OjE0WlwiLFwiYnlcIjpcImN1c3RvbWVyIGNhcmVcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDE5OTkgYXQgVsO9c3RhdmnFoXTEmy5cIixcInR5cGVcIjpcInByb21pc2VcIixcInF1b3RlXCI6XCJQxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfY2E4NmEwMjdlOWFkMzYyNWNlM2FcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTdUMTE6MjM6MjVaXCIsXCJieVwiOlwiY3VzdG9tZXIgY2FyZVwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTEwOCBhdCBLcsOhbG92byBQb2xlLlwiLFwidHlwZVwiOlwiY29tcGxhaW50XCIsXCJxdW90ZVwiOlwiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2Q2NmFiODc1OWE3Y2U1N2U3MWNhXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTE3VDA3OjI4OjIyWlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxNzE3IGF0IEhsYXZuw60gbsOhZHJhxb7DrS5cIixcInR5cGVcIjpcImluZm9ybWF0aW9uXCIsXCJxdW90ZVwiOlwiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2Q0ZTNhYjQ3NDkyOGQ0OTgxMDRiXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTExVDE0OjU5OjU0WlwiLFwiYnlcIjpcInJpZGVyXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHJpZGVyIHJlcG9ydGVkIGEgZGlzcGxheSBmYXVsdCBvbiBiaWtlIDE0NDIgYXQgQnlzdHJjIHDFmcOtc3RhdmnFoXTEmy5cIixcInR5cGVcIjpcImluZm9ybWF0aW9uXCIsXCJxdW90ZVwiOlwiTmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2RlY2I1OGMyZmQwZmUzOTM4MWJkXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTIwVDA5OjM0OjQyWlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTU1MyBhdCBLb23DoXJvdi5cIixcInR5cGVcIjpcImNvbXBsYWludFwiLFwicXVvdGVcIjpcIktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfODY0ZjUzZGI3NjE5MzRjNGM1YzFcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTFUMjE6MjY6NTZaXCIsXCJieVwiOlwib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3RcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDE0MTIgYXQgU3RhcsO9IEzDrXNrb3ZlYy5cIixcInR5cGVcIjpcInJlcXVlc3RcIixcInF1b3RlXCI6XCJQcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfNjA4MjQzMWFlMjVjM2ZmZTY4ZmRcIn0se1wiYXRcIjpcIjIwMjYtMTAtMjJUMTQ6MzE6MjNaXCIsXCJieVwiOlwic2VydmljZSB0ZWNobmljaWFuXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBiZWxsIGZhdWx0IG9uIGJpa2UgMTk0MiBhdCBLcsOhbG92byBQb2xlLlwiLFwidHlwZVwiOlwicHJvbWlzZVwiLFwicXVvdGVcIjpcIkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfZDA1NzAzMzhkNzFkNjdmODE4ODRcIn0se1wiYXRcIjpcIjIwMjYtMTAtMDhUMTk6Mzg6NDNaXCIsXCJieVwiOlwiY3VzdG9tZXIgY2FyZVwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBraWNrc3RhbmQgZmF1bHQgb24gYmlrZSAxNDQwIGF0IEJ5c3RyYyBwxZnDrXN0YXZpxaF0xJsuXCIsXCJ0eXBlXCI6XCJjb21wbGFpbnRcIixcInF1b3RlXCI6XCJExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2NjYmZhYWJmNmJmNjJlMmVkM2ZhXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTE3VDE3OjMzOjEyWlwiLFwiYnlcIjpcImN1c3RvbWVyIGNhcmVcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxNzk0IGF0IEtvbcOhcm92LlwiLFwidHlwZVwiOlwicHJvbWlzZVwiLFwicXVvdGVcIjpcIktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfY2I4YWU4NWVlMDBhOTcxODNiZjlcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTJUMjE6MjQ6MzRaXCIsXCJieVwiOlwib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3RcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiB0aGUgZGVwb3QgY29uZmlybWVkIGEgc2FkZGxlIGZhdWx0IG9uIGJpa2UgMTM4MCBhdCBLcmF2w60gaG9yYS5cIixcInR5cGVcIjpcInJlcXVlc3RcIixcInF1b3RlXCI6XCJaw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5X2Q2NmRkMDIxZTc2N2Y0ZjFjN2NhXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTEwVDA4OjUwOjQzWlwiLFwiYnlcIjpcInJpZGVyXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHJpZGVyIHJlcG9ydGVkIGEgbG9jayBmYXVsdCBvbiBiaWtlIDE2NDkgYXQgS29tw6Fyb3YuXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV9mOGU3ZDk3Yjc4ZDJjNGUxYjhkNlwifSx7XCJhdFwiOlwiMjAyNi0xMC0wMlQxMTo0MTo1OFpcIixcImJ5XCI6XCJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdFwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgYmVsbCBmYXVsdCBvbiBiaWtlIDE1NTcgYXQgTm92w6kgc2FkeS5cIixcInR5cGVcIjpcInByb21pc2VcIixcInF1b3RlXCI6XCJTZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV8zNGI2YjU5YzFhMDUxNTY1ODgwOFwifSx7XCJhdFwiOlwiMjAyNi0xMC0yNlQyMToxNzo1MlpcIixcImJ5XCI6XCJzZXJ2aWNlIHRlY2huaWNpYW5cIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiBjdXN0b21lciBjYXJlIHByb21pc2VkIGEgbGlnaHQgZmF1bHQgb24gYmlrZSAxNDQ1IGF0IEJ5c3RyYyBwxZnDrXN0YXZpxaF0xJsuXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfYTJkYTc1ZWVlMzI3MTYxNDI1NDRcIn0se1wiYXRcIjpcIjIwMjYtMTAtMTdUMDk6MjI6MzBaXCIsXCJieVwiOlwic2VydmljZSB0ZWNobmljaWFuXCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogY3VzdG9tZXIgY2FyZSBwcm9taXNlZCBhIGxvY2sgZmF1bHQgb24gYmlrZSAxMjM0IGF0IE5vdsOpIHNhZHkuXCIsXCJ0eXBlXCI6XCJyZXF1ZXN0XCIsXCJxdW90ZVwiOlwiU2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfZDVhYzFmYWVkYWNjNjkxZjlmOWFcIn0se1wiYXRcIjpcIjIwMjYtMTAtMjRUMTA6MjI6NDhaXCIsXCJieVwiOlwib3BlcmF0b3Igb2YgdGhlIEJybm8gZGVwb3RcIixcImZhY3RcIjpcIlRpY2tldCAxODc5OiB0aGUgdGVjaG5pY2lhbiBmb3VuZCBhIGRpc3BsYXkgZmF1bHQgb24gYmlrZSAxMjgyIGF0IEtyw6Fsb3ZvIFBvbGUuXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLlwiLFwic291cmNlXCI6XCJhY3Rpdml0eV9kMTMwNmIyN2I0ODcwYzFmMWQ0YVwifSx7XCJhdFwiOlwiMjAyNi0xMC0wMlQxNzoxNjoxMVpcIixcImJ5XCI6XCJvcGVyYXRvciBvZiB0aGUgQnJubyBkZXBvdFwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IGN1c3RvbWVyIGNhcmUgcHJvbWlzZWQgYSBzYWRkbGUgZmF1bHQgb24gYmlrZSAxODk0IGF0IE7DoW3Em3N0w60gTcOtcnUuXCIsXCJ0eXBlXCI6XCJwcm9taXNlXCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5Xzc5ZDc4M2FjMDAxMjVhYzFlZWFmXCJ9LHtcImF0XCI6XCIyMDI2LTEwLTI1VDEzOjEyOjU1WlwiLFwiYnlcIjpcInNlcnZpY2UgdGVjaG5pY2lhblwiLFwiZmFjdFwiOlwiVGlja2V0IDE4Nzk6IHRoZSB0ZWNobmljaWFuIGZvdW5kIGEgY2hhaW4gZmF1bHQgb24gYmlrZSAxMTg1IGF0IE7DoW3Em3N0w60gTcOtcnUuXCIsXCJ0eXBlXCI6XCJwcm9taXNlXCIsXCJxdW90ZVwiOlwiUHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5XzcwZWYzMTAyYjBlZDIxOTgzOTU0XCJ9LHtcImF0XCI6XCIyMDI2LTEwLTIzVDIxOjU4OjEyWlwiLFwiYnlcIjpcIm9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90XCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBjaGFpbiBmYXVsdCBvbiBiaWtlIDEzNzUgYXQgS3JhdsOtIGhvcmEuXCIsXCJ0eXBlXCI6XCJyZXF1ZXN0XCIsXCJxdW90ZVwiOlwiQmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuXCIsXCJzb3VyY2VcIjpcImFjdGl2aXR5Xzk0ZjI3MWY4YTE0ODBmMWZjM2Y3XCJ9LHtcImF0XCI6XCIyMDI2LTEwLTI0VDExOjEwOjI1WlwiLFwiYnlcIjpcIm9wZXJhdG9yIG9mIHRoZSBCcm5vIGRlcG90XCIsXCJmYWN0XCI6XCJUaWNrZXQgMTg3OTogdGhlIHRlY2huaWNpYW4gZm91bmQgYSBsaWdodCBmYXVsdCBvbiBiaWtlIDE3NjkgYXQgw5p2b3ouXCIsXCJ0eXBlXCI6XCJpbmZvcm1hdGlvblwiLFwicXVvdGVcIjpcIlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS5cIixcInNvdXJjZVwiOlwiYWN0aXZpdHlfNmUwMDJiOWMwYTUwYzQwMmUxYzhcIn1dIn0=') using utf8mb4);
set @n = convert(from_base64('eyJFeHRlcm5hbElkIjoiYWN0aXZpdHlfZjJjZDUzNDJiYjlhZTFkNTA2MTciLCJSZXBseUV4dGVybmFsSWQiOm51bGwsIlN0YXR1c0lkIjo0LCJMb2NrZWRVbnRpbCI6bnVsbCwiSW5jb21pbmdNZXNzYWdlVGV4dCI6IjxkaXYgbGFuZz1cImNzXCI+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPlDFmWVkbsOtIHN2xJt0bG8gbmVzdsOtdMOtLCB6YSB0bXkgc2UgbmVkw6EgamV0LjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5Qcm9zw61tIG8gdnLDoWNlbsOtIHBvcGxhdGt1IDQ5IEvEjSB6YSBuZWRva29uxI1lbm91IGrDrXpkdS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+UHJvc8OtbSBvIHZyw6FjZW7DrSBwb3BsYXRrdSA0OSBLxI0gemEgbmVkb2tvbsSNZW5vdSBqw616ZHUuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+S29sbyBuYSBzdGFuaWNpIEx1xb7DoW5reSBtw6EgcHJhc2tsb3UgcG5ldW1hdGlrdSwgcHJvc8OtbSBvIHbDvW3Em251LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5aw6FtZWsgc2UgbmVvZGVta2wgYW5pIG5hIHTFmWV0w60gcG9rdXMsIGrDrXpkYSBzZSBtaSBwxZllc3RvIMO6xI10b3ZhbGEuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5ExJtrdWppIHphIHJ5Y2hsw6kgdnnFmcOtemVuw60sIGtyZWRpdCBqc2VtIGRvc3RhbGEuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPk5hIHN0YW5pY2kgVmHFiGtvdmthIG5lYnlsbyDFvsOhZG7DqSB2b2xuw6kgbcOtc3RvLCBrb2xvIGpzZW0gbmVjaGFsIHZlZGxlLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlNlcnZpcyBzbMOtYmlsIG9wcmF2dSBkbyBww6F0a3UgMzAuIMWZw61qbmEuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5CYXRlcmllIHVrYXpvdmFsYSA4MCAlLCBwbyBkdm91IGtpbG9tZXRyZWNoIGJ5bGEgdnliaXTDoS48L3A+PHA+TmEgc3RhbmljaSBWYcWIa292a2EgbmVieWxvIMW+w6FkbsOpIHZvbG7DqSBtw61zdG8sIGtvbG8ganNlbSBuZWNoYWwgdmVkbGUuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+RMSba3VqaSB6YSByeWNobMOpIHZ5xZnDrXplbsOtLCBrcmVkaXQganNlbSBkb3N0YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5QxZllZG7DrSBzdsSbdGxvIG5lc3bDrXTDrSwgemEgdG15IHNlIG5lZMOhIGpldC48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxwPlrDoW1layBzZSBuZW9kZW1rbCBhbmkgbmEgdMWZZXTDrSBwb2t1cywgasOtemRhIHNlIG1pIHDFmWVzdG8gw7rEjXRvdmFsYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPlByb3PDrW0gbyB2csOhY2Vuw60gcG9wbGF0a3UgNDkgS8SNIHphIG5lZG9rb27EjWVub3UgasOtemR1LjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5TZXJ2aXMgc2zDrWJpbCBvcHJhdnUgZG8gcMOhdGt1IDMwLiDFmcOtam5hLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkJhdGVyaWUgdWthem92YWxhIDgwICUsIHBvIGR2b3Uga2lsb21ldHJlY2ggYnlsYSB2eWJpdMOhLjwvcD48cD5Lb2xvIG5hIHN0YW5pY2kgTHXFvsOhbmt5IG3DoSBwcmFza2xvdSBwbmV1bWF0aWt1LCBwcm9zw61tIG8gdsO9bcSbbnUuPC9wPjxwPkTEm2t1amkgemEgcnljaGzDqSB2ecWZw616ZW7DrSwga3JlZGl0IGpzZW0gZG9zdGFsYS48L3A+PHA+WsOhbWVrIHNlIG5lb2RlbWtsIGFuaSBuYSB0xZlldMOtIHBva3VzLCBqw616ZGEgc2UgbWkgcMWZZXN0byDDusSNdG92YWxhLjwvcD48cD5OYSBzdGFuaWNpIFZhxYhrb3ZrYSBuZWJ5bG8gxb7DoWRuw6kgdm9sbsOpIG3DrXN0bywga29sbyBqc2VtIG5lY2hhbCB2ZWRsZS48L3A+PHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+PHA+UMWZZWRuw60gc3bEm3RsbyBuZXN2w610w60sIHphIHRteSBzZSBuZWTDoSBqZXQuPC9wPjxwPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L3A+PHA+QmF0ZXJpZSB1a2F6b3ZhbGEgODAgJSwgcG8gZHZvdSBraWxvbWV0cmVjaCBieWxhIHZ5Yml0w6EuPC9wPjxibG9ja3F1b3RlPktvbG8gbmEgc3RhbmljaSBMdcW+w6Fua3kgbcOhIHByYXNrbG91IHBuZXVtYXRpa3UsIHByb3PDrW0gbyB2w71txJtudS48L2Jsb2NrcXVvdGU+PC9kaXY+IiwiU3VnZ2VzdGVkUmVwbHlUZXh0IjoiPHA+U2VydmlzIHNsw61iaWwgb3ByYXZ1IGRvIHDDoXRrdSAzMC4gxZnDrWpuYS48L3A+IiwiU2lnbmF0dXJlIjoiWsOha2F6bmlja8OhIHBvZHBvcmEgwrcgdGVsLjogMDM3MyA4MDYgNzAzIMK3IEUtbWFpbDogcG9kcG9yYUBleGFtcGxlLmNvbSJ9') using utf8mb4);
set @ticketId = (select max(id) + 1 from ticket);
set @noteId = (select max(id) + 1 from ticket_note);

insert into ticket (id, rider_id, city_id, subject, email, external_id, external_json, received_at, facts)
select @ticketId, json_value(@g, '$.RiderId'), json_value(@g, '$.CityId'), json_value(@g, '$.Subject'), json_value(@g, '$.Email'), json_value(@g, '$.ExternalId'), json_value(@g, '$.ExternalJsonData'), json_value(@g, '$.ReceivedAt'), json_value(@g, '$.Facts');

insert into ticket_note (id, ticket_id, external_id, status_id, incoming_text, suggested_text)
select @noteId, @ticketId, json_value(@n, '$.ExternalId'), json_value(@n, '$.StatusId'), json_value(@n, '$.IncomingMessageText'), json_value(@n, '$.SuggestedReplyText');

select @ticketId ticket_id, @noteId note_id; -- clone of test ticket 1879
```

_0 rows · 0.4 s_

## 11:32:51 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1546 | lock | 2026-10-14 |
| 1174 | flat tyre | 2026-10-01 |
| 1281 | battery | 2026-10-02 |
| 1408 | chain | 2026-10-26 |
| 1630 | display | 2026-10-20 |
| 1054 | battery | 2026-10-12 |
| 1845 | brake | 2026-10-11 |
| 1878 | bell | 2026-10-29 |
| 1746 | bell | 2026-10-17 |
| 1592 | chain | 2026-10-09 |
| 1203 | brake | 2026-10-07 |
| 1903 | light | 2026-10-22 |
| 1805 | lock | 2026-10-05 |
| 1518 | brake | 2026-10-08 |
| 1421 | kickstand | 2026-10-12 |
| 1032 | chain | 2026-10-27 |
| 1221 | display | 2026-10-12 |
| 1240 | lock | 2026-10-13 |
| 1884 | display | 2026-10-15 |
| 1788 | bell | 2026-10-16 |
| 1582 | brake | 2026-10-04 |
| 1927 | light | 2026-10-29 |
| 1149 | bell | 2026-10-19 |
| 1144 | battery | 2026-10-20 |
| 1634 | battery | 2026-10-06 |
| 1058 | kickstand | 2026-10-29 |
| 1968 | display | 2026-10-03 |
| 1830 | brake | 2026-10-04 |
| 1293 | light | 2026-10-11 |
| 1425 | saddle | 2026-10-20 |
| 1854 | display | 2026-10-28 |
| 1162 | kickstand | 2026-10-26 |
| 1640 | saddle | 2026-10-06 |
| 1047 | bell | 2026-10-03 |
| 1677 | bell | 2026-10-01 |
| 1484 | saddle | 2026-10-11 |
| 1932 | kickstand | 2026-10-03 |
| 1609 | light | 2026-10-01 |
| 1821 | lock | 2026-10-07 |
| 1508 | saddle | 2026-10-21 |
| 1988 | bell | 2026-10-15 |
| 1797 | saddle | 2026-10-08 |
| 1328 | bell | 2026-10-06 |
| 1032 | battery | 2026-10-26 |
| 1076 | flat tyre | 2026-10-10 |
| 1056 | light | 2026-10-07 |
| 1502 | flat tyre | 2026-10-06 |
| 1061 | lock | 2026-10-21 |
| 1721 | chain | 2026-10-09 |
| 1519 | brake | 2026-10-08 |
| 1553 | kickstand | 2026-10-12 |
| 1419 | light | 2026-10-24 |
| 1902 | battery | 2026-10-18 |
| 1949 | brake | 2026-10-30 |
| 1095 | display | 2026-10-07 |
| 1722 | lock | 2026-10-06 |
| 1345 | light | 2026-10-15 |
| 1146 | chain | 2026-10-07 |
| 1329 | battery | 2026-10-20 |

_59 rows · 0.8 s_

## 11:35:58 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 204893 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/2570?tab=history"},{"type":"string","title":"Searched","value":"ride 115257: 1 found"},{"type":"multiline","title":"Ticket… |
| 207833 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/4297?tab=history"},{"type":"string","title":"Searched","value":"ride 103561: 1 found"},{"type":"multiline","title":"Ticket… |
| 206511 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/4800?tab=history"},{"type":"string","title":"Searched","value":"ride 105293: 1 found"},{"type":"multiline","title":"Ticket… |

_3 rows · 2.3 s_

## 11:36:54 · bikes-test / bikeshare_test (read-only) · select id, meta from station where meta is not null limit 5

```sql
select id, meta from station where meta is not null limit 5
```

| id | meta |
|---|---|
| 104 | {"station":"Mendlovo náměstí","docks":21,"lat":49.19118,"lon":16.61032,"notes":"Kolo na stanici Lužánky má prasklou pneumatiku, prosím o výměnu.","contacts":["Klára Veselá","Ondřej Marek"]} |
| 55 | {"station":"Úvoz","docks":17,"lat":49.21441,"lon":16.64884,"notes":"Zámek se neodemkl ani na třetí pokus, jízda se mi přesto účtovala.","contacts":["Tomáš Král","Jana Dvořáková"]} |
| 47 | {"station":"Mendlovo náměstí","docks":15,"lat":49.21655,"lon":16.6034,"notes":"Děkuji za rychlé vyřízení, kredit jsem dostala.","contacts":["Eva Horáková","Jakub Fiala"]} |
| 113 | {"station":"Královo Pole","docks":19,"lat":49.21565,"lon":16.64212,"notes":"Prosím o vrácení poplatku 49 Kč za nedokončenou jízdu.","contacts":["Jakub Fiala","Martin Procházka"]} |

_4 rows · 0.6 s_

## 11:39:01 · bikes-localhost / bikeshare (read-write) · local tickets with facts

```sql
select count(*) from ticket_note where facts is not null
```

| count(*) |
|---|
| 22 |

_1 rows · 1.5 s_

## 11:41:55 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1410 | lock | 2026-10-15 |
| 1769 | light | 2026-10-06 |
| 1318 | flat tyre | 2026-10-17 |
| 1224 | kickstand | 2026-10-10 |
| 1118 | flat tyre | 2026-10-01 |
| 1681 | brake | 2026-10-01 |
| 1093 | battery | 2026-10-30 |
| 1392 | light | 2026-10-11 |
| 1890 | battery | 2026-10-12 |
| 1179 | saddle | 2026-10-19 |
| 1975 | battery | 2026-10-09 |
| 1725 | light | 2026-10-03 |
| 1719 | lock | 2026-10-06 |
| 1978 | chain | 2026-10-18 |
| 1259 | saddle | 2026-10-18 |
| 1079 | bell | 2026-10-05 |
| 1363 | battery | 2026-10-19 |
| 1164 | chain | 2026-10-25 |
| 1761 | kickstand | 2026-10-18 |
| 1175 | bell | 2026-10-06 |
| 1153 | battery | 2026-10-07 |
| 1424 | kickstand | 2026-10-06 |
| 1572 | light | 2026-10-08 |
| 1436 | lock | 2026-10-02 |
| 1131 | brake | 2026-10-02 |
| 1297 | bell | 2026-10-27 |
| 1810 | light | 2026-10-18 |
| 1360 | bell | 2026-10-29 |
| 1698 | display | 2026-10-20 |
| 1237 | brake | 2026-10-15 |
| 1004 | display | 2026-10-16 |
| 1887 | light | 2026-10-16 |
| 1200 | bell | 2026-10-28 |
| 1811 | lock | 2026-10-18 |
| 1194 | battery | 2026-10-24 |
| 1297 | chain | 2026-10-13 |
| 1614 | battery | 2026-10-16 |
| 1056 | display | 2026-10-02 |
| 1388 | flat tyre | 2026-10-23 |
| 1063 | saddle | 2026-10-25 |
| 1205 | saddle | 2026-10-21 |
| 1599 | flat tyre | 2026-10-30 |
| 1888 | light | 2026-10-17 |
| 1784 | chain | 2026-10-14 |
| 1567 | brake | 2026-10-11 |
| 1759 | kickstand | 2026-10-09 |
| 1267 | flat tyre | 2026-10-26 |
| 1572 | display | 2026-10-26 |
| 1977 | flat tyre | 2026-10-10 |
| 1817 | bell | 2026-10-24 |
| 1091 | display | 2026-10-15 |

_51 rows · 1.1 s_

## 11:47:59 · bikes-localhost / bikeshare (WRITE) · point the first local fact at a note in ticket 451

```sql
update ticket set facts = json_set(facts, '$[0].source', 'activity_' || '62939ea333df3c6d3652') where id = 451;
```

_0 rows · 2.6 s_

## 11:51:39 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 208500 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/2048?tab=history"},{"type":"string","title":"Searched","value":"ride 167251: 1 found"},{"type":"multiline","title":"Ticket… |

_1 rows · 1.0 s_

## 11:54:09 · bikes-prod / bikeshare_prod (read-only) · rides by hour of day

```sql
select hour(started_at) h, count(*) n from ride where started_at >= '2026-10-01' group by h order by h
```

| h | n |
|---|---|
| 0 | 2107 |
| 1 | 1586 |
| 2 | 3299 |
| 3 | 2663 |
| 4 | 3152 |
| 5 | 202 |
| 6 | 984 |
| 7 | 3118 |
| 8 | 2766 |
| 9 | 2588 |
| 10 | 2221 |
| 11 | 2447 |
| 12 | 973 |
| 13 | 3828 |
| 14 | 2313 |
| 15 | 830 |
| 16 | 86 |
| 17 | 3741 |
| 18 | 2867 |
| 19 | 2027 |
| 20 | 1773 |
| 21 | 1101 |
| 22 | 2658 |
| 23 | 1436 |

_24 rows · 1.6 s_

## 11:56:20 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1411 | light | 2026-10-14 |
| 1742 | display | 2026-10-30 |
| 1985 | kickstand | 2026-10-16 |
| 1396 | kickstand | 2026-10-20 |
| 1654 | brake | 2026-10-29 |
| 1540 | brake | 2026-10-10 |
| 1585 | chain | 2026-10-23 |
| 1118 | display | 2026-10-19 |
| 1709 | lock | 2026-10-29 |
| 1955 | bell | 2026-10-12 |
| 1432 | light | 2026-10-23 |
| 1813 | bell | 2026-10-24 |
| 1563 | kickstand | 2026-10-17 |
| 1161 | lock | 2026-10-22 |
| 1713 | kickstand | 2026-10-05 |
| 1612 | battery | 2026-10-07 |
| 1123 | saddle | 2026-10-26 |
| 1980 | light | 2026-10-01 |
| 1901 | kickstand | 2026-10-26 |
| 1716 | lock | 2026-10-02 |
| 1029 | brake | 2026-10-27 |
| 1163 | light | 2026-10-14 |
| 1751 | kickstand | 2026-10-07 |
| 1523 | lock | 2026-10-30 |
| 1445 | chain | 2026-10-05 |
| 1678 | display | 2026-10-29 |
| 1556 | light | 2026-10-09 |
| 1418 | saddle | 2026-10-19 |
| 1680 | brake | 2026-10-13 |
| 1574 | chain | 2026-10-28 |
| 1225 | flat tyre | 2026-10-18 |
| 1135 | saddle | 2026-10-07 |
| 1528 | kickstand | 2026-10-18 |
| 1239 | brake | 2026-10-21 |
| 1687 | flat tyre | 2026-10-08 |
| 1268 | bell | 2026-10-01 |
| 1458 | kickstand | 2026-10-24 |
| 1225 | saddle | 2026-10-20 |
| 1328 | flat tyre | 2026-10-13 |
| 1850 | battery | 2026-10-23 |
| 1639 | light | 2026-10-30 |
| 1002 | display | 2026-10-23 |
| 1527 | brake | 2026-10-12 |
| 1052 | display | 2026-10-24 |

_44 rows · 0.4 s_

## 11:57:53 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1397 | light | 2026-10-24 |
| 1789 | bell | 2026-10-22 |
| 1421 | brake | 2026-10-23 |
| 1105 | chain | 2026-10-21 |
| 1479 | saddle | 2026-10-18 |
| 1490 | chain | 2026-10-30 |
| 1837 | kickstand | 2026-10-10 |
| 1970 | battery | 2026-10-14 |
| 1175 | bell | 2026-10-23 |
| 1402 | display | 2026-10-29 |
| 1245 | kickstand | 2026-10-22 |
| 1521 | saddle | 2026-10-10 |
| 1440 | lock | 2026-10-07 |
| 1874 | light | 2026-10-20 |
| 1590 | chain | 2026-10-23 |
| 1105 | display | 2026-10-24 |
| 1272 | battery | 2026-10-11 |
| 1751 | flat tyre | 2026-10-25 |
| 1288 | display | 2026-10-30 |
| 1299 | chain | 2026-10-06 |
| 1890 | display | 2026-10-24 |
| 1248 | flat tyre | 2026-10-02 |
| 1363 | battery | 2026-10-02 |
| 1073 | light | 2026-10-14 |
| 1945 | saddle | 2026-10-08 |
| 1964 | brake | 2026-10-09 |
| 1662 | kickstand | 2026-10-15 |
| 1865 | brake | 2026-10-11 |
| 1873 | display | 2026-10-11 |
| 1958 | display | 2026-10-29 |
| 1346 | light | 2026-10-21 |
| 1839 | battery | 2026-10-07 |
| 1214 | saddle | 2026-10-26 |
| 1924 | flat tyre | 2026-10-13 |
| 1639 | brake | 2026-10-20 |
| 1312 | bell | 2026-10-25 |
| 1204 | display | 2026-10-07 |
| 1113 | lock | 2026-10-10 |
| 1221 | lock | 2026-10-10 |
| 1794 | light | 2026-10-22 |
| 1980 | flat tyre | 2026-10-24 |
| 1578 | bell | 2026-10-02 |
| 1620 | lock | 2026-10-14 |
| 1288 | saddle | 2026-10-05 |
| 1752 | bell | 2026-10-25 |
| 1954 | flat tyre | 2026-10-02 |
| 1864 | kickstand | 2026-10-19 |
| 1788 | battery | 2026-10-23 |
| 1249 | light | 2026-10-28 |
| 1519 | kickstand | 2026-10-02 |
| 1887 | display | 2026-10-18 |
| 1395 | flat tyre | 2026-10-06 |
| 1851 | display | 2026-10-30 |
| 1373 | kickstand | 2026-10-24 |
| 1399 | brake | 2026-10-10 |
| 1195 | light | 2026-10-12 |
| 1054 | bell | 2026-10-28 |
| 1682 | saddle | 2026-10-22 |
| 1476 | display | 2026-10-28 |
| 1200 | display | 2026-10-10 |
| 1561 | chain | 2026-10-22 |
| 1313 | bell | 2026-10-23 |
| 1776 | saddle | 2026-10-07 |
| 1885 | flat tyre | 2026-10-07 |

_64 rows · 1.7 s_

## 12:02:17 · bikes-prod / bikeshare_prod (read-only) · free docks per station

```sql
select s.name, count(*) free_docks
from dock d join station s on s.id = d.station_id
where d.bike_id is null group by s.name order by free_docks desc
```

| name | free_docks |
|---|---|
| Náměstí Míru | 14 |
| Hlavní nádraží | 7 |
| Výstaviště | 11 |
| Mendlovo náměstí | 12 |
| Lužánky | 4 |
| Královo Pole | 2 |
| Žabovřesky | 6 |
| Komárov | 2 |
| Starý Lískovec | 1 |
| Bystrc přístaviště | 24 |
| Kraví hora | 20 |
| Vaňkovka | 20 |
| Úvoz | 8 |
| Moravské náměstí | 8 |
| Nové sady | 16 |

_15 rows · 1.3 s_

## 12:03:01 · bikes-test / bikeshare_test (read-only) · open faults on test, oldest first

```sql
select bike_id, fault, reported_on from fault where closed_on is null order by reported_on
```

| bike_id | fault | reported_on |
|---|---|---|
| 1400 | lock | 2026-10-15 |
| 1055 | light | 2026-10-27 |
| 1204 | light | 2026-10-30 |
| 1694 | kickstand | 2026-10-28 |
| 1053 | flat tyre | 2026-10-27 |
| 1818 | kickstand | 2026-10-22 |
| 1002 | lock | 2026-10-17 |
| 1219 | chain | 2026-10-03 |
| 1134 | light | 2026-10-02 |
| 1947 | saddle | 2026-10-19 |
| 1472 | brake | 2026-10-22 |
| 1735 | brake | 2026-10-09 |
| 1594 | chain | 2026-10-15 |
| 1203 | light | 2026-10-30 |
| 1481 | lock | 2026-10-10 |
| 1191 | lock | 2026-10-30 |
| 1582 | brake | 2026-10-01 |
| 1988 | saddle | 2026-10-18 |
| 1418 | lock | 2026-10-07 |
| 1487 | lock | 2026-10-03 |
| 1760 | brake | 2026-10-18 |
| 1365 | chain | 2026-10-06 |
| 1041 | saddle | 2026-10-01 |
| 1282 | saddle | 2026-10-17 |
| 1439 | brake | 2026-10-28 |
| 1769 | kickstand | 2026-10-07 |
| 1273 | battery | 2026-10-25 |
| 1277 | brake | 2026-10-19 |
| 1197 | display | 2026-10-07 |
| 1041 | saddle | 2026-10-22 |
| 1567 | display | 2026-10-15 |
| 1907 | brake | 2026-10-12 |
| 1466 | saddle | 2026-10-01 |
| 1373 | display | 2026-10-07 |
| 1147 | kickstand | 2026-10-30 |
| 1084 | flat tyre | 2026-10-24 |
| 1567 | light | 2026-10-08 |
| 1461 | bell | 2026-10-01 |
| 1536 | battery | 2026-10-15 |
| 1901 | display | 2026-10-30 |
| 1891 | kickstand | 2026-10-19 |

_41 rows · 0.5 s_

## 12:06:50 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 205217 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/2659?tab=history"},{"type":"string","title":"Searched","value":"ride 147075: 1 found"},{"type":"multiline","title":"Ticket… |
| 201514 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/8770?tab=history"},{"type":"string","title":"Searched","value":"ride 169434: 1 found"},{"type":"multiline","title":"Ticket… |

_2 rows · 0.5 s_

## 12:08:30 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Tomáš Král | student |
| Zuzana Pokorná | company |
| Martin Procházka | company |
| Petr Novotný | senior |
| Zuzana Pokorná | company |
| Petr Novotný | senior |
| Ondřej Marek | student |
| Petr Novotný | student |
| Jakub Fiala | student |

_9 rows · 2.2 s_

## 12:09:30 · bikes-localhost / bikeshare (read-write) · local tickets with facts

```sql
select count(*) from ticket_note where facts is not null
```

| count(*) |
|---|
| 6 |

_1 rows · 2.1 s_

## 12:15:07 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 204506 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/9823?tab=history"},{"type":"string","title":"Searched","value":"ride 127396: 1 found"},{"type":"multiline","title":"Ticket… |

_1 rows · 2.3 s_

## 12:18:07 · bikes-prod / bikeshare_prod (read-only) · rides by hour of day

```sql
select hour(started_at) h, count(*) n from ride where started_at >= '2026-10-01' group by h order by h
```

| h | n |
|---|---|
| 0 | 2053 |
| 1 | 548 |
| 2 | 2245 |
| 3 | 3391 |
| 4 | 335 |
| 5 | 3329 |
| 6 | 1092 |
| 7 | 3958 |
| 8 | 3252 |
| 9 | 1858 |
| 10 | 1532 |
| 11 | 1527 |
| 12 | 639 |
| 13 | 2749 |
| 14 | 3855 |
| 15 | 2904 |
| 16 | 3896 |
| 17 | 3926 |
| 18 | 2382 |
| 19 | 2870 |
| 20 | 950 |
| 21 | 665 |
| 22 | 1939 |
| 23 | 1905 |

_24 rows · 2.6 s_

## 12:24:26 · bikes-prod / bikeshare_prod (read-only) · riders with a tier

```sql
select name, tier from rider where tier is not null order by tier
```

| name | tier |
|---|---|
| Klára Veselá | senior |
| Klára Veselá | student |
| Tomáš Král | senior |
| Ondřej Marek | student |
| Ondřej Marek | company |
| Eva Horáková | company |
| Jakub Fiala | senior |
| Klára Veselá | company |
| Jana Dvořáková | senior |
| Martin Procházka | company |
| Eva Horáková | student |
| Lucie Benešová | company |

_12 rows · 2.4 s_

## 12:27:21 · bikes-localhost / bikeshare (read-write) · select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) …

```sql
select id, left(json_extract(data,'$.customFields'),600) c from ticket_note where ticket_id = (select max(id) from ticket)
```

| id | c |
|---|---|
| 206981 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/1426?tab=history"},{"type":"string","title":"Searched","value":"ride 197798: 1 found"},{"type":"multiline","title":"Ticket… |
| 205480 | [{"type":"url","title":"Result","value":"https://dispatch.example.com/tickets/6754?tab=history"},{"type":"string","title":"Searched","value":"ride 192981: 1 found"},{"type":"multiline","title":"Ticket… |

_2 rows · 0.3 s_
