# Maintainer: Archlatam <corelinuxx@mail>
#

pkgname=core-settings-kde
pkgver=r0.0000000
pkgrel=1
pkgdesc="Configuración base de KDE de Arch Latam (instalada en /etc/skel)"
arch=('any')
url="https://github.com/archlatam/core-settings-kde"
license=('GPL-3.0-only')
depends=('plasma-desktop')

optdepends=('dolphin: configuración de dolphinrc'
  'konsole: perfiles y esquema de colores de Konsole'
  'fastfetch: config.jsonc para fastfetch')
makedepends=('git')

provides=("${pkgname%-git}")
conflicts=("${pkgname%-git}")
source=("${pkgname%-git}::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/${pkgname%-git}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/${pkgname%-git}"

  install -d "$pkgdir/etc"
  cp -a --no-preserve=ownership src/etc/skel "$pkgdir/etc/"

  # Permisos normalizados
  find "$pkgdir/etc/skel" -type d -exec chmod 755 {} +
  find "$pkgdir/etc/skel" -type f -exec chmod 644 {} +
}
