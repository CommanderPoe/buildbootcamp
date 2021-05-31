### Bitcoin Price History.
---

Will work with bitcoin price history, manipulating data from coinmarket cap.

Check `prices.py` for this lesson
<br>

#### Writing a dict into a csv

> `import csv`
> `f= open('foo.csv', 'w')`
> `writer= csv.DictWriter(f, ['high', 'low'])`
> `writer.writeheader()`
> `writer.writerow({'high': 100, 'low': 45})`
> `f.close()`