# Maintainer: Yukari Chiba <i@0x7f.cc>

pkgname=hello
pkgver=2.12.1
pkgrel=2
pkgdesc="Prints Hello World and more"
arch=(x86_64 aarch64 riscv64 loongarch64)
url='https://www.gnu.org/software/hello/'
license=('GPL')
source=(https://ftp.gnu.org/gnu/hello/$pkgname-$pkgver.tar.gz)
sha256sums=('8d99142afd92576f30b0cd7cb42a8dc6809998bc5d607d88761f512e26c7db20')

build(){
  cd "$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}
package(){
  cd "$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
