## 需求描述
### 文章抓取和分析
1. 定时自动抓取CSDN、Iteye两个网站指定账号发表的文章，包括文章标题、文章分类、发表分组、发表人、发表时间、阅读次数、评论次数。
    * 支持配置定时间隔、网站账号

### 汇总统计
1. 提供web页面展示文章的发表情况，支持如下查询条件:
网站来源、博客ID、分组、作者、发表时间范围、文章分类
2. 按月汇总分组总的文章数量、阅读次数，分组排名
    * 每篇文章从发表开始统计90天的阅读量，前30天100%，后面50%、25%；例如：流程管理组5月20号发表了一篇文章，5月31号阅读量为100，那5月底的比赛会统计一次为100，6月低的比赛会分成6月1号~6月19号的阅读量*100%，6月20号到6月30号的阅读量*50%，依次类推。

### 邮件自动通知
1. 每周自动发送邮件到部门邮件群，邮件内容包括当月分组的排名，按分组展示当月发表的文章（点击标题打开浏览器查看详细内容），阅读和回复量。
2. 每天有新的文章发表，系统自动邮件发送通知大家。

### 设计要求
1. B/S架构，DB采用MYSQL，编程语言不限。
2. 避免单点，考虑数据备份。
3. 运行环境不要求一定在公司内部。