# Composing Programs Notes

This is a repository where I take notes of [Composing Programs](http://www.composingprograms.com).

## Chapter 1 Comment

第一章整体来说写得还是非常好的。

在 1.1 节中，我认识了 statement 和 expression 两个至关重要的概念。statement 表示的是一种动作和变化；而 expression 表示的是 value，可以通过 evaluation 得到。值得注意的是，Python 中的 code 就是由一系列的 statement 组成的，expression 是各种 statement 的组成部分。可以说，statement 和 expression 是构建整个 program 的基石。

计算机方面的术语我以前都是用中文学的，statement 应该叫「语句」，而 expression 应该叫「表达式」，但是我总有种雾里看花的感觉，不明白天天看到的这两个单词到底有什么区别和联系。而在仔细学习了这两个概念后，我则有种豁然开朗的感觉。

然后，1.2 节中又介绍了 primitive expression 和 compound expression。顾名思义，primitive expression 就是组成 compound expression 的成分。那什么是 compound expression 呢？直观地说，函数调用就是 compound expression， 而且这个函数调用有两种形式：infix notation 和 function notation。infix notation 就是像 `1 + 2` 这样的 expression，function notation 就是像 `add(1, 2)` 这样的 expression。

在这里，两种看似风马牛不相及的事物又一次被联系了起来。当时我看到这里的时候也直呼神奇，原来像 `1 + 2` 这种简单的式子和 `add(1, 2)` 表达的是一个意思。

接下来，我又接触到 name、binding。name 表示的只是一个名字，而这个名字可以和任何 value 之间存在 binding。这里的 value 不是狭义的 value，它包括 data 和 function。所以 name 不仅可以指向 data，还可以指向 function。指向 data 的 name 在中文里面叫「变量名」，而指向 function 的 name 在中文里面叫「函数名」。两者并非割裂的状态，在 Python 这种 function 拥有 first-class status 的语言中其实就是一个东西。「first-class status」下面会讲到。

然后是 assignment statement，它的主要作用就是建立 binding。比较特殊的是，Python 中还有 multiple assignment。

接着，书中又介绍了 environment，environment 就是 interpreter 存放 binding 的地方，对 expression 的 evaluation 有至关重要的作用。

1.2 节最后介绍了 pure function 和 non-pure function 的函数分类方法。这也是我之前没有听说过的。

1.3 节首先介绍的是如何定义一个新的函数，比较常规。然后就是重头戏 environment diagram 了。environment diagram 就是 expression evaluation 的 visualization。environment diagram 由两种 frame 构成：global frame 和 local frame。借着 local name，书中又提出了 scope 的概念。

1.4 节则讨论了一些对 function 而言比较重要的概念，比如如何写好一个 function 以及 documentation。最后提到了 function 的 default argument。

1.5 节又是重头戏。expression 前面讲了很多，而 1.5 节则展开讲解了 statement。1.5 节先是引入了 simple statement 和 compound statement 的概念，然后介绍了两种 compound statement：conditional statement 和 iteration statement。最后是如何对 function 进行测试，书中介绍了 `assert` 和 doctest 两种办法。

1.6 节开始介绍 higher-order function。说实话，看到这里以后，我已经有种要成仙的感觉了。higher-order function 作为 first-class status 的产物，和正常的 function 用法完全不同。higher-order function 主要涉及：将 function 作为 argument；nested function（nested function 中介绍了 lexical scope 和 closure，closure 好像是 functional programming 比较重要的一个概念）；将 function 作为 return value；currying（我觉得最骚的还是 currying）；lambda function。然后，书中介绍了 first-class status，这个概念非常重要，并且在 Python function 的概念和使用中充分得到了体现。1.6 节最后介绍了 function decorator。

1.7 节介绍了 recursive function，我觉得最重要的就是 recursive leap of faith 这个概念。
