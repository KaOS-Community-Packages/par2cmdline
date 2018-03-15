pkgname=par2cmdline
pkgver=0.8.0
pkgrel=1
pkgdesc='A PAR 2.0 compatible file verification and repair tool'
url='https://github.com/BlackIkeEagle/par2cmdline'
license=('GPL2')
arch=('x86_64')
source=("$pkgname-$pkgver.tar.gz::https://github.com/BlackIkeEagle/$pkgname/archive/v$pkgver.tar.gz")
sha512sums=('7dc19d18d375c1ec62f438613fec0008515e325a1387feb9c9f92d84b5bfa955911459147732ead4c20ce7e77dc6d7d22da5b388fb572026aa431b28252b5fcf')

build() {
	cd "$pkgname-$pkgver"
	aclocal
	automake --add-missing
	autoconf
	./configure --prefix=/usr
  make
}

check() {
	cd "$pkgname-$pkgver"
	make check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir" install
}
