# Maintainer: Fabiano Rosas <fabianorosas@gmail.com>
pkgname=session-packages-git
pkgver=0.0.0
pkgrel=1
pkgdesc="Lists and removes packages installed during the current session. Good for moments of package-installing frenzy."
arch=('any')
url="https://github.com/fabianorosas/session-packages"
license=('GPL')
makedepends=('git')
conflicts=('session-packages')
provides=('session-packages')
source=("$pkgname"::'git+https://github.com/fabianorosas/session-packages.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  git describe --long | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "$srcdir/$pkgname"
  install -Dm755 session-packages $pkgdir/usr/bin/session-packages
}

