pkgname=bengal-wallpaper-kde
pkgver=1.1
pkgrel=1
pkgdesc='BengalBoot wallpapers for the Plasma Workspace'
arch=(any)
url='https://github.com/BCW52'
license=(LGPL)
makedepends=(extra-cmake-modules qt5-base)
groups=(bengal-de)
source=(bengal-wallpaper-kde::git+https://github.com/BCW52/bengal-wallpaper-kde.git)
sha256sums=('SKIP')
build() {
  cmake -B build -S $pkgname \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
