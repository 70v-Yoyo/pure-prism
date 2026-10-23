---
title: 我的文章
date: 2026-10-23
tags:
  - CSS
---

---

# 一级标题

## 二级标题

### 三级标题

这是普通段落。**粗体**，*斜体*，***粗斜体***，~~删除线~~，<u>下划线</u>，`行内代码`，H~2~O（下标），X^2^（上标） ，键盘按键：<kbd>⌘</kbd>

-   TypeScript
    -   类型系统

1.  明确问题
    1.  检查正常路径

-   [x] 检查 Mermaid 渲染
-   [ ] 检查数学公式

> 一级引用：Markdown 是轻量级标记语言。
>
> > 二级引用：适合记录结构化知识。
> >
> > -   引用中可以嵌套列表也可以包含 `代码`

-   行内链接：[Typora 官网](https://typora.io/)
-   自动链接：<https://typora.io/>

![示例图片：Typora](https://dummyimage.com/640x240/eeeeee/222222.png&text=Typora+Markdown+Preview)

| A    | B    |
| ---- | ---- |
| 1    | 2    |
| 3    | 4    |

``` javascript
const debounce = (fn, delay = 300) => {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
};

const search = debounce((keyword) => {
  console.log("search:", keyword);
}, 300);

search("Typora");
```

行内公式：质能关系 \(E = mc^2\)，以及二次方程求根公式中的判别式 \(\Delta = b^2 - 4ac\)。

独立公式：

$$
\int_{-\infty}^{+\infty} e^{-x^2}\,dx = \sqrt{\pi}
$$

这里有一个脚注引用。[^note]

<details>
<summary>点击展开 HTML 折叠区</summary>
``` mermaid
flowchart LR
    A[输入请求] --> B{参数有效}
    B -->|是| C[执行业务逻辑]
    B -->|否| D[返回错误]
    C --> E[输出结果]
```

### 饼图

``` mermaid
pie showData
    title Time Allocation
    "Coding" : 50
    "Reading" : 30
    "Testing" : 20
```

### 思维导图（需较新 Mermaid 版本）

``` mermaid
mindmap
  root((Typora))
    Markdown
      Headings
      Lists
      Tables
    Code
      Syntax Highlighting
    Diagrams
      Flowchart
      Sequence
```

### 流程图

```mermaid
flowchart TD
    A[用户请求] --> B{是否登录}
    B -->|是| C[查询数据]
    B -->|否| D[跳转登录]
    C --> E[返回结果]
    D --> E

```



```mermaid
sequenceDiagram
    participant U as 用户
    participant F as 前端
    participant B as 后端
    participant D as 数据库

    U->>F: 点击查询
    F->>B: 发送 HTTP 请求
    B->>D: 查询数据
    D-->>B: 返回数据
    B-->>F: 返回 JSON
    F-->>U: 展示结果

```



```mermaid

classDiagram
    class User {
        +String name
        +login()
        +logout()
    }

    class Admin {
        +deleteUser()
    }

    User <|-- Admin



```



```mermaid
stateDiagram-v2
    [*] --> Pending
    Pending --> Running: 开始执行
    Running --> Success: 执行成功
    Running --> Failed: 执行失败
    Failed --> Running: 重试
    Success --> [*]

```

### ER图

```mermaid
erDiagram
    USER ||--o{ ORDER : creates
    ORDER ||--|{ ORDER_ITEM : contains
    PRODUCT ||--o{ ORDER_ITEM : references

    USER {
        int id PK
        string name
    }

    ORDER {
        int id PK
        int user_id FK
    }

    PRODUCT {
        int id PK
        string name
    }

```

### 甘特图

```mermaid
gantt
    title 项目开发计划
    dateFormat YYYY-MM-DD

    section 后端
    API 设计 :a1, 2026-10-01, 3d
    API 开发 :after a1, 5d

    section 前端
    页面开发 :2026-10-04, 5d
    联调测试 :2026-10-09, 3d

```

### 时间线

```mermaid
timeline
    title Web 技术演进
    1991 : HTML 诞生
    1995 : JavaScript 出现
    2006 : jQuery 流行
    2013 : React 发布
    2014 : Vue 发布

```

### 架构图

```mermaid
C4Context
    title 电商系统上下文

    Person(user, "用户", "购买商品")
    System(shop, "电商系统", "商品与订单管理")
    System_Ext(payment, "支付系统", "处理支付")

    Rel(user, shop, "浏览与下单")
    Rel(shop, payment, "发起支付")

```

### X-Y图表

```mermaid
xychart-beta
    title "接口响应时间"
    x-axis ["周一", "周二", "周三", "周四", "周五"]
    y-axis "毫秒" 0 --> 500
    bar [320, 280, 350, 200, 180]
    line [320, 280, 350, 200, 180]

```

### 看板图

```mermaid
kanban
    todo[待办]
        task1[实现登录]
        task2[设计数据库]
    doing[进行中]
        task3[开发接口]
    done[已完成]
        task4[搭建项目]

```

### 数据包图

```mermaid
packet-beta
    title TCP 头部字段示意
    0-15: "源端口"
    16-31: "目标端口"
    32-63: "序列号"
    64-95: "确认号"

```
