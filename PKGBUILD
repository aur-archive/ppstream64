# Contributor: figo1802 <figo1802@gmail.com>
# modify for 64bit <lerosua@gmail.com>


pkgname='ppstream64'
pkgver='1.0.2'
pkgrel='5'
arch='x86_64'
url='http://www.ppstream.com'
license=('unknown')
pkgdesc='PPStream for Archlinux 64bit'
provides=('ppstream')
conflicts=('ppstream')


depends=('mplayer' 'lib32-qt' 'lib32-giflib' 'lib32-libpng' 'lib32-libpng12' 'lib32-libjpeg-turbo' 'lib32-libjpeg6' 'lib32-alsa-lib' 'lib32-libxv' 'lib32-util-linux' 'lib32-libxdmcp' 'lib32-glibc' 'lib32-libsm' 'lib32-zlib' 'lib32-libx11' 'lib32-libxext' 'lib32-libxcb' 'lib32-libxau' 'lib32-glib2' 'lib32-libxrender' 'lib32-expat' 'lib32-pcre' 'lib32-bzip2' 'lib32-openssl' 'lib32-fontconfig' 'lib32-gtk-engines' 'lib32-libcanberra' 'lib32-libcanberra-pulse' )
source=('http://download.ppstream.com/linux/PPStream.deb')
md5sums=('c5d02182e34f58edd65a03d0cf42fcef')

install=$pkgname.install
build() {
	cd $startdir/src/
      ar -xv PPStream.deb;
      tar -xvf data.tar.gz

	mv usr/ ${startdir}/pkg/ ;
	mv opt/ ${startdir}/pkg/ ;
	mv etc/ ${startdir}/pkg/ ;

	#mkdir -p ${startdir}/pkg/usr/lib/;
	ln -s /opt/pps/lib/libemscore.so.0.1.1946 ${pkgdir}/usr/lib/libemscore.so.0;
	ln -s /opt/pps/lib/libemsnet.so.0.1.1946 ${pkgdir}/usr/lib/libemsnet.so.0;
}
