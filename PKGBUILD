# Maintainer: Richard Wiedenhöft <richard.wiedenhoeft@gmail.com>
pkgname=neutron-git
pkgver=253.9c9f63e
pkgrel=1
pkgdesc="A web-development-library written in vala"
url="http://github.com/Richard-W/neutron"
arch=('x86_64' 'i686')
license=('AGPL3')
depends=('libgee')
makedepends=('cmake' 'vala' 'git')
source=("git://github.com/Richard-W/neutron")
md5sums=('SKIP')

pkgver() {
	cd neutron
	echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

build() {
	cd neutron
	./configure --prefix=/usr
	make
}

package() {
	cd neutron
	make DESTDIR="${pkgdir}" install
}
