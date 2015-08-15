# Maintainer: Cedric MATHIEU <me.xenom @ gmail.com>
# Contributor : Det <nimetonmaili @ gmail.com>
# Contributor: coderoar <coderoar @ gmail.com>

pkgname=firefox-nightly-symbols
pkgdesc='Debug symbols for firefox nightly'
url='http://www.mozilla.org/projects/firefox'
pkgver=21.0a1
pkgrel=1
arch=('i686' 'x86_64')
license=('MPL' 'GPL' 'LGPL')
source=('http://hg.mozilla.org/users/jwatt_jwatt.org/fetch-symbols/raw-file/ce4848a1ff21/fetch-symbols.py')
md5sums=('5e9301143383c867240b784192783544')
depends=("firefox-nightly=$pkgver")
makedepends=("firefox-nightly=$pkgver" 'python2')

package() {
  msg "Fetching..."
  python2 fetch-symbols.py /opt/firefox-${pkgver} http://symbols.mozilla.org/ "${pkgdir}"
}
