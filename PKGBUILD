# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=dropbox-humanity-icons
pkgver=1.1
pkgrel=10
pkgdesc="Notification icons for Dropbox matching the Humanity theme."
arch=(any)
url="https://forums.dropbox.com/topic.php?id=7818"
license=(CCPL:by-3.0)
depends=(dropbox hicolor-icon-theme)
conflicts=(dropbox-{humanity-dark,{light,dark}-panel}-icons)
install=icons.install
source=($pkgname.tar.gz::'https://dl.dropbox.com/u/62148/Misc/Dropbox Humanity Notification Icons.tar.gz?dl=1')
sha256sums=('fe76301c5bb17780650e772adb1b1a0b65ffcfa9448f49ab1d57884c2a650f94')
sha512sums=('1b2537cbacacdfcb235c9efff9a95ffc09a3909262a66247e0b8be19a59f60fcb606ff857d30b84f62ab61bfcf19ef2fb9b2da691025a72902c6454cd9b23034')

package() {
    cd "$srcdir"/Dropbox\ Humanity\ Notification\ Icons/Humanity/icons/
    for i in {busy{,2},logo,x}.png; do
        mv $i dropboxstatus-$i
    done
    for i in *.png; do
        install -Dm644 $i "$pkgdir"/usr/share/icons/hicolor/16x16/status/$i
    done
}
