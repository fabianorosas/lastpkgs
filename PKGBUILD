# Maintainer: Fabiano Rosas <fabianorosas@gmail.com>
pkgname=lastpkgs-git
pkgver=0.0.0
pkgrel=1
pkgdesc="Lists or removes packages from the last N reboots. Good for cleaning up after experimenting with new programs."
arch=('any')
url="https://github.com/fabianorosas/lastpkgs"
license=('GPL')
makedepends=('git')
conflicts=('lastpkgs')
provides=('lastpkgs')
source=("$pkgname"::'git+https://github.com/fabianorosas/lastpkgs.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  git describe --long | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "$srcdir/$pkgname"
  install -Dm755 lastpkgs $pkgdir/usr/bin/rm-recent-pkgs
}

