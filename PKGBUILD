# Maintainer: Dragu Mihai <mikleaish@proton.me>
pkgname=watrpaper
pkgver=1.0.1
pkgrel=1
pkgdesc="GTK4 wallpaper picker with CSS styling support"
arch=('any')
url="https://github.com/judii8/watrpicker"
license=('MIT')
depends=('python' 'python-gobject' 'gtk4' 'gdk-pixbuf2')
optdepends=('swww: fallback backend for setting the wallpaper'
            'hyprland: hyprctl/hyprpaper fallback backend')
source=("$pkgname-$pkgver.tar.gz::https://github.com/judii8/watrpicker/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('8a9981b3686b881bf5d66b1f487a7a0065df94d4141ecc60ef94ee1dfd30d32f')

package() {
  cd "$srcdir/watrpicker-$pkgver"
  install -Dm755 watrpaper "$pkgdir/usr/bin/watrpaper"
  install -Dm644 style.css "$pkgdir/usr/share/doc/$pkgname/style.css.example"
  install -Dm644 watrpaper.desktop "$pkgdir/usr/share/applications/watrpaper.desktop"

  if [ -f README.md ]; then
    install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
  fi
  if [ -f LICENSE ]; then
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  fi
}
