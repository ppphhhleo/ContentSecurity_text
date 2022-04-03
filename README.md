# ContentSecurity_text
基于Word2Vec文本分类，THUNews；博文内容审核。

## 文件目录
* data - 七个类别新闻，各自200条
* result - 七个类别新闻的分词结果；  
    * all.txt - 所有语料的分词整合
    * all_model.model - 所有语料训练的词向量模型
* posts - 爬取微博博文
    * results.csv / json 内容审核结果
* **Weibo-search** 微博爬虫，可设置关键词，需要登录获取[微博](https://weibo.com/) 的cookie 
* 7000data.csv - THUNews 同样七个类别的新闻，各1000条
* **test.ipynb** - Word2Vec文本分类，内容审核调用处理
* w2vt.ipynb - 尝试基于词向量模型构建embedding，训练分类模型（未完善，数据集不够）

## 使用
* Weibo-search 设置关键词、时间范围
```bash
$ scrapy crawl search 
```
* test.ipynb 对文本数据处理；对爬取内容进行审核
* 百度文本审核API ：[百度内容审核，点击注册创建实例](https://ai.baidu.com/tech/textcensoring?track=cp:ainsem|pf:pc|pp:878-chanpin-neirongshenhe|pu:neirongshenhe-minganciguolv|ci:|kw:10531584
)