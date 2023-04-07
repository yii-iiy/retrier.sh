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

它基于 SHell 编写，能对指定的命令自动失败时重试。

依靠元编程简化了重复代码；依靠子命令打包代码； Bash 版依靠 TCO 的 Tail Call 完成不依赖关键字的迭代。
