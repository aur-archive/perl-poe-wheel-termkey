# CPAN Name  : POE-Wheel-TermKey
# Contributor: Maciej Ciemborowicz <pub@ciemborowicz.pl>
# Generator  : CPANPLUS::Dist::Arch 1.23

pkgname='perl-poe-wheel-termkey'
pkgver='0.02'
pkgrel='3'
pkgdesc="terminal key input using libtermkey with POE"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-poe' 'perl-term-termkey')
makedepends=()
url='http://search.cpan.org/dist/POE-Wheel-TermKey'
source=('http://search.cpan.org/CPAN/authors/id/P/PE/PEVANS/POE-Wheel-TermKey-0.02.tar.gz')
md5sums=('56e96bec21fb93c94e5da78136860b69')
sha512sums=('14e409da2bcc592300d2570afe6a6c45be37dfcab98bda0badb220d3bff3bc8429bee478f581475f5634006a8c95ac720e91a9041bc3e70ac7f4ba2358c86632')
_distdir="${srcdir}/POE-Wheel-TermKey-0.02"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
