# Maintainer: Nuno Araujo <nuno.araujo@russo79.com>
pkgname=libg15-gnome15
_pkgname=libg15
pkgver=1.3.0.3
pkgrel=2
pkgdesc="Modified version of lib15 for compatibility with gnome15"
arch=('i686' 'x86_64')
url="http://www.russo79.com/gnome15"
license=('GPL')
depends=('libusb-compat')
provides=('libg15')
conflicts=('libg15')
install=$pkgname.install
source=("https://projects.russo79.com/attachments/download/74/$pkgname-$pkgver.tar.gz")
md5sums=('48d8473b44c0a59f41e9ed118f3e1f5f')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

check() {
  cd "$srcdir/$pkgname-$pkgver"
  make -k check
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
