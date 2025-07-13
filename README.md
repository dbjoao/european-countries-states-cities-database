# European-countries-states-cities-database
Database containing every European Country, State, City and territories <br>
Containing 77,747 registries: 53 Countries, 1884 States & 75810 Cities

```sql
CREATE TABLE `cities` (
  `id` mediumint(8) UNSIGNED NOT NULL,
  `name` varchar(255) NOT NULL,
  `state_id` mediumint(8) UNSIGNED NOT NULL,
  `state_code` varchar(255) NOT NULL,
  `country_id` mediumint(8) UNSIGNED NOT NULL,
  `country_code` char(2) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci ROW_FORMAT=COMPACT;


CREATE TABLE `countries` (
  `id` mediumint(8) UNSIGNED NOT NULL,
  `name` varchar(100) NOT NULL,
  `iso3` char(3) DEFAULT NULL,
  `numeric_code` char(3) DEFAULT NULL,
  `iso2` char(2) DEFAULT NULL,
  `region` varchar(255) DEFAULT NULL,
  `region_id` mediumint(8) UNSIGNED DEFAULT NULL,
  `subregion` varchar(255) DEFAULT NULL,
  `subregion_id` mediumint(8) UNSIGNED DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

CREATE TABLE `states` (
  `id` mediumint(8) UNSIGNED NOT NULL,
  `name` varchar(255) NOT NULL,
  `country_id` mediumint(8) UNSIGNED NOT NULL,
  `country_code` char(2) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci ROW_FORMAT=COMPACT;
```

```sql
INSERT INTO `cities` (`id`, `name`, `state_id`, `state_code`, `country_id`, `country_code`) VALUES
(1, 'Andorra la Vella', 488, '07', 6, 'AD'),
(2, 'Arinsal', 493, '04', 6, 'AD'),
(3, 'Canillo', 489, '02', 6, 'AD'),
(4, 'El Tarter', 489, '02', 6, 'AD'),
(5, 'Encamp', 487, '03', 6, 'AD'),
(6, 'Ordino', 491, '05', 6, 'AD'),
(7, 'Pas de la Casa', 487, '03', 6, 'AD'),
(8, 'Sant Julià de Lòria', 490, '06', 6, 'AD'),
(9, 'la Massana', 493, '04', 6, 'AD'),
(10, 'les Escaldes', 492, '08', 6, 'AD'),
(151, 'Bajram Curri', 623, 'KU', 3, 'AL'),
--- etcetera.....
```
