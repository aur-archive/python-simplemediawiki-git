# Maintainer: Jakub Klinkovský <j.l.k@gmx.com>

_pkgname=python-simplemediawiki
pkgname=python-simplemediawiki-git
pkgdesc="Extremely low-level wrapper to the MediaWiki API"
pkgver=1.2.0b2.2.g05ed3d2
pkgrel=1
arch=('any')
url="https://github.com/ianweller/python-simplemediawiki"
license=('LGPL')
depends=('python')
makedepends=('git')
source=('git://github.com/ianweller/python-simplemediawiki.git#branch=release/1.2.0')
md5sums=('SKIP')

pkgver() {
  cd "$_pkgname"
  git describe --tags --always | sed 's|-|.|g'
}

package() {
  cd "$_pkgname"
  python setup.py install --prefix=/usr --root="$pkgdir" --optimize=1
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

# vim:set ts=2 sw=2 et:
