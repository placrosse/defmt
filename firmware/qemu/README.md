# `firmware`

Firmware configured to run on QEMU to try out defmt end-to-end (encoder + decoder + singleton) on an emulated microcontroller

## dependencies
- [qemu](https://www.qemu.org/download/)

## running

Run the examples with:

``` console
$ cargo run --target thumbv7m-none-eabi --bin log
(...)
0.000000 INFO Hello!
0.000001 INFO World!
0.000002 INFO The answer is 42
0.000003 TRACE log trace
0.000004 DEBUG log debug
0.000005 INFO log info
0.000006 WARN log warn
0.000007 ERROR log error
0.000008 INFO S { x: 1, y: 256 }
0.000009 INFO X { y: Y { z: 42 } }
```

or
``` console
$ cargo run --target thumbv7m-none-eabi --release --bin log
(...)
0.000000 INFO Hello!
0.000001 INFO World!
0.000002 INFO The answer is 42
0.000003 INFO log info
0.000004 WARN log warn
0.000005 ERROR log error
0.000006 INFO S { x: 1, y: 256 }
0.000007 INFO X { y: Y { z: 42 } }
```

Note the difference in log levels for debug and release; for details see the [Logging level filtering](../README.md#logging-level-filtering) documentation.
