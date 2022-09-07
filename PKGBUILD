# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-settings
pkgver=0.6.2
pkgrel=1
pkgdesc="QML based settings application for nemomobile"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-settings"
license=('BSD-3-Clause')
depends=('qt5-glacier-app'
    'qt5-location'
    'nemo-qml-plugin-devicelock'
    'nemo-qml-plugin-settings'
    'libconnman-qt'
    'libmce-qt'
    'nemo-qml-plugin-connectivity'
    'nemo-qml-plugin-configuration'
    'nemo-qml-plugin-models>=0.2.1'
    'nemo-qml-plugin-systemsettings>=0.8.0')
makedepends=('qt5-tools' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('c8eb651ae2b35b3f9b2a8b47a098afc824a970fc15b243b9a0f38f71c31f4237')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
