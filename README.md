
Demonstrates a dependency build error with `cabal new-build`.

I have zlib installed into /usr/local via homebrew on macOS.

Building this project, even with extra-*-dirs flags set, results in a build error.


```
Failed to build digest-0.0.1.2. The failure occurred during the configure
step.
Build log (
/Users/nkpart/.cabal/logs/ghc-8.0.2/digest-0.0.1.2-5d30d30d7d2e93c4245c1d2f590f03bf3515dc7425cc86e699c5f54e3ca962cf.log
):
Configuring digest-0.0.1.2...
cabal: Missing dependency on a foreign library:
* Missing (or bad) header file: zlib.h
This problem can usually be solved by installing the system package that
provides this library (you may need the "-dev" version). If the library is
already installed but in a non-standard location then you can use the flags
--extra-include-dirs= and --extra-lib-dirs= to specify where it is.
If the header file does exist, it may contain errors that are caught by the C
compiler at the preprocessing stage. In this case you can re-run configure
with the verbosity flag -v3 to see the error messages.
cabal: Failed to build digest-0.0.1.2 (which is required by
cabal-new-build-test-0.1.0.0). See the build log above for details.

```
