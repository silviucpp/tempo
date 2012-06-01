

#tempo#


__Authors:__ Dmitry Groshev ([`groshev@selectel.ru`](mailto:groshev@selectel.ru)), Sergei Levedev ([`lebedev@selectel.ru`](mailto:lebedev@selectel.ru)).


`tempo` is a library for parsing and formatting dates in
Erlang. It provides a clean and nice interface to libc's
[strptime](http://linux.die.net/man/3/strptime) and
[strftime](http://linux.die.net/man/3/strftime) functions,
which, are unfortunately missing in Erlang's standard library.

###<a name="Is_it_any_good?">Is it any good?</a>##



Yes.

###<a name="How_can_I_use_it?">How can I use it?</a>##


The only two functions you have to remember is [`tempo:parse/2`](https://github.com/selectel/tempo/blob/master/doc/tempo.md#parse-2)
and [`tempo:format/2`](https://github.com/selectel/tempo/blob/master/doc/tempo.md#format-2), here're some examples:<pre>(tempo_dev@localhost)1> {ok, Bin} = tempo:format(iso8601, {now, now()}).
{ok,<<"2012-06-01T19:06:420000">>}
(tempo_dev@localhost)2> tempo:parse(iso8601, {datetime, Bin}).
{ok,{{2012,6,1},{19,6,42}}}</pre>


##Modules##


<table width="100%" border="0" summary="list of modules">
<tr><td><a href="https://github.com/selectel/tempo/blob/master/doc/tempo.md" class="module">tempo</a></td></tr></table>

