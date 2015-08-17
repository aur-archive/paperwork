# Maintainer: Francois Boulogne <fboulogne@april.org>

pkgname=paperwork
pkgver=0.2.4
pkgrel=0
pkgdesc='A tool to make papers searchable - scan & forget'
arch=('any')
url='https://github.com/jflesch/paperwork'
license=('GPL3')
provides=('paperwork')
conflicts=('paperwork')
depends=('pygobject2-devel' 'pygtk' 'python2-pycountry'
'python2-poppler' 'python2-pyinsane-git' 'python2-pyocr'
'python2-levenshtein' 'python2-whoosh' 'python2-pyenchant'
'python2-joblib' 'python2-numpy' 'python2-scipy' 'python2-scikit-learn' 'python2-scikit-image'
'python2-gobject' 'python2-nltk' 'glade')
makedepends=('python2' 'python2-setuptools')
optdeps=('cuneiform: alternativer OCR')
source=("https://github.com/jflesch/paperwork/archive/${pkgver}.zip")
install=paperwork.install

build() {
  cd "${pkgname}-${pkgver}"
  python2 setup.py build
}

package() {
  cd "${pkgname}-${pkgver}"
  python2 setup.py install --prefix=/usr --root="${pkgdir}" --optimize=1
  install -D -m644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
# vim:ts=2:sw=2:et:
md5sums=('fb3f4840af6ceec519a48a712d5af2ed')
