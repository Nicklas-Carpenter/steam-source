# Maintainer: Nicklas Carpenter <carpenter.nicklas@gmail.com>

pkgname='steam-source'
pkgver=2021.09.11.1
pkgrel=1
pkgdesc='Package of Steam based off the Valve unpackaged release'
arch=('x86_64')
url='https://github.com/Nicklas-Carpenter/steam-source'
license=('GPLv3')
makedepends=('curl' 'make' 'tar')

src_uri='http://repo.steampowered.com/steam/archive/precise/steam_latest.tar.gz'
output_name='steam_latest.tar.gz'
output_dir='steam-launcher'

prepare() {
	curl ${src_uri} --output ${output_name}	
	tar -xf ${output_name} -z
}

package() {
	cd ${srcdir}/${output_dir}
	pwd
	make install DESTDIR=${pkgdir}
}
	
