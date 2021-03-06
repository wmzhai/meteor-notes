# A. 术语表

** 客户端 Client **

当我们谈论客户端时，我们指的是用户的**网页浏览器**，不论是传统的像 Firebox 或 Safari 的浏览器，或是像在 iPhone 原生应用中的 UIwebView 一样复杂的其他程序。

** 集合 Collection **

Meteor 的集合是自动在客户与服务器之间同步的数据源。集合的名称（比如 `posts`）通常存在于客户端和服务器端。虽然它们表现不同，但是它们有共同的基于 Mongo 的 API。

** 组件 Component **

Meteor支持3个界面库Blaze，React和Angular，其用来构建的可复用界面元素称为“组件(Component)”。

** Computation **

Computation 就是每当响应数据源变化时而运行的代码块。如果你想让一个响应数据源去响应处理（比如，Session 变量），你需要为它来设置一个 computation。

** 游标 Cursor **

Cursor 是查询 Mongo 集合后的结果。在客户端，cursor 不仅仅是结果的数组，也是一个*响应的*对象，对应于相关集合的添加、删除和更新对象。

** 分布式数据协议 DDP **

DDP 是 Meteor 的分布式数据协议，用来同步集合和调用方法。DDP 的目的是作为一个通用的协议，在大数据的实时应用中起 HTTP 的作用。

** Tracker **

Tracker 是 Meteor 响应性系统。Tracker 在后台使 HTML 自动保持与底层数据模型的同步。

** 文档 Document **

Mongo 是基于文档（document）的数据库，多个文档组成集合。它们是纯 JavaScript 对象（虽然它们不能包含函数），只有一个 `_id` 属性，Meteor 用这个属性通过 DDP 跟踪这些对象的属性。

** Helper **

当模板需要渲染复杂的多于一个文档属性时，调用 helper 以函数方式来完成渲染任务。

** 延迟补偿 Latency Compensation **

延迟补偿是一种在客户端模拟方法调用以避免等待服务器回应的一种技术。

** 方法 Method **

Meteor 方法是一个从客户端到服务器端的远程调用，以一些特别的逻辑保持跟踪集合的更改和允许延迟补偿。

** MiniMongo **

客户端的集合，是有类似 Mongo API 并存在内存的数据源。支持这种操作的库叫做“MiniMongo”，是在内存中运行的小版本的 Mongo。

** 代码包 Package **

Meteor 代码包可以包含服务器端运行的、客户端运行的 JavaScript 代码，处理资源的说明（比如 SASS 至 CSS），处理的资源。<br/>代码包就像一个超级库。Meteor 自带了很多核心代码包，同时在 [Atmosphere](http://atmosphere.meteor.com) 集合了社区提供的第三方代码包。

** 发布 Publication **

一个发布就是一套为每个订阅用户而订制的数据。在服务器端设置发布。

** 服务器 Server **

Meteor 服务器是运行在 Node.js 之上的 HTTP 和 DDP 服务器。它包含了所有的 Meteor 库，同时也包含了你的服务器端的 JavaScript 代码。当 Meteor 服务器启动时，它会连接 Mongo 数据库（在开发模式时，会自启动）。

** 会话 Session **

在 Meteor 中，会话指的是客户端的响应数据源，用来跟踪用户所处的状态。

** 订阅 Subscription **

订阅是为特定客户的发布的连接。订阅是运行在浏览器中的代码，与服务器的发布对话，并保持数据同步。

** 模板 Template **

模板就是一个通过 JavaScript 生成 HTML 的方法。Meteor 默认支持 Spacebars 模板系统，但是将来也会支持其他系统。

** 模板数据上下文 Template Data Context **

当模板渲染时，它指的是 JavaScript 对象为此次渲染提供特定的数据。通常来说，对象就是纯原始的 JavaScript 对象（POJO），经常也是集合的文档，但是它们也可以变得更复杂，可拥有函数。
