# Maintainer: Your Name <youremail@domain.com>
pkgname=projman-git 
pkgver=r4.77567d1
pkgrel=1
pkgdesc="A simple tui project manager"
arch=(x86_64)
url="https://github.com/delta1024/projman"
license=('none')
makedepends=('git' 'go') # 'bzr', 'git', 'mercurial' or 'subversion'
provides=("${pkgname%-git}")
conflicts=("${pkgname%-git}")
options=(!debug)
source=('git+https://github.com/delta1024/projman')
sha256sums=('SKIP')


pkgver() {
	cd "$srcdir/${pkgname%-git}"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

prepare() {
	cd "$srcdir/${pkgname%-git}"
}

build() {
	cd "$srcdir/${pkgname%-git}"
	go build
}

check() {
	cd "$srcdir/${pkgname%-git}"
}

package() {
	cd "$srcdir/${pkgname%-git}"
	install -Dm755 ${pkgname%-git} "$pkgdir/usr/bin/${pkgname%-git}" 
}
