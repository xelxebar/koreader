### Building

1. Fetch third party dependencies:
    $ ./kodev fetch-thirdparty

2. Install the following packages:
    - autoconf
    - automake
    - ccache
    - cmake
    - gcc
    - gettext
    - libtool
    - luarocks-lua51 (2.x)
    - make
    - nasm
    - patch
    - pkg-config
    - unzip
    - wget
    - python

3. Build

    $ ./kodev build


### Testing

1. Install the following packages:
    - LuaJIT
    - cairo
    - icu
    - lua51-devel
    - pango

2. Setup environment for lua:

    $ ./kodev activate

3. Install the following lua rocks:
    - ansicolors
    - busted
    - luacheck

4. Install Tesseract English data:

    $ curl -LO 'https://src.fedoraproject.org/repo/pkgs/tesseract/tesseract-ocr-3.02.eng.tar.gz/3562250fe6f4e76229a329166b8ae853/tesseract-ocr-3.02.eng.tar.gz'
    $ tar -xzvf tesseract-ocr-3.02.eng.tar.gz
    $ mv tesseract-ocr/tessdata base/thirdparty/kpvcrlib/crengine/cr3gui/data/

5. Run tests

    $ ./kodev test base
    $ ./kodev test front


### Building Release

1. Install the following packages:
    - gcc-multilib
    - python3
    - zip

2. Install transifex-client:

    $ pip install transifex-client

3. Setup transifex account and join koreader project

4. Initialize transifex client

    $ tx init

5. Setup koxtoolchain and update PATH accordingly

6. ./kodev release <device>
