All libs were configured with:

    ./configure --enable-static --disable-shared \
   		CC="gcc -m64" CXX="g++ -m64"

The client needs to manually set the path of `gpgme-w32spawn.exe` via

      gpgme_set_global_flag("w32-inst-dir", "C://Program Files (x86)//GnuPG/bin");

See also dicussion: http://marc.info/?l=gnupg-devel&m=144604688823859&w=2
