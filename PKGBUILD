# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-settings
pkgver=0.8.9
pkgrel=1
pkgdesc="QML based settings application for nemomobile"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-settings"
license=('BSD-3-Clause')
depends=('qt6-glacier-app'
    'qt6-positioning'
    'nemo-qml-plugin-devicelock'
    'nemo-qml-plugin-settings'
    'libconnman-qt'
    'libmce-qt'
    'bluez-qt>=6.0'
    'nemo-qml-plugin-connectivity'
    'nemo-qml-plugin-configuration'
    'nemo-qml-plugin-models>=0.2.1'
    'nemo-qml-plugin-systemsettings>=0.8.0')
makedepends=('qt6-tools' 'clang' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('dfb02af0bdac44b7203c5bdf6a19b82abb112c80309f516d94b8d3a1361ee4e3')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr' \
        -DCMAKE_POLICY_VERSION_MINIMUM=3.5
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
