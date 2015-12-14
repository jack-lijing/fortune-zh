# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# See http://wiki.archlinux.org/index.php/VCS_PKGBUILD_Guidelines
# for more information on packaging from CVS sources.

# Maintainer: Debian Chinese Team <chinese-developers@lists.alioth.debian.org>
pkgname=fortune-zh
pkgver=1.9
pkgrel=1
pkgdesc=" This software package contains the Chinese data files for fortune in utf8 encoding.  Those libraries included tang300 -- 300_Tang_Poems and other Chinese classical poetry"
arch=('any')
url="http://anonscm.debian.org/gitweb/?p=chinese/fortune-zh.git"
license=('GPL')
groups=()
depends=('fortune-mod' 'zh-autoconvert')
makedepends=('fortune-mod' 'zh-autoconvert')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
source=("http://http.debian.net/debian/pool/main/f/fortune-zh/fortune-zh_1.9.tar.gz")
sha1sums=('dabc9b495fca75584ae52041187d93da1e6c44df')

build() {
  cd "$srcdir"
  msg "Connecting to Server"
  tar xvf ${pkgname}_${pkgver}.tar.gz
  cd "$srcdir/${pkgname}-${pkgver}"
  make all
}

package() {
  cd "$srcdir/${pkgname}-${pkgver}"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
