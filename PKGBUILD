# Contributor: ernest21 <ernest2193 at gmail dot com>
# Maintainer: ernest21 <ernest2193 at gmail dot com>



pkgname=circle-flat-icons-git
pkgver=0.r16.47525d2
pkgrel=1
pkgdesc="Circle-Flat is an icon theme for Linux desktops, the set is remix of Flattr-icons and Numix Circle."
arch=('any')
url='http://acutbal.deviantart.com/art/Circle-Flat-Icons-452501505'
license=('GPL3')
depends=('gnome-icon-theme' 'numix-icon-theme-git' 'flattr-icon-theme-git')
makedepends=('git')
provides=("${pkgname%-*}")
conflicts=("${pkgname%-*}")
options=('!strip')
install="${pkgname%-*}.install"
source=("git+https://github.com/ernest21/Circle-Flat-Icon.git")
sha256sums=('SKIP')
_gitname=("Circle-Flat-Icon")

pkgver() {
  cd ${_gitname}

  printf "0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd ${_gitname}

  install -dm 755 "$pkgdir"/usr/share/icons
  cp -dr --no-preserve='ownership' Circle-Flat "$pkgdir"/usr/share/icons/
}

# vim: ts=2 sw=2 et:
