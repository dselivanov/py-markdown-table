# markdownTable

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/hvalev/markdownTable/test?label=test)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/hvalev/markdownTable/deploy?label=deploy)
[![codecov](https://codecov.io/gh/hvalev/markdownTable/branch/main/graph/badge.svg?token=ZZ8WXO4H6P)](https://codecov.io/gh/hvalev/markdownTable)
[![HitCount](http://hits.dwyl.com/hvalev/markdownTable.svg)](http://hits.dwyl.com/hvalev/markdownTable)

A class used to generate padded tables in a markdown code block 

# Installation
You can install it via pip with the following command 
```pip3 install py-markdown-table```
and consequently import it via
```from markdownTable import markdownTable```

# Examples

```markdownTable(data)..setParams(row_sep = 'always').getMarkdown()```
```
+----------------------------------------+
|    title   |    time   |   date  |seats|
+------------+-----------+---------+-----+
|Vrij Zwemmen|21:30-23:00|Wed 09.12|24/24|
+------------+-----------+---------+-----+
|Vrij Zwemmen|12:00-13:00|Thu 10.12|18/18|
+------------+-----------+---------+-----+
|Vrij zwemmen| 7:30-8:30 |Fri 11.12|18/18|
+------------+-----------+---------+-----+
|Vrij Zwemmen|13:15-14:15|Sat 12.12|18/18|
+----------------------------------------+
```

```markdownTable(data).setParams(row_sep = 'topbottom').getMarkdown()```
```
+----------------------------------------+
|    title   |    time   |   date  |seats|
|Vrij Zwemmen|21:30-23:00|Wed 09.12|24/24|
|Vrij Zwemmen|12:00-13:00|Thu 10.12|18/18|
|Vrij zwemmen| 7:30-8:30 |Fri 11.12|18/18|
|Vrij Zwemmen|13:15-14:15|Sat 12.12|18/18|
+----------------------------------------+
```

```markdownTable(data).setParams(row_sep = 'topbottom', padding_width = 5, padding_weight='left').getMarkdown()```
```
+------------------------------------------------------------+
|            title|            time|          date|     seats|
|     Vrij Zwemmen|     21:30-23:00|     Wed 09.12|     24/24|
|     Vrij Zwemmen|     12:00-13:00|     Thu 10.12|     18/18|
|     Vrij zwemmen|       7:30-8:30|     Fri 11.12|     18/18|
|     Vrij Zwemmen|     13:15-14:15|     Sat 12.12|     18/18|
+------------------------------------------------------------+
```

```markdownTable(data).setParams(row_sep = 'topbottom', padding_width = 5, padding_weight = 'centerright').getMarkdown()```
```
+------------------------------------------------------------+
|      title      |      time      |     date     |  seats   |
|  Vrij Zwemmen   |  21:30-23:00   |  Wed 09.12   |  24/24   |
|  Vrij Zwemmen   |  12:00-13:00   |  Thu 10.12   |  18/18   |
|  Vrij zwemmen   |   7:30-8:30    |  Fri 11.12   |  18/18   |
|  Vrij Zwemmen   |  13:15-14:15   |  Sat 12.12   |  18/18   |
+------------------------------------------------------------+
```

```mt = markdownTable(data).setParams(row_sep = 'always', padding_width = 5, padding_weight='centerright', padding_char = '.').getMarkdown()```
```
+------------------------------------------------------------+
|......title......|......time......|.....date.....|..seats...|
+-----------------+----------------+--------------+----------+
|..Vrij Zwemmen...|..21:30-23:00...|..Wed 09.12...|..24/24...|
+-----------------+----------------+--------------+----------+
|..Vrij Zwemmen...|..12:00-13:00...|..Thu 10.12...|..18/18...|
+-----------------+----------------+--------------+----------+
|..Vrij zwemmen...|...7:30-8:30....|..Fri 11.12...|..18/18...|
+-----------------+----------------+--------------+----------+
|..Vrij Zwemmen...|..13:15-14:15...|..Sat 12.12...|..18/18...|
+------------------------------------------------------------+
```
