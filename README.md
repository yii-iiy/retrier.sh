### retrier.sh

🦔 tool for retry works on shell.

#### install

Two way:

- copy the context of one `source` file, and write them into `~/bin/retrier` .
- or change the last line `exec retrier "$@"` to `:;`, then write the context into `/etc/profile.d/retrier.sh`, then run `exec $SHELL`.

#### demo

~~~ sh
ENV='WORKS () { sleep 3 ; cd $RETRIED ; }' retrier WORKS
~~~
