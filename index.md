# Es常用地址

```sh
#删除resident索引下的数据
curl -X POST "localhost:9200/resident/_delete_by_query" -H 'Content-Type: application/json' -d'{"query": {"match_all": {}}}'
#新建索引
curl -X PUT  "localhost:9200/test" -H 'Content-Type: application/json' -d'{"settings": {"number_of_shards": 1,"number_of_replicas":1 }}'
#删除索引数据之后还占用空间，可以执行这个
curl -X POST "localhost:9200/resident/_forcemerge?only_expunge_deletes=true"
#查看节点信息
curl "localhost:9200/_cat/nodes"

```



### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/huihuiwuhui/testpage/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
