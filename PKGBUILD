# Contributor: Andrea Scarpino <andrea@archlinux.org>
# Contributor: MeMi69  MetalMilitia at gmx dot net

pkgname=activitymanager-plasmoid
pkgver=0.5
pkgrel=2
pkgdesc="Lightweight plasmoid to manage your activities effectively"
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/Activity+Manager+Plasmoid?content=136278"
license=('LGPL')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4')
source=("http://kde-look.org/CONTENT/content-files/136278-activitymanager-$pkgver.tar.bz2")
md5sums=('7592bf60fafcb465fe75cd987a037ffc')

build() {
  cd $srcdir
  mkdir build
  cd build
  cmake ../activitymanager-${pkgver} \
    -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix`
  make
}

package() {
  cd ${srcdir}/build
  make DESTDIR="$pkgdir" install
}
