---
date: 2017-11-19 22:13:00

title: python使用爬虫获取json格式的网页，输出以及写入文件乱码
tags: scarpy
categories: python
---

解决python使用爬虫获取json格式的网页，输出以及写入文件乱码的情况

```
import codecs

resp = requests.get(url,headers=headers)
result = json.dumps(resp.json(),ensure_ascii=False)
#若不指定ensure_ascii=False，输出的是中文的ascii 字符码，而不是真正的中文。
#这是因为json.dumps 序列化时对中文默认使用的ascii编码.想输出真正的中文需要指定ensure_ascii=False：

file1 = codecs.open(date+"liujiqian.txt",'a','utf-8')	
#将获取到的内容写到文件，以指定的编码方式打开文件，这样才能正常写入中文
file1.write(result)
file1.close()

```
