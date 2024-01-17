```
#pd.merge(temp_1, table, left_on='id', right_on='id', how='inner')
'''
SELECT *
FROM temp_1
INNER JOIN table ON temp_1.id = table.id
'''
```

```
#data[data['name'].str.contains('String')]
'''
SELECT *
FROM data
WHERE name LIKE '%String%'
'''
```

```
#data[(data['name'] == 'A') | (data['name'] == 'B')][['name', 'period_start', 'period_end', 'participants']]
'''
SELECT name, period_start, period_end, participants
FROM data
WHERE name = 'A' 
   OR name = 'B'
'''
```

```
#table[table['period_start'] >= pd.to_datetime('2022-12-10 00:00:00', format='%Y-%m-%d %H:%M:%S')]
'''
SELECT *
FROM table
WHERE period_start >= '2022-12-10 00:00:00'
'''
```

```
#table1[table1['content_id'].isin(table2['talk_id'])]
'''
SELECT table1.*
FROM table1
INNER JOIN table2 ON table1.content_id = table2.talk_id
'''
```

```
#len(table[(
#    (table['c_time'] >= pd.to_datetime('2023-01-01 00:00:00', format='%Y-%m-%d %H:%M:%S')) &
#    (table['c_time'] <= pd.to_datetime('2023-01-31 00:00:00', format='%Y-%m-%d %H:%M:%S'))
#)])
'''
SELECT COUNT(*)
FROM table
WHERE c_time >= '2023-01-01 00:00:00' AND c_time <= '2023-01-31 00:00:00'
'''
```
