# 代码块

    Block = "{" StatementList "}" .
    StatementList = { Statement ";" } .

- 代码块有可能为空
- 源码中除了显式的块,还有隐式的:
    - 在go源码文本之外还有一个块,这个块包含了源码中所有的块,这个块叫universe,宇宙
    - 每一个package都有一个块,用于包含这个包中的go源码文本
    - 每一个文件还有一个文件块,包含了本文件中的go源码文本
    - if for switch 都有自己隐式的块
    - switch select每个分支,都被看作是一个隐式块
- 块都是可嵌套的
- 显示块就很简单:大括号包着的就是

```golang
type struct abc {
    a,b int
    c,d string
}
```
