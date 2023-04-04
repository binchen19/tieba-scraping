# tieba-scraping
Scraping Baidu Tieba posts and replies using R:
- Scraping posts of interest from a specific Tieba (post_topic, urls)
- Scraping replies of posts of interest (author, date-time, texts)

# 百度贴吧爬虫 R
我在收集百度贴吧数据的时候发现目前已有的贴吧爬虫大部分基于python, 尝试了几个现成的项目之后决定试试用R来实现。
数据需求主要是：
- 收集主题帖和回复数据
基本策略：
- 首先例如贴吧网站搜索功能（吧内/全站）得到搜索结果页面，然后锁定自己感兴趣的页码（例如搜索结果页面的5-10页）
- 使用网页翻页爬取每一页搜索页面的主题帖URL
- 对每一个主题帖爬取所有楼层回复（用户名，日期/时间，回复内容）
