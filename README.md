# Search-beacon-trafic-squid for Investigations
Search for beacon traffic in squid access.log files

**beacon request** обычно относится к записи события, когда устройство (например, мобильное приложение) пытается подключиться к серверу


```bash
sec504@slingshot:~/labs/falsimentis$ ./findbeacons.py -i 5 -c 10 172.16.42.107 access.log 
Sites that had at least 10 5-second intervals
  193 - https://push.services.mozilla.com/
   11 - 172.217.11.162:443
   43 - https://px.moatads.com/pixel.gif?
   12 - 216.58.217.194:443
   20 - 172.217.5.194:443
   11 - https://t.wayfair.com/b.php?
   11 - https://att-app.quantummetric.com/?
   10 - https://a.espncdn.com/combiner/i?
 3268 - http://www1-google-analytics.com/collect
   28 - https://start.specless.tech/report/1
   11 - https://apx.moatads.com/pixel.gif?
```
`-i 5` - look for beacons that are at 5-second intervals <br>
`-c 10` - look for a minimum of 10 beacons
