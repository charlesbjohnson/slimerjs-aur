# Maintainer: L42y <423300@gmail.com>
# Contributor: cbjohnson <mail@cbjohnson.info>
pkgname=slimerjs
pkgver=0.9.2
pkgrel=1
pkgdesc="A PhantomJS-like tool running Gecko"
arch=(i686 x86_64)
url="http://slimerjs.org/"
license=('MPL2')
depends=(xulrunner)
optdepends=('xorg-server-xvfb: run slimerjs without the need of an X-Windows environment')
source=(http://download.$pkgname.org/releases/$pkgver/$pkgname-$pkgver.zip)
md5sums=('b359c89029b9b8a2fc4eddbea6a16f6d')

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm644 application.ini $pkgdir/usr/lib/$pkgname/application.ini
  install -Dm644 omni.ja $pkgdir/usr/lib/$pkgname/omni.ja
  install -Dm755 $pkgname $pkgdir/usr/lib/$pkgname/$pkgname
  install -Dm644 LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE

  install -d $pkgdir/usr/bin
  ln -s /usr/lib/$pkgname/$pkgname $pkgdir/usr/bin/$pkgname
}
