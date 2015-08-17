# Maintainer: Ecmel Ercan <ecmel.ercan@gmail.com>
# Contributor: Sébastien Luttringer <seblu@aur.archlinux.org>

pkgname=vicious21
pkgver=2.1.0
pkgrel=2
pkgdesc='Widgets for the Awesome window manager'
arch=('any')
url='http://git.sysphere.org/vicious/about/'
license=('GPL2')
depends=('lua51')
conflicts=('vicious-git' 'vicious')
optdepends=(
  'hddtemp: for the HDD Temp widget type'
  'alsa-utils: for the Volume widget type'
  'wireless_tools: for the Wireless widget type'
  'curl: for widget types accessing network resources'
)
source=("http://git.sysphere.org/vicious/snapshot/vicious-$pkgver.tar.xz")
md5sums=('988bb423eafa6db951412f05cd237e31')

package() {
  cd vicious-$pkgver
  # Install the vicious library
  install -dm755 "$pkgdir"/usr/share/lua/5.1/vicious/{widgets,contrib}
  install -m644 *.lua "$pkgdir/usr/share/lua/5.1/vicious"
  install -m644 widgets/*.lua "$pkgdir/usr/share/lua/5.1/vicious/widgets"
  install -m644 contrib/*.lua "$pkgdir/usr/share/lua/5.1/vicious/contrib"
  # Install documentation
  install -dm755 "$pkgdir/usr/share/doc/vicious"
  install -m644 README CHANGES "$pkgdir/usr/share/doc/vicious"
}

# vim:set ts=2 sw=2 ft=sh et:

