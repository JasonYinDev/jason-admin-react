# jason-admin-react

## This is a project under development!

------
## 这是一个正在开发中的项目！

这是一个基于react开发的admin 系统，我在学习react的过程中，开发了此系统，所以再各个阶段，可能看到的这个系统并不一样。在初期这个系统甚至是一个不可用的状态。

有着很多我的个人特色，本仓库随意下载使用。

20230819补充：原本想着学习react的过程顺便写一个工作台，但学到今天，暂时放弃了，目前考虑优先完成techui-react-lite的开发工作。这个工作台离完成还差得远，甚至动态路由的bug依然存在。


------
## 学习日志

**注意现在首次进入是空白屏幕，20230811第三条描述的此bug产生的详细原因，因为动态路由未完善导致的。**

- 20230809
  - 习惯用vue了，react写着真费劲，长期习惯了solo开发，没怎么用过TS，现在学React的同时用TS写代码，非常痛苦。
  - 用TS写完这个工程，就会把TS雪藏了，除非团队协作必须上TS，否则solo开发绝对不会用TS，完全就是给自己上枷锁。
  - 今天到此为止，明天要移除semi-ui改用antd。

- 20230810
  - 替换semi-ui为antd
  - 集成mock，为动态路由做准备，折腾好久没生效，发现是版本问题！
  - 完成简易登录页面
  - 完成路由守卫开发
  - 完成axios封装和调用
  - 心得：用习惯了vue2-3+elementUI，使用react+atd的时候感觉很多东西都比较繁琐。vue yyds! 尤其vue3的写法，和原生差不多，模板语法写起来比jsx、tsx要爽很多。
  - 晚上8:10分折腾了几个小时的动态路由终于写完了，自己想出来的一个方案，其实是根据之前vue的动态路由思路实现的。结果还可以。
  - 之前写vue3动态路由的时候，文件的动态导入受限，不支持多层目录嵌套式的动态导入。这次在react实现的时候，新建了一个文件预先导入了各个组件，然后在序列化路由的时候再把组件赋值给路由，无需像之前一样动态加载组件。后期写一下懒加载，应该就很完美了。回头把vue3工作台的动态路由也按照这个思路完善一下。

- 20230811
  - 动态路由写完后，又做了一下改善，首先把mock导航数据，存放到了sessionStorage中，然后侧边栏用这个数据来初始化导航，路由则拿这个数据来初始化路由，但是初始化的时候，同时把导航数据扁平化，这样方便做导航跳转。其实不做扁平化也行，但并不想路由的层级太深，否则需要不断嵌套一个layoutCommone组件。
  - **动态路由有一个问题，就是进入登录的时候，未获取到mock的导航数据，router已经初始化，所以目前的状况就是首次进来后，导航和路由都未初始化，需要刷新才能让router.tsx获取到导航数据并初始化。后续学习高阶组件后，再回过头处理这个问题。**
  - 学习和配置了redux的使用，太繁琐了，怀念vuex的便利，还有TS....习惯solo了，使用TS浑身不舒服，就和套了一层枷锁一样。
  - 导航配置完毕，包括导航的展开和激活状态
  - 备注一下后续要看的几个状态管理的库，1.zustand 2.jotai 3.mobx 4.recoil 5.dva
  - 界面比较丑陋，我UI设计入行的，这方面最拿手，也因此UI界面对于学习来说不重要，凑合看即可。
  - 明天继续！

- 20230812
  - 今天重新封装了axios，重写了api等接口ts
  - 新增了全局的types interface文件
  - 登录新增了验证码功能，数据请求自mockjs
  - 深入学习redux，更加坚定要放弃redux，太繁琐了。
  - 根据其他视频教程做了一些案例。
  - 有一些TS类型错误，不知道如何解决。后续再说。

- 20230813
  - 根据网上的视频，对比了vue中提供的一些语法糖和功能，用react如何使用
  - 相关的案例，放到了sub目录中的这些ts文件中。
  - 还是很不错的一个课程，作者叫“最爱白菜”

- 20230814
  - 开始二刷TS语法，之前系统的学过一次TS语法，是为了用assemblyScript语言来写webassembly模块。但是写了一些工具后，发现这个语言完成度非常差，所以就放弃了。转而学习rust来写webassembly组件。所以TS从那之后就搁置了。大概是5月份左右。
  - 现在二刷巩固一下TS的语法，顺便再次巩固js和ts中类的概念以及构造函数等。

- 20230815
  - 跟着教程，练习TS语法

- 20230816
  - 网上看了看贪吃蛇的逻辑，用React+TS实现了一下，主要是为了锻炼react中的父子组件之间的传参和函数调用。
  - 明天再完善，如蛇头碰撞自己身体等，再添加暂停继续重来等功能，以及虚拟按键。

