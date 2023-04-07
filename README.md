## retrier.sh

~~~~
🦔 tool for retry works on shell.
~~~~

### install

Two way:

- copy the context of one `source` file, and write them into `~/bin/retrier` .
- or change the last line `exec retrier "$@"` to `:;`, then write the context into `/etc/profile.d/retrier.sh`, then run `exec $SHELL`.

### demo

~~~ sh
ENV='WORKS () { sleep 3 ; cd $RETRIED ; }' retrier WORKS
~~~

### desc (zh)

它能对指定的命令自动失败时重试。

这是个知识总结性质的，
但也经过了一定生产上的测试（以及相应的改进）。

它基于 SHell 编写，
用到了元编程来简化重复代码、
以及我自己的模块化方案来组织代码。
 Bash 版本还使用了有 TCO 的 Tail Call ，
用以不依靠关键字地完成迭代功能。
