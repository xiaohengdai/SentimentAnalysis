/usr/local/bin/python3.7 -m pip install gensim -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com
 /Library/Frameworks/Python.framework/Versions/3.8/bin/python3 -m pip uninstall  scipy
 
 
 - 问题1
 ```
ValueError: Error downloading 'wordnet_ic' from <https://raw.githubusercontent.com/nltk/nltk_data/gh-pages/packages/corpora/wordnet_ic.zip>:
  <urlopen error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1045)>
解决办法：
看报错代码，for token in ("wordnet", "wordnet_ic", "sentiwordnet"):
    try:
        nltk.data.find("corpora/" + token)
是需要将下好的放在corpora目录下，报错处有提示：Searched in:
    - '/Users/xiaoheng/nltk_data'
故可将下载好的放到/Users/xiaoheng/nltk_data/corpora/目录下
```

- 问题2
python3.7


- 问题3
```
解决Keras加载模型TypeError: ('Keyword argument not understood:', u'return_state'):https://blog.csdn.net/yutingzhaomeng/article/details/78516145
```

- 问题4
```
RuntimeError: you must first build vocabulary before training the model:
用word2vec训练词向量是报错，百度发现是因为训练文本太小的。
为了省事，随便往训练文本里敲了点东西，这样是远远不够的。
增大训练文本之后，问题解决。
```