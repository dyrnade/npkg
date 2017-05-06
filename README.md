### npkg ###

This is inspired from awesome SolusOS's ypkg.

For now, it handles some fields. This is an attempt for making packaging with Nix easy.

**Dependencies:** nix-prefetch-url and nix-prefetch-git *(if you will use only one of them, then other is not necessary)*
If you run, you will have something like this.

```bash
[vagrant@nixbox:~/npkg]$ ./npkg https://github.com/dyrnade/npkg.git
{stdenv, fetchgit}:

stdenv.mkDerivation {
name = "npkg";

src = fetchgit {
url = https://github.com/dyrnade/npkg.git;
rev = "a1ca90e2caef24736aa8b8a3968dcc2b89c70372";
sha256 = "0hdxw6hm89mkkfyavx62l17aa1izrv4797kd44awml33xn6gn385";
};

buildInputs = [];

meta = with stdenv.lib; {
homepage = https://github.com/dyrnade/npkg.git;
description = "";
license = licenses.unlicensed;
platforms = platforms.linux;
maintainers = ;
};

```

**Note**: Not finished yet and any suggestions and improvements are welcome.
