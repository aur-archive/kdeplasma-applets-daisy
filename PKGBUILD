# Maintainer: t3ddy <t3ddy1988 "at" gmail {dot} com>
# Contributor: Bram Schoenmakers <me@bramschoenmakers.nl>
# Contributor: Jan Tylich (Kurt) <jan.tylich (at) gmail.com>

pkgname=kdeplasma-applets-daisy
pkgver=0.0.4.26
pkgrel=2
pkgdesc="A simple application launcher for Plasma."
arch=('i686' 'x86_64')
url="http://cdlszm.org/"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('gcc' 'cmake' 'automoc4')
replaces=('plasma-daisy-plasmoid')
install=daisy.install
source=("http://cdlszm.org/downloads/plasma-applet-daisy-$pkgver.tar.gz")
md5sums=('43c1ae617a0216e0780187db8e628cdf')

build() {
  cd $srcdir/plasma-applet-daisy-${pkgver}
  
  mkdir build && cd build
  
  cmake -DCMAKE_INSTALL_PREFIX=/usr ..
  make
}

package() {
  cd $srcdir/plasma-applet-daisy-${pkgver}/build

  make DESTDIR="$pkgdir/" install
}
