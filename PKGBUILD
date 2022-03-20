pkgname=bengal-wallpaper-kde
pkgver=5.24.2
pkgrel=1
pkgdesc='Additional wallpapers for the Plasma Workspace'
arch=(any)
url='https://github.com/BCW52'
license=(LGPL)
makedepends=(extra-cmake-modules qt5-base)
groups=(plasma)
source=(https://github.com/BCW52/bengal-wallpaper-kde/archive/refs/heads/main.zip)
sha256sums=('c4037525a75f1ebd6749c9eea6572eac6917dd68e8f2aabeb587047759cdff41')
build() {
  cmake -B build -S $pkgname-main \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
