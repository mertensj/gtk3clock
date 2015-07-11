# Maintainer: Jan Mertens <Jan.JM.Mertens at gmail dot com>

pkgname=aclock-git
pkgver=20150712
pkgrel=1
pkgdesc="Analog clock written in GTK3."
arch=('i686' 'x86_64')
url="http://github.com/mertensj/aclock"
license=('BSD')
depends=()
source=("git+https://git@github.com/mertensj/aclock.git")
md5sums=("SKIP")

_gitname="aclock"

pkgver() {
  cd "$srcdir/${_gitname}"
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

build() {
  cd "$srcdir/$_gitname"
  make
}

package() {
  cd "$srcdir/$_gitname"
  install -Dm 755 $_gitname "$pkgdir/usr/bin/$_gitname"
} 
