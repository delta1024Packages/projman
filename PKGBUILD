# Maintainer: Your Name <youremail@domain.com>
pkgname=projman 
pkgver=0.1.0
pkgrel=1
pkgdesc="A simple tui project manager"
arch=(x86_64)
url="https://github.com/delta1024/projman"
license=('none')
makedepends=('git' 'go') # 'bzr', 'git', 'mercurial' or 'subversion'
provides=("${pkgname}")
conflicts=("${pkgname}")
replaces=("${pkgname}-git")
options=(!debug)
source=("https://github.com/delta1024/${pkgname}/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('SKIP')


prepare() {
	cd "${pkgname}-${pkgver}"
}

build() {
	cd "${pkgname}-${pkgver}"
	go build
}

check() {
	cd "${pkgname}-${pkgver}"
}

package() {
	cd "${pkgname}-${pkgver}"
	install -Dm755 ${pkgname} "$pkgdir/usr/bin/${pkgname}" 
}
