
pkgname=magicseteditor-mtg-m15
pkgver=20140808
pkgrel=3
pkgdesc="Magic Set Editor templates for Magic: The Gathering M15 redesign"
arch=(any)
url="http://msetemps.sourceforge.net/phpBB3/viewtopic.php?t=144"
license=('freeware')
depends=('magicseteditor-mtg-base')
conflicts=("")
source=("http://downloads.sourceforge.net/msetemps/Magic - Printed M15 Styles.mse-installer"
        "http://downloads.sourceforge.net/msetemps/Magic - Custom M15 Styles.mse-installer")
md5sums=('1b6c534b5845322ff6f841a8a7d65af9'
         '18cbc0674f9f400d92d4d57899b2d235')

package() {
  install -d $pkgdir/usr/share/magicseteditor/data

  cd $srcdir
  find magic-m15* -name '*.png' -type f -exec mogrify {} \;
  cp -r magic-m15* $pkgdir/usr/share/magicseteditor/data
  chmod 755 $pkgdir/usr/share/magicseteditor/data/*
}
