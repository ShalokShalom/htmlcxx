pkgname=htmlcxx
pkgver=0.86
pkgrel=1
pkgdesc="A simple non-validating CSS1 and HTML parser for C++."
arch=('x86_64')
url="http://htmlcxx.sourceforge.net/"
license=('LGPL')
source=("https://sourceforge.net/projects/${pkgname}/files/${pkgname}/${pkgver}/${pkgname}-${pkgver}.tar.gz/download")
sha256sums=('07542b5ea2442143b125ba213b6823ff4a23fff352ecdd84bbebe1d154f4f5c1')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	
	LDFLAGS="$LDFLAGS -Wl,--no-as-needed"
	./configure --prefix=/usr
	make
}

package() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	make DESTDIR="${pkgdir}" install
} 
