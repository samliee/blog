# Beancount-Fava-Android-Tutorial

Fava is a web interface for the double-entry bookkeeping software Beancount with a focus on features and usability. <https://github.com/beancount/fava>

This tutorial aim to install fava on Android.

## Prepare

- Android Phone
- Termux <https://termux.dev/en/>
- Network connection

## Installation Sequence

### Step 1

Open the Termux. Enter the following command to install python and rust

```bash
pkg install python rust
```

### Step 2

```bash
pkg install libxml2-utils libxslt libxml2
```

### Step 3

```bash
pip install lxml
```

MAKE SURE THE LXML IS SUCCESSFULLY INSTALLED

### Step 4

```bash
pip install fava
```

run `fava`, you will see the text below.

```bash
$ fava
Usage: fava [OPTIONS] [FILENAMES]...
Try 'fava --help' for help.

Error: No file specified
```

Now the Installtion is complete. Congratulation!

## Troubleshooting 

remove the pip cache and try again.

```bash
pip cache purge 
```

## My environment

### termux-info

```bash
$ termux-info
Termux Variables:
TERMUX_EXEC__PROC_SELF_EXE=/data/data/com.termux/files/usr/bin/termux-info
TERMUX_VERSION=googleplay.2024.10.30
TERMUX__USER_ID=0
Packages CPU architecture:
aarch64
Subscribed repositories:
# sources.list
deb https://termux.net stable main
Updatable packages:
command-not-found/stable 2.4.0-52 aarch64 [upgradable from: 2.4.0-48]
curl/stable 8.11.0-1 aarch64 [upgradable from: 8.10.1-2]
debianutils/stable 5.21 aarch64 [upgradable from: 5.20]
inetutils/stable 2.5 aarch64 [upgradable from: 2.4-2]
libc++/stable 27c aarch64 [upgradable from: 27b]
libcurl/stable 8.11.0-1 aarch64 [upgradable from: 8.10.1-2]
libsmartcols/stable 2.40.2-2 aarch64 [upgradable from: 2.40.2-1]
rust-std-aarch64-linux-android/stable 1.83.0 all [upgradable from: 1.82.0]
rust/stable 1.83.0 aarch64 [upgradable from: 1.82.0]
util-linux/stable 2.40.2-2 aarch64 [upgradable from: 2.40.2-1]
termux-tools version:
3.0.8
Android version:
13
Kernel build information:
Linux localhost 4.4.302-Rave-EAS-QTI-v4.9 #1 SMP PREEMPT Sat Nov 25 23:34:26 CET 2023 aarch64 Android
Device manufacturer:
******
Device model:
******
LD Variables:
LD_LIBRARY_PATH=
LD_PRELOAD=/data/data/com.termux/files/usr/lib/libtermux-exec.so
```

### python -v

```bash
Python 3.12.7 (main, Oct 23 2024, 22:38:17) [Clang 18.0.2 (https://android.googlesource.com/toolchain/llvm-project d8003a456 on linux
```

### pip list

```bash
$ pip list

Package                  Version
------------------------ -----------
anyio                    4.6.2.post1
babel                    2.16.0
beancount                2.3.6
beautifulsoup4           4.12.3
blinker                  1.9.0
bottle                   0.13.2
cachetools               5.5.0
certifi                  2024.8.30
chardet                  5.2.0
charset-normalizer       3.4.0
cheroot                  10.0.1
click                    8.1.7
fava                     1.29
Flask                    3.1.0
flask-babel              4.0.0
google-api-core          2.23.0
google-api-python-client 2.154.0
google-auth              2.36.0
google-auth-httplib2     0.2.0
googleapis-common-protos 1.66.0
httplib2                 0.22.0
idna                     3.10
iniconfig                2.0.0
itsdangerous             2.2.0
jaraco.functools         4.1.0
Jinja2                   3.1.4
lxml                     5.3.0
markdown2                2.5.1
MarkupSafe               3.0.2
more-itertools           10.5.0
packaging                24.2
pdfminer2                20151206
pip                      24.3.1
pluggy                   1.5.0
ply                      3.11
proto-plus               1.25.0
protobuf                 5.29.0
pyasn1                   0.6.1
pyasn1_modules           0.4.1
pyparsing                3.2.0
pytest                   8.3.3
python-dateutil          2.9.0.post0
python-magic             0.4.27
pytz                     2024.2
requests                 2.32.3
rsa                      4.9
simplejson               3.19.3
six                      1.16.0
sniffio                  1.3.1
soupsieve                2.6
uritemplate              4.1.1
urllib3                  2.2.3
watchfiles               1.0.0
Werkzeug                 3.1.3
```

### pkg list

