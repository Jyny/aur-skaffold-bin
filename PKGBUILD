# Maintainer: Brad Erhart <tocusso underscore malty at aleeas dot com>
# Maintainer: Jerry Y. Chen <chen@jyny.dev>

pkgname=skaffold-bin
reponame=skaffold
provides=('skaffold')
conflicts=('skaffold')
pkgver=2.11.0
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
  x86_64)    _CARCH=amd64 && sha256sums=('574b8862ec4625f19d2bbafc88e5e58868bb2db39e4b6cc74c429ad11b4839e4');;
  aarch64)   _CARCH=arm64 && sha256sums=('46e4f8ea4070b55ebe931db5b7960312a101475f16aa4bd0e2cd2f8ed13a5218');;
esac

source=("${reponame}-${pkgver}-${_CARCH}::https://github.com/GoogleContainerTools/skaffold/releases/download/v$pkgver/skaffold-linux-${_CARCH}")

package() {
  install -Dm 0755 ${reponame}-${pkgver}-${_CARCH} "$pkgdir/usr/bin/skaffold"
}
