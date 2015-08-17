# Maintainer: Viech <viech unvanquished net>

pkgname=q3chameleon-git
pkgver=v1.0.2.0.g79ad0db
pkgrel=1
pkgdesc="Texture replacement editor for the Quake 3 map format"
arch=("any")
url="http://www.unvanquished.net"
license=("GPL3")
depends=("python>=3.3" "python-pyqt4" "python-pillow")
source=("$pkgname::git+https://github.com/Unvanquished/Chameleon.git")
md5sums=('SKIP')

pkgver() {
	cd $srcdir/$pkgname
	local ver="$(git describe --long)"
	printf "%s" "${ver//-/.}"
}

package() {
	install -d $pkgdir/usr/bin
	install -m 755 $srcdir/$pkgname/chameleon.py $pkgdir/usr/bin/${pkgname/-git/}
}
