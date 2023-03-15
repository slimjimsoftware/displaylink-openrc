# Maintainer: Simon Morgan <simonmorgan@slimjimsoftware.co.uk>

pkgname=displaylink-openrc
pkgver=1
pkgrel=0
pkgdesc="OpenRC files for starting displaylink"
arch=('any')
license=('custom' 'GPL2' 'LGPL2.1')
depends=('displaylink')
source=(
	rc-displaylink 
        displaylink-sleep.sh)
sha256sums=('fd71de688c773ad9ffe1bc7cd13910c85835d403e0f806d2257f27ba783b03d1'
            '8be4ab7616e38f91746bdd3e7fafe9004322a8be8e6722389746df9868d576e0')

package() {
  echo "Installing DLM openrc service"
  install -D -m755 rc-displaylink "$pkgdir/etc/init.d/dlm"
  install -D -m755 displaylink-sleep.sh "$pkgdir/etc/pm/sleep.d/displaylink.sh"
}
