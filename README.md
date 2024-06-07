# Chinese dictionary for elasticsearch analysis-ik
主要用於擴充 analysis-ik plugin 詞庫, 增加中文搜尋分詞的準確性

## How to use
1. Download main.dic file
2. Configure your analysis-ik dict configuration directory
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
<properties>
	<entry key="ext_dict">custom/mydict.dic;custom/single_word_low_freq.dic</entry>
	<entry key="ext_stopwords">custom/ext_stopword.dic</entry>
	<entry key="remote_ext_dict">location</entry>
	<entry key="remote_ext_stopwords">http://xxx.com/xxx.dic</entry>
</properties>
```
3. Then copy or move the main.dic file to your analysis-ik configuration directory
4. Restart your elasticsearch service
