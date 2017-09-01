
react
====

    1.组件化
    2.单向数据流
    3.一个react组件可以理解成一个独立的函数，接受参数（props),可复用，可以传递，返回结果（渲染组件）
    4.虚拟DOM树
    5.可以在node.js中运行（服务器端运行）

##  简单的react示例
    示例1：
        var HelloWorld = React.createClass({
            render : function(){
                return <p> Hello {this.props.name}</p>;
            }
        });
        Rendering the component on the page:
        React.render(
            <HelloWorld name="john" />,
            document.getElementById("app")
        );

##  JSX是什么？
    javaScript 的xml语法扩展
    采用你所熟悉并且易于理解的语法来定义DOM树

##  React是如何使用JSX的？

    <p className="hello">
        Hello {this.props.name}
    </p>
    将编译成React构造器的方法：
    React.createElement("p",
                        {className:"hello"},
                        "Hello",
                        this.props.name
    )
    嵌套的子组件：
    <p>
        Hello <a href="https://www.baidu.com"> LocalMed</a>
    </p>
    将编译成React构造器的方法：
    React.createElement("p",
                       null,
                        "Hello",
                        React.createElement("a",
                                            {href:"http://www.baidu.com"},
                                            "LocalMed"
                        )
    )

##  setState 之后发生了什么 —— 浅谈 React 中的 Transaction
    https://undefinedblog.com/what-happened-after-set-state/

##  使用React.setState需要注意的三点
    http://www.cnblogs.com/little-ab/articles/6958852.html

##  React从入门到精通系列
    https://segmentfault.com/u/zhangyatao/articles
    
object getInitialState()
在组件挂载之前调用一次。返回值将会作为 this.state 的初始值。


##  使用PropTypes进行类型检测
https://segmentfault.com/a/1190000007814801


## 使用ref refs

## react-with-addons.js 包含了一下插件 可以实现双向数据流


## 组件生命周期（The Component Lifecycle）

    https://facebook.github.io/react/docs/react-component.html

Mounting    装载

Updating    更新

Unmounting  卸载



##  React创建组件的三种方式比较
　  推荐文章： https://www.cnblogs.com/wonyun/p/5930333.html

　　创建组件的方式主要有：

　　1、function 方式

　　2、class App extends React.component {}

　　3.  React.creatClass 

　　大致区别： function创建组件的方式最为高效，但是其只能传递props，而不能使用状态等。
     extends React.component 的方式功能更为强大，他不仅可以通案过 this.props 来使用prop并且还可以使用状态管理，另外，还可以通过 extends 继承 React.pureComponent ，这样，我们就更加容易使用钩子函数等。

 

　　http://cn.redux.js.org/docs/basics/UsageWithReact.html

　　这篇文章中也大致介绍了function方式和class方式的区别，即function方式适用于只有props的组件，而class方式适用于希望使用本地state、声明周期方法、性能优化的情况。

 
## mixin  让不同的组件共用一些逻辑代码








