# Chinese Dictionary for Elasticsearch Analysis-IK

**Enhance your Elasticsearch search capabilities for Chinese text!**  
This open-source Chinese dictionary is designed to extend the [analysis-ik plugin](https://github.com/medcl/elasticsearch-analysis-ik) for Elasticsearch, improving Chinese text segmentation accuracy and search relevance. Perfect for developers and search engineers looking to optimize Chinese language processing in Elasticsearch.

---

## About

**Chinese Dictionary for Elasticsearch Analysis-IK** is an open-source project aimed at enhancing the Chinese text segmentation capabilities of the popular [analysis-ik plugin](https://github.com/medcl/elasticsearch-analysis-ik). By integrating this dictionary, you can achieve:

- **More accurate tokenization:** Better segmentation of Chinese words leads to more relevant search results.
- **Improved search performance:** Enhanced search precision and recall.
- **Easy integration:** Seamlessly extend your Elasticsearch instance with custom dictionaries.

*Keywords: Elasticsearch, analysis-ik, Chinese dictionary, Chinese text segmentation, open-source, search optimization, natural language processing*

This project is actively maintained by the community. Contributions, suggestions, and improvements are welcome!

---

## Features

- **Accurate Chinese Word Segmentation:** Significantly improves the default segmentation of the analysis-ik plugin.
- **Customizable Dictionary and Stopwords:** Easily extend or modify the dictionary based on your specific use case.
- **Open Source Community:** Actively maintained and improved through community contributions.
- **SEO & Performance Optimization:** Enhance search results with finely tuned text segmentation.

---

## How to Use

1. **Download the Dictionary File:**  
   Download the [main.dic](./main.dic) file, which contains the core vocabulary for the dictionary.

2. **Configure the Analysis-IK Dictionary Directory:**  
   Set up your analysis-ik dictionary configuration by creating or modifying the XML configuration file (e.g., `ik_dict.xml`). Below is an example configuration:

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
   <properties>
       <entry key="ext_dict">custom/mydict.dic;custom/single_word_low_freq.dic</entry>
       <entry key="ext_stopwords">custom/ext_stopword.dic</entry>
       <entry key="remote_ext_dict">location</entry>
       <entry key="remote_ext_stopwords">http://xxx.com/xxx.dic</entry>
   </properties>
   ```

3. **Deploy the Dictionary File:**  
   Copy or move the downloaded `main.dic` file to your analysis-ik configuration directory so that it aligns with your XML settings.

4. **Restart Elasticsearch:**  
   After configuring, restart your Elasticsearch service to apply the new dictionary settings.

---

## Installation & Setup

1. **Clone the Repository:**  
   Clone the repository from GitHub:
   ```bash
   git clone https://github.com/junminhong/es-analysis-ik-zh-dict
   ```

2. **Configure the Dictionary:**  
   Adjust the XML configuration file to match your Elasticsearch and analysis-ik installation directory.

3. **Restart Your Service:**  
   After updating the configuration, restart Elasticsearch to activate the dictionary enhancements.

---

## License

This project is licensed under the [MIT License](./LICENSE). Feel free to use, modify, and distribute it as needed.
