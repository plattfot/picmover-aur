# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Fredrik Salomonsson <plattfot@gmail.com>
pkgname=picmover
pkgver=1.2.2
pkgrel=1
epoch=
pkgdesc="Image and video importer/organizer."
arch=('any')
url="https://github.com/plattfot/picmover"
license=('GPL3')
groups=()
depends=('python-gobject' 'libgexiv2')
makedepends=()
checkdepends=()
optdepends=('libnotify: notification support.')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=ChangeLog
source=("$pkgname-$pkgver::git+https://github.com/plattfot/picmover.git#tag=v$pkgver")
noextract=()
md5sums=('SKIP') #generate with 'makepkg -g'

# prepare() {
# 	cd "$srcdir/$pkgname-$pkgver"
# 	cd "doc"
# 	gzip picmover.*
# }

build() {
	cd "$pkgname-$pkgver"
	make
}

# check() {
# 	cd "$pkgname-$pkgver"
# 	make -k check
# }

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir/usr" install
}


