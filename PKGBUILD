
pkgname=ms-sys
pkgver=2.4.1
pkgrel=1
pkgdesc="A tool to write Win9x/2k/XP/2k3/Vista/7/2k8 master boot records (mbr) under linux - RTM!"
arch=('x86_64')
url="http://ms-sys.sourceforge.net/"
license=('GPL')
#source=(${pkgname}-${pkgver}.tar.gz::http://sourceforge.net/projects/${pkgname}/files/${pkgname}%20stable/${pkgver}/${pkgname}-${pkgver}.tar.gz/download)
source=(${pkgname}-${pkgver}.tar.gz::http://prdownloads.sourceforge.net/${pkgname}/${pkgname}-${pkgver}.tar.gz?download)
md5sums=('d31e7ef3db6bd77dbb13df11057fa0f2')

build() {
  cd "${srcdir}"/${pkgname}-${pkgver}
  make
}

package() {
  cd "${srcdir}"/${pkgname}-${pkgver}
  make PREFIX=/usr MANDIR=/usr/share/man DESTDIR="${pkgdir}" install
}
