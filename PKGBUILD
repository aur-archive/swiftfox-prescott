# Maintainer: Dario Dax Vilardi <dax@deelab.org>
pkgname=swiftfox-prescott
pkgver=3.6.13
pkgrel=1
_pkgname=swiftfox
_pkgarch=prescott
pkgdesc="Swiftfox is a prebuilt version of Firefox3, optimized for Core Solo/Duo processors."
url="http://www.getswiftfox.com"
license=('custom')
arch=(i686)
conflicts=('swiftfox')
depends=('libxt' 'nss' 'sqlite3')
provides=(swiftfox=${pkgver})
source=(http://www.getswiftfox.com/builds/releases/$pkgver/$_pkgname-$pkgver-$_pkgarch.tar.bz2
        http://www.getswiftfox.com/LICENSE
        swiftfox.desktop
        swiftfox.png)
md5sums=('b5389e47a45e6abf9c1e9b98d08dcb6f'
         '7d2764ff8d5c9b0ba5be6028a3459e1d'
         '7b2bc5553bb2beaa8d49b4745bbc0c02'
         '92cb01c531a7ada40ca063b58d597de2')
		 
build() {
  mkdir $pkgdir/opt/
  cp -r $srcdir/swiftfox $pkgdir/opt/swiftfox
  mkdir -p $pkgdir/usr/bin
  ln -s /opt/$_pkgname/swiftfox $pkgdir/usr/bin/swiftfox
  install -D -m644 $srcdir/swiftfox.desktop $pkgdir/usr/share/applications/swiftfox.desktop
  install -D -m644 $srcdir/swiftfox.png $pkgdir/usr/share/pixmaps/swiftfox.png
  install -D -m644 -D $srcdir/LICENSE $pkgdir/usr/share/licenses/swiftfox/LICENSE
}
