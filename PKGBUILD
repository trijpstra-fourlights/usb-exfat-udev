# Maintainer: Thomas Rijpstra <thomas at fourlights dot nl>
pkgname=usb-exfat-udev
pkgver=1.0.0
pkgrel=1
pkgdesc="Udev rule to limit cache size using max_bytes for USB exFAT drives"
arch=('any')
url="git@github.com:trijpstra-fourlights/usb-exfat-udev.git"
license=('MIT')
depends=('udev')
backup=('usr/lib/udev/rules.d/99-usb-exfat.rules')
source=("99-usb-exfat.rules")

package() {
    install -Dm644 "$srcdir/99-usb-exfat.rules" "$pkgdir/usr/lib/udev/rules.d/99-usb-exfat.rules"
}

post_install() {
    udevadm control --reload
}

post_upgrade() {
    post_install
}

sha256sums=('41803bff959c962f6dfeeee716ae8be21a8fe65e4fc231b53d3e21f161645b65')
