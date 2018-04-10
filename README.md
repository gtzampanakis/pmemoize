# pmemoize
Python memoizer with optional persistence to disk

Yet another memoizer. I have been using this for a long time. It is simple but
useful. Features:

* Optional persistence to disk, using pickle to save the cache on exit.
* Configurable cache size. When it is reached a FIFO strategy is used to
  discard old entries.
* Stats tracking. Allows to see if memoization is useful for a certain function
  call.

## Usage

Simply decorate your function:

    import pmemoize
    @pmemoize.MemoizedFunction
    def add(x, y):
        return x+y

    add(5, 3)
