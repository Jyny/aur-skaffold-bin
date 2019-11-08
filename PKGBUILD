# Maintainer: Stefan Cocora <stefan dot cocora at gmail dot com>
# Maintainer: Brad Erhart <brae dot 04+aur at gmail dot com >
# Maintainer: Michael Beaumont
# Maintainer: aps42 <arch at andre-sterba dot de>
# Contributor:

_pkgauthor=GoogleContainerTools
_upstream_pkgname=skaffold
pkgname=skaffold-bin
pkgver=1.0.0
pkgrel=1
pkgdesc="A command line tool that facilitates continuous development for Kubernetes applications."
arch=('x86_64')
_goos="linux"
_goarch="amd64"
groups=()
depends=()
makedepends=()
provides=("skaffold-bin")
conflicts=("skaffold" "skaffold-git")
replaces=("skaffold" "skaffold-git")
backup=()
options=()
install=
url="https://github.com/${_pkgauthor}/${_upstream_pkgname}"
license=("Apache")
_doc_html="index.html"
_doc_pdf="index.pdf"
### https://github.com/GoogleContainerTools/skaffold/releases/download/v0.19.0/skaffold-linux-amd64
source=("${_upstream_pkgname}-${_goos}-${_goarch}::https://github.com/${_pkgauthor}/${_upstream_pkgname}/releases/download/v${pkgver}/${_upstream_pkgname}-linux-${_goarch}"
  "LICENSE::https://raw.githubusercontent.com/${_pkgauthor}/${_upstream_pkgname}/master/LICENSE")
sha256sums=('f03cb2115cd510b6de8b024165b6621e453935faaf99b20c8cdf9933eec9b913'
            '43a2aa523a99dddb6c131e67e11334493e64c67f03b0d8f6745b6b3f34157d65')

package() {

  install -Dm755 "${srcdir}/${_upstream_pkgname}-${_goos}-${_goarch}" "${pkgdir}/usr/bin/${_upstream_pkgname}"
  install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${_upstream_pkgname}/LICENSE"
}