```bash
$ pkg list-installed

apt/stable,now 2.9.10 aarch64 [installed]
bash/stable,now 5.2.37 aarch64 [installed]
ca-certificates/stable,now 2024.09.24 all [installed]
clang/stable,now 19.1.4 aarch64 [installed]
command-not-found/now 2.4.0-48 aarch64 [installed,upgradable to: 2.4.0-52]
coreutils/stable,now 9.5-3 aarch64 [installed]
curl/now 8.10.1-2 aarch64 [installed,upgradable to: 8.11.0-1]
dash/stable,now 0.5.12 aarch64 [installed]
debianutils/now 5.20 aarch64 [installed,upgradable to: 5.21]
diffutils/stable,now 3.10 aarch64 [installed]
dos2unix/stable,now 7.5.2 aarch64 [installed]
dpkg/stable,now 1.22.6-3 aarch64 [installed]
ed/stable,now 1.20.2 aarch64 [installed]
findutils/stable,now 4.10.0 aarch64 [installed]
gawk/stable,now 5.3.0 aarch64 [installed]
gdbm/stable,now 1.24 aarch64 [installed,automatic]
glib/stable,now 2.82.2 aarch64 [installed,automatic]
gpgv/stable,now 2.4.5-7 aarch64 [installed]
grep/stable,now 3.11 aarch64 [installed]
inetutils/now 2.4-2 aarch64 [installed,upgradable to: 2.5]
less/stable,now 661 aarch64 [installed]
libandroid-posix-semaphore/stable,now 0.1-3 aarch64 [installed,automatic]
libandroid-selinux/stable,now 14.0.0.11 aarch64 [installed]
libassuan/stable,now 3.0.1-2 aarch64 [installed]
libbz2/stable,now 1.0.8-7 aarch64 [installed]
libc++/now 27b aarch64 [installed,upgradable to: 27c]
libcap-ng/stable,now 0.8.5 aarch64 [installed]
libcompiler-rt/stable,now 19.1.4 aarch64 [installed,automatic]
libcrypt/stable,now 0.2-5 aarch64 [installed,automatic]
libcurl/now 8.10.1-2 aarch64 [installed,upgradable to: 8.11.0-1]
libexpat/stable,now 2.6.4 aarch64 [installed,automatic]
libffi/stable,now 3.4.6-1 aarch64 [installed,automatic]
libgcrypt/stable,now 1.11.0 aarch64 [installed]
libgmp/stable,now 6.3.0-1 aarch64 [installed]
libgnutls/stable,now 3.8.5-1 aarch64 [installed]
libgpg-error/stable,now 1.50 aarch64 [installed]
libiconv/stable,now 1.17-1 aarch64 [installed,automatic]
libidn2/stable,now 2.3.7 aarch64 [installed]
libllvm/stable,now 19.1.4 aarch64 [installed,automatic]
liblzma/stable,now 5.6.3 aarch64 [installed]
libmd/stable,now 1.1.0 aarch64 [installed]
libmpfr/stable,now 4.2.1 aarch64 [installed]
libnettle/stable,now 3.10 aarch64 [installed]
libnghttp2/stable,now 1.64.0 aarch64 [installed]
libnghttp3/stable,now 1.6.0 aarch64 [installed]
libnpth/stable,now 1.6-2 aarch64 [installed]
libsmartcols/now 2.40.2-1 aarch64 [installed,upgradable to: 2.40.2-2]
libsqlite/stable,now 3.47.1 aarch64 [installed,automatic]
libssh2/stable,now 1.11.1 aarch64 [installed]
libunistring/stable,now 1.3 aarch64 [installed]
libxml2-utils/stable,now 2.13.5 aarch64 [installed]
libxml2/stable,now 2.13.5 aarch64 [installed]
libxslt/stable,now 1.1.42-1 aarch64 [installed]
lld/stable,now 19.1.4 aarch64 [installed,automatic]
llvm/stable,now 19.1.4 aarch64 [installed,automatic]
make/stable,now 4.4.1 aarch64 [installed,automatic]
nano/stable,now 8.2 aarch64 [installed]
ncurses-ui-libs/stable,now 6.5.20240831-2 aarch64 [installed,automatic]
ncurses/stable,now 6.5.20240831-2 aarch64 [installed]
ndk-sysroot/stable,now 27c aarch64 [installed,automatic]
net-tools/stable,now 2.10.0 aarch64 [installed]
openssl/stable,now 3.3.2 aarch64 [installed]
patch/stable,now 2.7.6-3 aarch64 [installed]
pcre2/stable,now 10.44 aarch64 [installed]
pkg-config/stable,now 0.29.2-2 aarch64 [installed,automatic]
procps/stable,now 3.3.17-5 aarch64 [installed]
psmisc/stable,now 23.7 aarch64 [installed]
python-ensurepip-wheels/stable,now 3.12.7-1 all [installed,automatic]
python-pip/stable,now 24.3.1 all [installed,automatic]
python/stable,now 3.12.7-1 aarch64 [installed]
readline/stable,now 8.2.13 aarch64 [installed]
resolv-conf/stable,now 1.3 aarch64 [installed,automatic]
rust-std-aarch64-linux-android/stable,now 1.82.0 all [installed,automatic]
rust/stable,now 1.82.0 aarch64 [installed]
sed/stable,now 4.9-1 aarch64 [installed]
tar/stable,now 1.35-1 aarch64 [installed]
termux-am/stable,now 0.8.0-1 all [installed]
termux-exec/stable,now 1.7 aarch64 [installed]
termux-keyring/stable,now 3.15 all [installed]
termux-licenses/stable,now 2.0-4 all [installed]
termux-tools/stable,now 3.0.8 aarch64 [installed]
unzip/stable,now 6.0-9 aarch64 [installed]
util-linux/now 2.40.2-1 aarch64 [installed,upgradable to: 2.40.2-2]
xxhash/stable,now 0.8.2 aarch64 [installed]
zlib/stable,now 1.3.1 aarch64 [installed]
zstd/stable,now 1.5.6-2 aarch64 [installed,automatic]
```