- 20230817 
  - 早8:30
  - 贪吃蛇完工，早上完成了如下功能
    - 禁止蛇头朝反方向掉头
    - 监测身体碰撞
    - 添加rest功能
    - 如果蛇非live状态，无法通过按键激活，必须reset重新玩
  - 这个react的练手工程暂时搁置，今天看更多的react案例，确保没有遗漏重要的知识点后于今天下午或者明天开始写techui-react-lite。
  - 晚19:17
  - 今天三刷了TS的一些基础课程
  - 开始学习React的高阶hook，之前只用到了useState，useEffect
  - 今天学习了useContext的使用方式，明天继续学习useReducer，useMemo，useCallback，useLayoutEffect，useRef
  - 再追加一个高阶组件的使用方法


- 20230810
  - 今天深入的学习了useContext和useReducer，其中useReducer的使用场景还是有点迷糊，感觉useState完全可以取代usereducer，不明白其使用的意义。
  - 明天继续学习其他的一些Hook，目前收集到的react的hook列表
    - useState
    - useEffect
    - useContext
    - useReducer
    - useCallback
    - useMemo
    - useRef
    - useLayoutEffect
    - useImperativeHandle
    - useDebugValue

- 20230819
  - 继续巩固一下useReducer是使用场景，
  - 我之前想useContext也能取代useReducer，但后来想想这个Context字面意思是上下文，父子孙这种情况用比较合适。也不一定用状态管理取代useReducer，因为可能同一类型的页面的逻辑并不适合放到全局的状态里面。
  - 从官方案例中了解到use-immer这个库，可以取代useReducer，能让不可变内容变成可变内容，从而直接修改值，而不用[...task,{id:action.id,text:action.text}]这样去修改，mark一下后续考虑使用 npm install immer use-immer
  - 今天学习了memo, useMemo，useCallback，useRef，forwadRef，useLayoutEffect
  - 简单了解了一下useImperativeHandle，或许还有其他的hook，暂时关于hook的学习就到这里。
  - 另外看了看HOC高阶组件，但是发现都是class的写法，查询react官网，发现已经没有HOC了，估计和class组件一样被放弃了，所以这块学习就不继续了。
  - 简单看了看zustand这个状态管理，打算抛弃redux使用zustand。
  - 基本上今天之后，react的学习可以说就告一段落了，接下来可能开始写techui-react-lite

- 20230820
  - react基本都学完了，今天学了一下useimmer，useImmerReducer
  - 深入学习了一下zustand的进阶用法以及结合immer来使用zustand
  - 感觉zustand可以取代useContext和useReducer，不过在组件封装的时候还是得使用这两个。 
  

## 结语
今天是20230819，学习react历时大概10天（此前断断续续看了1-2天的react的基础），因为是TS几乎没用过，所以可以说在边学习react的同时也在熟悉TS的使用过程。

不得不说习惯了用JS solo开发，使用TS开发是一件痛苦的事情，虽然如此但学到现在还是打算把TS用起来，工作14年有余，也应该走出自己的舒适圈来写点不一样的东西。

2023年对于我来说是一个变化的一年：
- 首先年初3月份接了一份荷兰的兼职工作，这份工作给了我很大的信心也让我在技术上有了更多想法。
- 其次对techui-vue2进行非常频繁的迭代，添加了非常多的新功能，并且修改了大量的不合理的命名，并且在此基础上发布了techui-vue3-lite免费版。
- 4月底首刷TS为了用AssemblyScript写WASM模块，最终因为AS语言非常不完善而放弃。
- 5月初开始学习rust基础，并在GPT的协助下开始了webassembly的开发。本月下旬完成了webassembly模块的开发，重写了techui-vue中的许可证逻辑，加解密，svg计算，自适应计算等功能。
- 6月初开始对techui-vue3-lite改造，同样采用wasm来做svg节点计算和自适应计算。
- 7月中旬开始构建一个techui-toolkit的工具库本在下旬发布，在这个工具库里面完成了一个陀螺仪3D面板组件和一个全新的简单的许可证逻辑。
- 8月份初开始学习React+TS，8月19日告一段落，同时可能要失去荷兰的兼职工作，是一个初创公司已经没太多事情可做。
- 8月下旬开始写techui-react-lite 动态SVG数据可视化框架

可以说2023年所学的知识和所做的事情，大大超出了我历年的工作学习成果，希望保持这样的势头，等techui-react-lite发布后，开始考虑学习python、nodejs等技术，转向全栈开发。知识越学越缺乏，永无止境。