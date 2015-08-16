# Maintainer: Tauren Chieftain <6ahodir@gmail.com>
pkgname=hunspell-uz
pkgver=0.1
pkgrel=1
pkgdesc="Uzbek hunspell dictionary"
arch=(any)
url="http://wiki.openoffice.org/wiki/Dictionaries"
license=("GPL")
optdepends=("hunspell: Spell checking library and program")
makedepends=()
source=(http://hunspell.sourceforge.net/uz-demo.tar.gz)
sha1sums=("768eb00309cc0e3d1f896fdd4d41a5535bfafc4e")

build() {
 /bin/true
}

package() {
    install -dm755 ${pkgdir}/usr/share/hunspell
    install -m644 ${srcdir}/uz/uz.dic ${srcdir}/uz/uz.aff ${pkgdir}/usr/share/hunspell
    ln -s /usr/share/hunspell/uz.dic ${pkgdir}/usr/share/hunspell/uz_UZ.dic
    ln -s /usr/share/hunspell/uz.aff ${pkgdir}/usr/share/hunspell/uz_UZ.aff

    install -dm755 ${pkgdir}/usr/share/myspell/dicts
    ln -s /usr/share/hunspell/uz.dic ${pkgdir}/usr/share/myspell/dicts/uz_UZ.dic
    ln -s /usr/share/hunspell/uz.aff ${pkgdir}/usr/share/myspell/dicts/uz_UZ.aff

    # docs
    install -dm755 ${pkgdir}/usr/share/doc/${pkgname}
    install -m 644 ${srcdir}/uz/README ${pkgdir}/usr/share/doc/${pkgname}
}
