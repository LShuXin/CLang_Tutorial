Unix时间戳

.Unix时间戳（英文为Unix epoch, Unix time, POSIX time 或 Unix timestamp）是从1970年1月1日（UTC/GMT的午夜）开始所经过的`秒数`，不考虑闰秒。

UNIX时间戳的0按照ISO 8601规范为 ：`1970-01-01T00:00:00Z.`
一个小时表示为UNIX时间戳格式为：3600秒；一天表示为UNIX时间戳为86400秒，闰秒不计算。
在大多数的UNIX系统中UNIX时间戳存储为32位，这样会引发2038年问题或Y2038。