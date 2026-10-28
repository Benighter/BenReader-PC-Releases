# libmobi 0.12 corresponding source

Each Windows release provides the original upstream `libmobi-0.12.tar.gz`, original licence notices and this build recipe. The separate `mobitool.exe` is LGPL-3.0-or-later. Its original source is https://github.com/bfabiszewski/libmobi/tree/v0.12.

With Windows x64 GCC, compile from the extracted source directory:

```text
gcc -O2 -s -std=gnu99 -DHAVE_GETOPT -DUSE_XMLWRITER -DUSE_MINIZ -DMINIZ_NO_ZLIB_COMPATIBLE_NAMES -I src -I tools src/buffer.c src/compression.c src/debug.c src/index.c src/memory.c src/meta.c src/parse_rawml.c src/read.c src/structure.c src/util.c src/write.c src/opf.c src/xmlwriter.c src/miniz.c tools/common.c tools/mobitool.c -o mobitool.exe
```

Optional encryption support is disabled. BenReader calls this separate executable to convert supported unprotected editions into EPUB. Users may rebuild it and replace the copy in the installed `current/native` folder under the component's original licence.
