[Oberon Microsystems](http://www.oberon.ch/) [BlackBox Component Builder](http://www.oberon.ch/blackbox.html)

Port for OpenBSD/i386, GNU/Linux/i386, FreeBSD/i386

Some significant parts taken from [OpenBUGS](http://www.openbugs.info/)

Tested on:
* OpenBSD 5.2
* Fedora Core 17
* Ubuntu 12.04 LTS, 12.10
* FreeBSD 9.0

Status: stable, but [TODO](BlackBox/blob/master/TODO) list is not empty

How to build:

	cd BlackBox
	./clean
	./switch-target `uname -s`

	compile loader executable:
		cd BlackBox/Lin/Rsrc/loader
		make clean
		make
		mv loader ../../../_`uname -s`_/Lin/Rsrc/loader/

	compile self:
		cd BlackBox
		./build
		./pack-dev0

Alexander V. Shiryaev, 2012
