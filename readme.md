# GPGME

Libraries built with GCC-8 (rtools40):

  - `mingw-w64-gpgme` 1.12.0
  - `mingw-w64-libassuan` 2.5.2
  - `mingw-w64-libgpg-error` 1.33-1

The `./bin` executables are taken from the windows installers from the GPG download site.

 - `gpgme-w32spawn.exe` : extracted from "GnuPG modern" (gnupg-w32-2.2.12_20181214.exe)
 - `gpg.exe` and `iconv.dll` : extracted from "GnuPG classic" (gnupg-w32cli-1.4.23.exe)

The client needs to manually set the path of `gpgme-w32spawn.exe` via

      gpgme_set_global_flag("w32-inst-dir", "C://Program Files (x86)//GnuPG/bin");

See also dicussion: http://marc.info/?l=gnupg-devel&m=144604688823859&w=2
