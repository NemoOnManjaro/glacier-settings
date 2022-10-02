# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-settings
pkgver=0.6.3
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
sha256sums=('137c5a48dc8e8a0fd772c568e43e163f024877ae46dfe32e80a4adcfd6e42795')

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
