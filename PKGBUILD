# Maintainer: Brad Erhart <tocusso underscore malty at aleeas dot com>
# Maintainer: Jerry Y. Chen <chen@jyny.dev>

pkgname=skaffold-bin
reponame=skaffold
provides=('skaffold')
conflicts=('skaffold')
pkgver=2.12.0
pkgrel=1
pkgdesc="A command line tool that facilitates continuous development for Kubernetes applications"
arch=("x86_64")
url="https://github.com/GoogleContainerTools/${reponame}"
license=("Apache")
optdepends=(
  "docker: One of tools for building images support by skaffold"
  "minikube: To use Minikube"
  "kubectl: One of tools for deploying applications support by skaffold"
  "bash-completion: Tab autocompletion"
)

case "${CARCH}" in
  x86_64)    _CARCH=amd64 && sha256sums=('1a8e1f561c33d7b57dc594c83f38abb336bbf16039640e7fac172b8af0ce67f5');;
  aarch64)   _CARCH=arm64 && sha256sums=('477cb44807974d0e707b8f008fcb6135cda25ade22544802e2d634a933c408e8');;
esac

source=("${reponame}-${pkgver}-${_CARCH}::https://github.com/GoogleContainerTools/skaffold/releases/download/v$pkgver/skaffold-linux-${_CARCH}")

package() {
  install -Dm 0755 ${reponame}-${pkgver}-${_CARCH} "$pkgdir/usr/bin/skaffold"
}
