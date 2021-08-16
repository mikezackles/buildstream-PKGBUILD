# Maintainer: Rafael Fontenelle <rafaelff@gnome.org>
pkgname=buildstream
pkgver=1.6.2
pkgrel=1
pkgdesc="A powerful and flexible software integration toolset"
arch=('any')
url="https://buildstream.build"
license=('LGPL')
depends=(
    bubblewrap
    python-click
    python-gobject
    python-grpcio
    python-jinja
    python-pluginbase
    python-protobuf
    python-psutil
    python-pyroaring
    python-ruamel-yaml
    python-six
    python-ujson
)
optdepends=(bzr git lzip ostree python-arpy)
makedepends=(python-setuptools cython)
source=("https://github.com/apache/buildstream/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('134dd7ce95e6846ccd36c6e8c8f74af038dcc3010a0287e67a6ae59d31e0ff7f')

build() {
  cd buildstream-$pkgver
  python setup.py build
}

package() {
  cd buildstream-$pkgver
  python setup.py install --root="$pkgdir/" --optimize=1 --skip-build
}
