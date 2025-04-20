# SPDX-License-Identifier: AGPL-3.0

#    ----------------------------------------------------------------------
#    Copyright © 2024, 2025  Pellegrino Prevete
#
#    All rights reserved
#    ----------------------------------------------------------------------
#
#    This program is free software: you can redistribute it and/or modify
#    it under the terms of the GNU Affero General Public License as published by
#    the Free Software Foundation, either version 3 of the License, or
#    (at your option) any later version.
#
#    This program is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#    GNU Affero General Public License for more details.
#
#    You should have received a copy of the GNU Affero General Public License
#    along with this program.  If not, see <https://www.gnu.org/licenses/>.

# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Truocolo <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
# Maintainer: Pellegrino Prevete (dvorak) <pellegrinoprevete@gmail.com>
# Maintainer: Pellegrino Prevete (dvorak) <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>
# Maintainer: Victor Häggqvist <aur a snilius d com>
# https://github.com/victorhaggqvist/archlinux-pkgbuilds

_pkg=apk-resigner
pkgname="${_pkg}"
pkgver=1
pkgrel=2
_pkgdesc=(
  'A bash script utility that'
  'resigns the Android Package'
  '(APK) files (Android'
  'applications) with different'
  'certificates.'
)
url="https://code.google.com/p/apk-resigner/"
arch=(
  'i686'
  'x86_64'
  'arm'
)
license=(
  'Apache License 2.0'
)
depends=(
  'java-environment-common'
)
install="${_pkg}.install"
_android_sdk_build_tools_optdepends=(
  'android-sdk-build-tools:'
    'build tools are required,'
    'however you may provide this'
    'via your own Android SDK setup in PATH'
)
optdepends=(
  "${_android_sdk_build_tools_optdepends[*]}"
)

source=(
  "signapk.sh"
  "apk-resigner.install"
)
sha512sums=(
  'fce7e6fbf9ed702f559772535eb8078756cf1c69c2873e71a1421f8e05d5039d0fa88157cd21d607554720edb72f70774be4589ba08569fbe7c8b42cd91d03d6'
  '94bc7f2874c51c215c4ec60dd6226ce3b12e85669b5104cf9504a9caeb6d506562212b6ac813b0653a71de9dc6acbf340501d8cf5be5174ef0aa274478ce9d37'
)

package() {
  install \
    -Dm0755 \
    "${srcdir}/signapk.sh" \
    "${pkgdir}/usr/bin/signapk.sh"
}

# vim:set ts=2 sw=2 et:
