# Contributor: Michael Krauss <michael.krauss@gmx.de>
# Contributor : LeCrayonVert
pkgname=xpn
pkgver=1.2.6
pkgrel=7
arch=('any')
pkgdesc="pygtk based newsreader"
url="http://xpn.altervista.org/index-en.html"
license="GPL"
depends=('python2>=2.4' 'gtk2>=2.8' 'pygtk>=2.8')
source=(http://xpn.altervista.org/codice/$pkgname-$pkgver.tar.gz
	xpn.sh
	xpn.desktop)

package() {
  mkdir -p $pkgdir/usr/lib
  mkdir -p $pkgdir/usr/share/pixmaps
  mkdir -p $pkgdir/usr/share/applications
  mv $startdir/src/$pkgname-$pkgver $pkgdir/usr/lib/$pkgname
  chmod -R 755 $pkgdir/usr/lib/$pkgname
  mkdir -p $pkgdir/usr/bin/
  install --mode=755 ../xpn.sh $pkgdir/usr/lib/$pkgname
  cp ../xpn.desktop $pkgdir/usr/share/applications
  cp $pkgdir/usr/lib/$pkgname/pixmaps/xpn-icon.png \
	$pkgdir/usr/share/pixmaps
  ln -s /usr/lib/$pkgname/xpn.sh $pkgdir/usr/bin/xpn
}

md5sums=('6b77345290a27406e411ea0ffa54780f'
         '5d10d37b5d41cf36c7be30e35be694b5'
         '136be80b4e22ebf3123cd0edc98bc240')
sha512sums=('dab4d96951757e881aac92c791e64f92eb86ac54a57c285c34a45ae3b83955e9c4f23b7c62a511675264604d1485107e979195e95f00964bbdbbce4481780d00'
            'd5a56f3cda4fcbb33c4cda85489dd6812bd071a4dc92f168f7ca685c03e1608e979044d2a8bfb8bd3feab8033d9505bcd6d19ae088a618090a63e6914991583b'
            'c2036237c1fad55632eb777f824a68ef21a20a0faf74c7e86029b2ddb2a3580860ae5bfd60ccc7578a15a9938c5a75ab88541fbc477673024d0c3d472d4c5b08')
