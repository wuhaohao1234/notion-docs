# React中的两种路由方式原理

React是一个非常流行的JavaScript库，用于构建用户界面，它提供了两种路由方式：HashRouter和BrowserRouter。这两种路由方式都可以用来实现单页应用程序（SPA）中的路由功能，但它们的工作原理有所不同。

## HashRouter

HashRouter是一种基于URL哈希值的路由方式。在HashRouter中，URL中的哈希值被用来表示应用程序的不同状态，而不是表示不同的网页。例如，当用户访问`http://example.com/#/about`时，浏览器会显示关于页面的内容。在这种情况下，`#/about`表示应用程序的状态，而不是一个实际的网页。

HashRouter使用浏览器的`window.location.hash`属性来监听URL中哈希值的变化，并根据哈希值的变化来更新UI。由于哈希值的变化不会引起浏览器向服务器发送请求，因此使用HashRouter可以实现无刷新的页面更新。

## BrowserRouter

BrowserRouter是一种基于HTML5历史API的路由方式。在BrowserRouter中，URL的路径部分被用来表示应用程序的不同状态，而不是表示不同的网页。例如，当用户访问`http://example.com/about`时，浏览器会显示关于页面的内容。在这种情况下，`/about`表示应用程序的状态，而不是一个实际的网页。

BrowserRouter使用浏览器的`window.history.pushState`方法来监听URL的变化，并根据URL的变化来更新UI。由于使用了HTML5历史API，所以BrowserRouter可以实现更加优雅的URL，而且不需要在URL中包含哈希值。

总的来说，HashRouter和BrowserRouter都可以用来实现React应用程序中的路由功能。HashRouter使用哈希值来实现路由，而BrowserRouter使用HTML5历史API来实现路由。具体的选择取决于您的应用程序的需求和您的个人偏好。