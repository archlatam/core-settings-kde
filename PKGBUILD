# Maintainer: Core GNU/linux <corelinuxx@gmail.com>

pkgname=core-settings-kde
pkgver=1.0
pkgrel=1
pkgdesc="Core settings configuration for KDE Plasma live session"
arch=('any')
url="https://github.com/archlatam/core-settings-kde"
license=('GPL3')
depends=()
source=("git+https://github.com/archlatam/core-settings-kde.git")
sha256sums=('SKIP')

package() {
  install -dm755 "${pkgdir}/etc/skel"
  cp -a "${srcdir}/core-skel-kde/src/etc/skel/." "${pkgdir}/etc/skel/"
}
