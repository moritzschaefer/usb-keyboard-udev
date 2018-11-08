# Maintainer: Moritz Schaefer <mail@moritzs.de>

pkgname=usb-keyboard-udev
pkgver=1
pkgrel=1
pkgdesc='Udev rules to run xmodmap after usb keyboard connected.'
arch=(any)
url='http://laurenceoflosangeles.blogspot.com/2015/08/configuring-udev-to-run-script-when-usb.html'
license=(GPL)
depends=(udev libusb)

source=(10-usb-keyboard.rules usb-keyboard-in usb-keyboard-in_udev udev_i_am_the_first)
sha256sums=('4be602a1f0893d4ac9c1a05dad61d9fac80287ff84cfbd66f5da0a9b8d56b6ab'
            '302c7dec954224b4b32226e93fadb9d62ac6d28a9635d944c4b3ed0537a8fba2'
            '4d3b39018339be2d5d077866a41a9e57f006a5c12e9153f177a2838f5a31fe18'
            '5ce43426259223e57671f8cda2e13542d3cd33e2723138740a0c6bcf34eb10b1'
)

package() {
  install -m755 -d "${pkgdir}/usr/lib/udev/rules.d"
  install -m755 -d "${pkgdir}/usr/bin"
  install -m644 "${srcdir}/10-usb-keyboard.rules" "${pkgdir}/usr/lib/udev/rules.d/"
  install -m755 "${srcdir}/udev_i_am_the_first" "${pkgdir}/usr/bin/"
  install -m755 "${srcdir}/usb-keyboard-in" "${pkgdir}/usr/bin/"
  install -m755 "${srcdir}/usb-keyboard-in_udev" "${pkgdir}/usr/bin/"
}
