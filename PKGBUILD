# Maintainer: Maxwell Pray a.k.a. Synthead <synthead@gmail.com>
# Contributor: Jacek Roszkowski <j.roszk@gmail.com>

pkgname=ruby1.8-rack-v1.1.0
pkgver=1.1.0
pkgrel=2
pkgdesc="A minimal interface between webservers supporting Ruby and Ruby frameworks"
arch=('any')
url="http://rack.rubyforge.org"
license=("GPL")
depends=('ruby1.8' 'rubygems1.8')
source=("http://gems.rubyforge.org/gems/rack-$pkgver.gem")
noextract=("rack-$pkgver.gem")
conflicts=('ruby1.8-rack-v1.0.1' 'ruby1.8-rack')
provides=('ruby1.8-rack')
md5sums=('f5ff2d6d348f41bb3833847223f792ce')

build() {
	local _gemdir="$(ruby-1.8 -rubygems -e'puts Gem.default_dir')"
	gem-1.8 install -Vl --no-user-install --ignore-dependencies -i "$pkgdir$_gemdir" "$srcdir/rack-$pkgver.gem"
}
