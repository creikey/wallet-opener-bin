# Maintainer: Cameron Reikes <cameronreikes@gmail.com>
pkgname=wallet-opener
pkgver=1
pkgrel=1
pkgdesc="Small application that requests to open the kde wallet"
arch=('i686' 'x86_64')
url="https://github.com/creikey/wallet-opener"
license=('MIT')
groups=()
depends=('kwallet')
makedepends=('qt5-base')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=$pkgname.install
source=("https://github.com/creikey/$pkgname/archive/master.tar.gz")
md5sums=('ce4025675d5565b522db93b5b9804c4e')

prepare() {
    mv "$pkgname-master" "$pkgname-$pkgver"
}

build() {
	cd "$srcdir/$pkgname-$pkgver"
    qmake $pkgname.pro
    make
}

check() {
	cd "$srcdir/$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
    install -D -m755 $pkgname.out "$pkgdir/usr/bin/$pkgname"
}
