# Axel for windows

Axel x86-64 v2.17.3 builded in Cygwin 2.925 (64 bit) for windows with openssl 1.1 & intl library:

    > .\axel.exe -V
    Axel version 2.17.3+gb1cf9b (cygwin)
    
    Copyright 2001-2007 Wilmer van der Gaast,
              2007-2009 Giridhar Appaji Nag,
              2008-2010 Philipp Hagemeister,
              2015-2017 Joao Eriberto Mota Filho,
              2016-2017 Stephen Thirlwall,
              2017      Ismael Luceno,
              2017      Antonio Quartulli,
                        and others.
    Please, see the CREDITS file.
    
# Usage

    > .\axel.exe -h
    Usage: axel [options] url1 [url2] [url...]
    
    --max-speed=x           -s x    Specify maximum speed (bytes per second)
    --num-connections=x     -n x    Specify maximum number of connections
    --max-redirect=x                Specify maximum number of redirections
    --output=f              -o f    Specify local output file
    --search[=n]            -S[n]   Search for mirrors and download from n servers
    --ipv4                  -4      Use the IPv4 protocol
    --ipv6                  -6      Use the IPv6 protocol
    --header=x              -H x    Add HTTP header string
    --user-agent=x          -U x    Set user agent
    --no-proxy              -N      Just don't use any proxy server
    --insecure              -k      Don't verify the SSL certificate
    --no-clobber            -c      Skip download if file already exists
    --quiet                 -q      Leave stdout alone
    --verbose               -v      More status information
    --alternate             -a      Alternate progress indicator
    --help                  -h      This information
    --timeout=x             -T x    Set I/O and connection timeout
    --version               -V      Version information
    
    Visit https://github.com/axel-download-accelerator/axel/issues to report bugs

# Build info

    $ file ./axel.exe
    ./axel.exe: PE32+ executable (console) x86-64, for MS Windows, 19 sections

    $ gcc -v
    Using built-in specs.
    COLLECT_GCC=gcc
    COLLECT_LTO_WRAPPER=/usr/lib/gcc/x86_64-pc-cygwin/11/lto-wrapper.exe
    Target: x86_64-pc-cygwin
    Configured with: /mnt/share/cygpkgs/gcc/gcc.x86_64/src/gcc-11.4.0/configure --srcdir=/mnt/share/cygpkgs/gcc/gcc.x86_64/src/gcc-11.4.0 --prefix=/usr --exec-prefix=/usr --localstatedir=/var --sysconfdir=/etc --docdir=/usr/share/doc/gcc --htmldir=/usr/share/doc/gcc/html -C --build=x86_64-pc-cygwin --host=x86_64-pc-cygwin --target=x86_64-pc-cygwin --without-libiconv-prefix --without-libintl-prefix --libexecdir=/usr/lib --with-gcc-major-version-only --enable-shared --enable-shared-libgcc --enable-static --enable-version-specific-runtime-libs --enable-bootstrap --enable-__cxa_atexit --with-dwarf2 --with-tune=generic --enable-languages=ada,c,c++,d,fortran,lto,objc,obj-c++,jit --enable-graphite --enable-threads=posix --enable-libatomic --enable-libgomp --enable-libquadmath --enable-libquadmath-support --disable-libssp --enable-libada --disable-symvers --disable-multilib --with-gnu-ld --with-gnu-as --with-cloog-include=/usr/include/cloog-isl --without-libiconv-prefix --without-libintl-prefix --with-system-zlib --enable-linker-build-id --with-default-libstdcxx-abi=gcc4-compatible --enable-libstdcxx-filesystem-ts
    Thread model: posix
    Supported LTO compression algorithms: zlib zstd
    gcc version 11.4.0 (GCC)


## Dependencies

 - `gettext` - 0.22-1
 - `pkg-config` - 1.9.5-1
 - `libssl` - 1.1.1u-1
 - `autoconf2.7` - 2.71-2
 - `autoconf-archive` - 2023.02.20-1
 - `automake1.16` - 1.16.5-1