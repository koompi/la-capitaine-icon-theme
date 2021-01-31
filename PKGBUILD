pkgname=('la-capitaine-icon-theme-koompi')
pkgver=20210131
pkgrel=1
pkgdesc="La Capitaine is an icon pack — designed to integrate with most desktop environments."
arch=('any')
url="https://github.com/koompi/la-capitaine-icon-theme"
license=('GPL3')
optdepends=('elementary-icon-theme' 'breeze-icons' 'gnome-icon-theme')
conflicts=('la-capitaine-icon-theme-git')
source=("git+https://github.com/koompi/la-capitaine-icon-theme.git")
md5sums=('SKIP')
package() {
    cd "${srcdir}/la-capitaine-icon-theme"
    git checkout koompi
    install -dm 755 "${pkgdir}"/usr/share/icons
    cp -dr --no-preserve='ownership' "${srcdir}/la-capitaine-icon-theme" "${pkgdir}"/usr/share/icons/la-capitaine

    find "${pkgdir}" -type d -exec chmod 755 {} +
    find "${pkgdir}" -type f -exec chmod 644 {} +
    find ${pkgdir}/usr -type f -name '.directory' -delete
    rm -rf "$pkgdir/usr/share/icons/la-capitaine/.gitignore"
    rm -rf "$pkgdir/usr/share/icons/la-capitaine/.git"
    rm -rf "$pkgdir/usr/share/icons/la-capitaine/.github"
    rm -rf "$pkgdir/usr/share/icons/la-capitaine/.product"
}
