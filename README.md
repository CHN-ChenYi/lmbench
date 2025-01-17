# Prerequisite

* libtirpc(https://sourceforge.net/projects/libtirpc/)

```sh
CC=riscv64-unknown-linux-gnu-gcc
SYSROOT=`${CC} -print-sysroot`
./configure --host=${CC} --prefix=${SYSROOT}/usr --disable-gssapi
make
make install
```

# README

README for lmbench 2alpha8 net release.

To run the benchmark, you should be able to say:

	cd src
	make results

If you want to see how you did compared to the other system results
included here, say

	make see

Be warned that many of these benchmarks are sensitive to other things
being run on the system, mainly from CPU cache and CPU cycle effects.
So make sure your screen saver is not running, etc.

It's a good idea to do several runs and compare the output like so

	make results
	make rerun
	make rerun
	make rerun
	cd Results && make LIST=<your OS>/*
