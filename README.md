# markdown
# Markdown——入门指南

### Markdown 语法的简要规则

[原文](https://www.jianshu.com/p/1e402922ee32/)

#### 标题

\# 一级标题      

#一级标题

\## 二级标题

## 二级标题

\###三级标题

### 三级标题

\#### 四级标题

####四级标题

\##### 五级标题

#####五级标题

\###### 六级标题

###### 六级标题

![](http://ww1.sinaimg.cn/large/6aee7dbbgw1effeaclhiyj20eh09cwez.jpg)

#### 列表

列表的显示只需要在文字前加上 - 或 * 即可变为无序列表，有序列表则直接在文字前加1.2.3.符号要和文字之间加上一个字符的空格。

##### 无序列表

* 1
* 2
* 3



- 1
- 2
- 3

##### 有序列表

1. 1
2. 2
3. 3

![](http://ww4.sinaimg.cn/large/6aee7dbbgw1effew5aftij20d80bz3yw.jpg)



#### 引用

如果你需要引用一小段别处的句子，那么就要用引用的格式。

> 这是引用

只需要在文本前加入 `>` 这种尖括号（大于号）即可

![](http://ww3.sinaimg.cn/large/6aee7dbbgw1effezhonxlj20e009c3yu.jpg)

#### 图片与链接

插入链接与插入图片的语法很像，区别在一个 `!`号

图片为：`![]()`

链接为：`[]()`



插入链接

[百度](www.baidu.com)

插入图片

![](http://ww2.sinaimg.cn/large/6aee7dbbgw1efffa67voyj20ix0ctq3n.jpg)

#### 粗体与斜体

Markdown 的粗体和斜体也非常简单，用两个 `*` 包含一段文本就是粗体的语法，用一个 `*` 包含一段文本就是斜体的语法。

**这是粗体**

 *这是斜体*



#### 表格

| Tables | Are  | Cool |
| ------ | ---- | ---- |
| 1      | 2    | 3    |
| 4      | 5    | 6    |
|        |      |      |
|        |      |      |
|        |      |      |
|        |      |      |

\| Tables 	|Are 		|Cool			|



#### 代码框

只需要用两个`把中间代码包裹起来

```java
public void doGet(HttpServletRequest request,
        HttpServletResponse response) throws ServletException,
        IOException {

    Cookie[] cookies = request.getCookies();
    Cookie maxRecordsCookie = null;
    if (cookies != null) {
        for (Cookie cookie : cookies) {
            if (cookie.getName().equals("maxRecords")) {
                maxRecordsCookie = cookie;
                break;
            }
        }
    }
    
    int maxRecords = 5; // default
    if (maxRecordsCookie != null) {
        try {
            maxRecords = Integer.parseInt(
                    maxRecordsCookie.getValue());
        } catch (NumberFormatException e) {
            // do nothing, use maxRecords default value
        }
    }
    
    response.setContentType("text/html");
    PrintWriter writer = response.getWriter();
    writer.print("<html><head>" + "<title>Cookie Class</title>"
            + "</head><body>" 
            + PreferenceServlet.MENU
            + "<div>Here are some of the methods in " +
                  "javax.servlet.http.Cookie");
    writer.print("<ul>");
    
    for (int i = 0; i < maxRecords; i++) {
        writer.print("<li>" + methods[i] + "</li>");
    }
    writer.print("</ul>");
    writer.print("</div></body></html>");
}
```

#### 分割线

分割线只要三个\*

***















