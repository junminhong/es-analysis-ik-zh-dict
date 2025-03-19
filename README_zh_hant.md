# Elasticsearch Analysis-IK 中文詞庫

**提升 Elasticsearch 中文搜尋能力！**
這個開源的中文詞庫旨在擴展 [analysis-ik 插件](https://github.com/medcl/elasticsearch-analysis-ik)，改善中文分詞準確性和搜尋相關性。非常適合希望優化 Elasticsearch 中文語言處理的開發者與搜尋工程師。

---

## 關於

**Elasticsearch Analysis-IK 中文詞庫** 是一個開源專案，致力於提升廣受歡迎的 [analysis-ik 插件](https://github.com/medcl/elasticsearch-analysis-ik) 的中文分詞功能。通過整合此詞庫，您可以達到以下效果：

- **更準確的分詞：** 更精細的中文斷詞可帶來更相關的搜尋結果。
- **改善搜尋效能：** 提升搜尋精確度與召回率。
- **輕鬆整合：** 無縫擴展您的 Elasticsearch 實例，使用自訂詞庫。

*關鍵字：Elasticsearch、analysis-ik、中文詞庫、中文分詞、開源、搜尋優化、自然語言處理*

本專案由社群積極維護，歡迎提交貢獻、建議或改進！

---

## 特色

- **精準中文分詞：** 顯著改善 analysis-ik 插件預設的分詞效果。
- **可自訂詞庫與停用詞：** 根據實際需求輕鬆擴充或調整詞庫。
- **開源社群：** 社群持續維護與改進，提供最新最佳化。
- **SEO 與效能優化：** 經過調整的分詞結果可大幅提升搜尋效果。

---

## 使用方式

1. **下載詞庫檔案：**
   下載 [main.dic](./main.dic) 檔案，此檔案包含詞庫核心字彙。

2. **配置 Analysis-IK 詞庫目錄：**
   建立或修改 XML 配置檔（例如 `ik_dict.xml`）來設定 analysis-ik 詞庫目錄。以下是一個範例配置：

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

3. **部署詞庫檔案：**
   將下載好的 `main.dic` 檔案複製或移動到您的 analysis-ik 配置目錄中，確保與 XML 配置一致。

4. **重啟 Elasticsearch：**
   完成配置後，重啟 Elasticsearch 服務以應用新的詞庫設置。

---

## 安裝與設置

1. **克隆倉庫：**
   從 GitHub 克隆本倉庫：
   ```bash
   git clone https://github.com/junminhong/es-analysis-ik-zh-dict
   ```

2. **配置詞庫：**
   根據您的 Elasticsearch 與 analysis-ik 插件安裝路徑，調整 XML 配置檔中的路徑與參數。

3. **重啟服務：**
   更新配置後，重啟 Elasticsearch 以啟用詞庫增強功能。

---

## 授權

本專案採用 [MIT 授權條款](./LICENSE) 發佈，歡迎自由使用、修改和分發。
