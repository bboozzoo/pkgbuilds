# Maintainer: Maciej Borzecki <maciek.borzecki@gmail.com
pkgname=image-garden
pkgver=0.1.1
pkgrel=1
pkgdesc="Tool for creating test virtual machines"
arch=(any)
url="https://gitlab.com/zygoon/image-garden"
license=('Apache-2.0')
groups=()
depends=('make' 'qemu-base' 'edk2-ovmf')
makedepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
source=("$pkgname-$pkgver.tar.bz2::https://gitlab.com/zygoon/${pkgname}/-/archive/v${pkgver}/image-garden-v${pkgver}.tar.bz2")
noextract=()
sha256sums=('e75ce3e9491b474425029787d8b4d456f593d23c62ca593673dfdd3f6bad1595')

prepare() {
	:
}

build() {
	cd "$pkgname-v$pkgver"
	make
}

check() {
	cd "$pkgname-v$pkgver"
	make check
}

package() {
	cd "$pkgname-v$pkgver"
	make DESTDIR="$pkgdir/" prefix=/usr install
}
