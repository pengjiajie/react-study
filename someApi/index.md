### PropTypes
组件类的PropTypes属性，就是用来验证组件实例的属性是否符合要求。

```javascript
var MyTitle = React.createClass({
  propTypes: {
    title: React.PropTypes.string.isRequired,
  },
  render: function() {
     return <h1> {this.props.title} </h1>;
   }
});
```
上面的Mytitle组件有一个title属性。PropTypes 告诉 React，这个 title 属性是必须的，而且它的值必须是字符串。<br/>
更多的PropTypes设置，可以查看<a href="https://reactjs.org/docs/components-and-props.html" target="_blank">官方文档</a>。

### getDefaultProps
getDefaultProps 方法可以用来设置组件属性的默认值。

```javascript
var MyTitle = React.createClass({
  getDefaultProps : function () {
    return {
      title : 'Hello World'
    };
  },
  render: function() {
     return <h1> {this.props.title} </h1>;
   }
});
ReactDOM.render(
  <MyTitle />,
  document.body
);
```

