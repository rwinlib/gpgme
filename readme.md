All libs were configured with:

    ./configure --enable-static --disable-shared \
   		CC="gcc -m64" CXX="g++ -m64"

The client needs to manually set the path of `gpgme-w32spawn.exe` via

      gpgme_set_global_flag("w32-inst-dir", "C://Program Files (x86)//GnuPG/bin");

See also dicussion: http://marc.info/?l=gnupg-devel&m=144604688823859&w=2

Update: added a `./bin` directory with all files required for a standalone package.
These files were taken from the windows installers from the GPG download site.

 - `gpgme-w32spawn.exe` : extracted from "GnuPG modern" (gnupg-w32-2.1.15_20160818.exe)
 - `gpg.exe` and `iconv.dll` : extracted from "GnuPG classic" (gnupg-w32cli-1.4.21.exe)

I tried building these myself with mingw-w64 but they didn't work. Looks like
threading problems or so.
