# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# See http://wiki.archlinux.org/index.php/VCS_PKGBUILD_Guidelines
# for more information on packaging from CVS sources.

# Maintainer: Debian Chinese Team <chinese-developers@lists.alioth.debian.org>
pkgname=fortune-zh
pkgver=2.0
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
source=("http://github.com/jack-lijing/fortune-zh/archive/master.zip")
sha1sums=('8df11f37348e93584d57abfe38bfe962338544fd')

build() {
  cd "$srcdir"
  msg "Connecting to Server"
  unzip master.zip
#  tar xvf ${pkgname}_${pkgver}.tar.gz
#  cd "$srcdir/${pkgname}-${pkgver}"
  cd "$srcdir/fortune-zh-master"
  make all
}

package() {
  cd "$srcdir/fortune-zh-master"
  make "DESTDIR=$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
