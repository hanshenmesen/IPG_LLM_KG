# 政府招商引资知识图谱（Investment Promotion Knowledge Graph）

本项目用于构建中国政府招商引资领域知识图谱，数据由大语言模型辅助抽取而来，政策文件下载自北大法宝平台。

## 数据说明

数据文件为三元组格式，字段包括：

- 头部实体
- 头部实体类型
- 关系
- 尾部实体
- 尾部实体类型

示例：

| 头部实体 | 头部实体类型 | 关系 | 尾部实体 | 尾部实体类型 |
|----------|------------|------|----------|--------------|
|《A政策》  | 政策文件    | 引用 |《B政策》  |  政策文件    |


## 使用方法

修改`to_neo4j.py`中的数据库连接信息和数据文件路径：

```python
NEO4J_URI = "bolt://localhost:7687"
NEO4J_USERNAME = "neo4j"
NEO4J_PASSWORD = "your_password_here"

CSV_FILE_PATH = r''
```

导入完成后即可在Neo4j界面查看知识图谱。
![image](https://github.com/user-attachments/assets/1deba891-a521-41fa-b076-fbf9d9f2d5c5)


