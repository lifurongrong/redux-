 redux有两个函数分别是createStore和combineReducers
 
    createStore接收一个参数reducer创建一个对象，对象里存储了getState、dispatch、subscribe三个方法
            reducer在dispatch内部执行，是个纯函数，reducer是使用redux的用户自己编写的函数，规则是redux规定的，需要state和action两个参数，reducer的作用有两个1、初始化state2、修改state
            getState返回state
            dispatch是redux提供的修改state的途径
            subscript是利用发布订阅模式把需要做的事情存放在事件池中，等到dispatch的时候会执行事件池里的事件
            
    combineReducers是为了把多个reducer合并成一个reducer，返回值还是一个函数，接收一个对象作为参数，对象里存放的是需要合并的reducer，属性名自己定义，属性值是各个reducer
