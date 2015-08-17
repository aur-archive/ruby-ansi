# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>
# Contributor: fnord0 <fnord0 AT riseup DOT net>

pkgname=ruby-ansi
_gemname=${pkgname#ruby-}
pkgver=1.4.3
pkgrel=1
pkgdesc="a superlative collection of ANSI escape code related libraries enabling ANSI colorization and stylization of console output"
arch=('any')
url="http://github.com/rubyworks/ansi"
license=('BSD')
depends=('ruby' 'rubygems')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('c32b8ab33a6bc3046d7763f42aacd93e')

build() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" -n "${pkgdir}/usr/bin" ${_gemname}-${pkgver}.gem
}
