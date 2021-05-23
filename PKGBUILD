pkgname=par2cmdline
pkgver=0.8.1
pkgrel=1
pkgdesc='A PAR 2.0 compatible file verification and repair tool'
url='https://github.com/BlackIkeEagle/par2cmdline'
license=('GPL2')
arch=('x86_64')
source=("$pkgname-$pkgver.tar.gz::https://github.com/BlackIkeEagle/$pkgname/archive/v$pkgver.tar.gz")
sha512sums=('d8a49ae7688c9833278e7c2c666855f92f91850adc700f5e5bb2afc01c508dc50a389b822e3cf120ed6c950bb98854724c8d84b9173dd4452f8216105a42145c')

build() {
    cd ${pkgname}-${pkgver}
    aclocal
    automake --add-missing
    autoconf
    ./configure --prefix=/usr
    make
}

# check() {
#     cd ${pkgname}-${pkgver}
#     make check
# }

package() {
	cd ${pkgname}-${pkgver}
	make DESTDIR="${pkgdir}" install
}
