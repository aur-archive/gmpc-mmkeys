# Maintainer: Limao Luo <luolimao+AUR@gmail.com>
# Contributor: Christian Brassat <christian@crshd.cc>

pkgname=gmpc-mmkeys
pkgver=11.8.16
pkgrel=1
pkgdesc="Control GMPC with the special keys on a multimedia-keyboard"
arch=(i686 x86_64)
url=http://sarine.nl/gmpc
license=(GPL3)
depends=(dbus-glib gmpc)
options=(!libtool)
source=(http://download.sarine.nl/Programs/gmpc/$pkgver/$pkgname-$pkgver.tar.gz)
sha256sums=('708a0ca30a424b8dacfe574bdcf18c147f9a3be7366faa2466525cf7b5936f2f')
sha512sums=('d7cc1f9ae8b4556e7573495cc4a08476aa6a8222a020f59549d3fb4b89f92c910f172c26aed72be9e8a463783e54348781537bf9dfe8b637bdf6b5a3787b033e')

build() {
    cd $pkgname-$pkgver/
    ./configure --prefix=/usr
    make
}

package() {
    make -C $pkgname-$pkgver DESTDIR="$pkgdir" install
}
