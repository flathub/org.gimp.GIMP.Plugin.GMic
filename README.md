GMIC plugin for GIMP
====================

It needs Qt6 (previously Qt5), so it needs to be built.

This make for most of the package size.

Some build trick:

Debug symbols still are not extracted from extensions. The strip build
option doesn't work because it strips the binaries (that we remove
later) that have hard links. Ensure writable doesn't help. So a
post-install is performing the strip.

Without strip, the package is around 500MB. With strip it's 55.4MB.

qt-tools are not necessary post build so the module is wholy cleaned
up.
