# Maintainer: Nelson Estevão <nelson@marmelasoft.com>
pkgname="livebook"
pkgver="0.7.2"
pkgrel="1"
pkgdesc="Livebook - Automate code & data workflows with interactive Elixir notebooks"
arch=("x86_64")

depends=('openssl'  'erlang'  'elixir')

# sha256sums=("SKIP")

build() {
  mix do local.rebar --force, local.hex --force
  mix escript.install hex livebook 0.7.2
}

package() {
  # Copy the installed package to the package directory
  sudo cp -r $HOME/.mix/escripts/livebook /usr/bin/
}


