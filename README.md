archbootstrap
=============

Let's bootstrap Arch Linux from BASH:

	$ curl -\# https://mirrors.kernel.org/archlinux/iso/latest/archlinux-bootstrap-$(date +%Y.%m.01)-$(uname -m).tar.gz | tar xz --strip-components 1 -C '/path/to/install/directory'

Wait, hold on. Hold on a second.

Yep, you can actually bootstrap one of the world's largest distros with a oneliner.

![Holy Shit!](media/jg8ZYsmN3ywJq.gif)

-------------

Alternatively, you can use `archbootstrap`:

	$ archbootstrap ./arch
	# archbootstrap /var/lib/machines/arch

`archbootstrap` will cache downloaded files in `$XDG_CACHE_HOME` or `$HOME/.cache` if run as a user, and in `/var/cache` if run as root.

`archbootstrap` supports some options:

	$ archbootstrap -h
	usage:	archbootstrap [options] root

		-a <arch>
		-c <cachedir>
		-h help
		-i show post-install ideas
		-m <mirror>
		-n no-cache
