# fck-curl

A simple server that shows that piping directly
into CURL might not be all that great of an idea.

It's one of the more harmless ways to break your system.

## Installation

You will need [lang-server](https://github.com/hellerve/lang-server).

```
zeps install hellerve/fck-curl
```

But you don't really want to use it, do you?

## Rationale

CURL normally tells the server that the request is sent
by it (through the `User-Agent` header). This tool is
a simple exploit that showcases how you can effortlessly
write a server that will serve harmless content as long
as you request it from any browser or other tool. As soon
as CURL enters the game, though, things get mischievous
and your system is at risk.

## Usage

```
zepto-serve fck-curl/fck-curl
```

Now try to access it from the browser of your choice, then
from CURL. If you try piping it into CURL, you might want
to create a temporary directory and `cd` into it.

<hr/>

Have fun!
