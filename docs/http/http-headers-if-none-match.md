# HTTP 头|如果不匹配

> 原文:[https://www.geeksforgeeks.org/http-headers-if-none-match/](https://www.geeksforgeeks.org/http-headers-if-none-match/)

**HTTP 头如果不匹配**是请求类型的头。通常，它用于更新服务器上的实体标签。首先，客户端向服务器提供一组实体标签**(电子标签)**。服务器将给定的标记与它已经拥有的资源标记进行比较。然后，服务器将提供请求的页面一个 **200 状态代码**只有当没有一个实体标签给它匹配。否则，服务器返回 **304 未修改**状态。

有两种类型的算法用于比较实体标签。它们是:

*   弱比较算法
*   强比较算法

**弱比较算法:**它忽略了实体标签之间被认为不重要的微小差异。例如，具有相同内容但不同日期的两个标签被认为是相同的。

**强比较算法:**逐字节检查标签**。**

****语法:****

```html
If-None-Match: "entity_tag"
```

```html
If-None-Match: *
```

****注:****“***用于表示任何资源。**

****指令:**该标题接受两个指令，如上所述，如下所述:**

*   ****entity_tag:** 表示被请求的资源。这是一个包含字母、数字和其他特殊字符的**字符串**，包含在**双引号(" ")中。****
*   ****“*:**它代表任何资源，用于避免 **PUT** 操作之间的竞争情况。当使用此指令时，如果给它的实体对于该资源已经存在，则服务器不应执行请求的方法。**

****示例:****

*   ```html
    If-None-Match:"2780-5524acffbda80-gzip"
    ```

*   ```html
    If-None-Match:*
    ```

**要检查该“如果-不匹配”是否有效，请转到**检查元素- >网络**检查“如果-不匹配”的请求头，如下所示。如果不匹配，则突出显示标题。
T3】**

****支持的浏览器:**浏览器兼容 **HTTP 如果不匹配标题**如下:**

*   **谷歌 Chrome**
*   **微软公司出品的 web 浏览器**
*   **Mozilla Firefox**
*   **微软边缘**
*   **歌剧**
*   **旅行队**