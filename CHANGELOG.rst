3.3.1: 2022/06/03
-----------------

- Fixed LZ4 filter compilation with `HDF5PLUGIN_HDF5_DIR` (PR #178)
- Renamed `PLUGINS_PATH` constant to `PLUGIN_PATH` without `S` (PR #179)
- Added notebook of European HUG meeting 2022 (PR #176)
- Updated changelog and version (PR #181)

3.3.0: 2022/05/25
-----------------

- Deprecated build options passed as arguments to `setup.py`, use environment variables instead (PR #167)
- Updated LZ4 filter to latest available code and LZ4 compression v1.9.3 (PR #172)
- Added `clevel` argument to `Zstd` (PR #164)
- Added `config.embedded_filters` to advertise embedded filters, and `HDF5PLUGIN_STRIP` to configure it during the build (PR #169)
- Added `-v` option to `python -m hdf5plugin.test` (PR #166)
- Changed "filter already loaded, skip it." log message from warning to info (PR #168)
- Updated build, now using `pyproject.toml` (PR #167, #173)
- Updated changelog and version (PR #174)

3.2.0: 2021/10/15
-----------------

- Updated libraries: blosc v1.21.1 (lz4 v1.9.3, zlib v1.2.11, zstd v1.5.0), snappy v1.1.8 (PR #152, #156)
- Fixed compilation issue occuring on ppc64le in conda-forge (PR #154)
- Documentation: Added European HDF User Group presentation (PR #150) and updated changelog (PR #155)

3.1.1: 2021/07/07
-----------------

This is a bug fix release:

- Fixed `hdf5plugin` when installed as a Debian/Ubuntu package (PR #147)
- Fixed and updated documentation (PR #143, #148)

3.1.0: 2021/07/02
-----------------

This version of `hdf5plugin` requires Python3 adds `mips64` supports and improves support for other architectures.

- Added support of `mips64` architecture (PR #126)
- Added enhanced documentation based on sphinx hosted at http://www.silx.org/doc/hdf5plugin/latest/ and on readthedocs.org (PR #137, #139, #141)
- Fixed LZ4 filter by downgrading used lz4 algorithm implementation (PR #123)
- Fixed `python setup.py install` (PR #125, #130)
- Improved build options support (PR #125, #130, #135, #140)
- Improved tests (PR #128, #129, #132)
- Cleaned-up python2 compatibility code (PR #134)
- Updated project description/metadata: Added Python3.9, `python_requires`, updated status to "Stable" (PR #119, #127, #138)
- Updated CHANGELOG and version (PR #142)

3.0.0
-----

This version of `hdf5plugin` requires Python3 and supports arm64 architecture.

- Stopped Python2.7 support (PR #104, #105)
- Added support of arm64 architecture (PR #116)
- Added `Zstd` filter to the supported plugin list (PR #106)
- Added `hdf5plugin.config` to retrieve build options at runtime (PR #113)
- Added support of build configuration through environment variables (PR #116)
- Fixed `FciDecomp` error message when built without c++11 (PR #113)
- Updated blosc compile flags (`-std-c99`) to build for manylinux1 (PR #109)
- Updated c-blosc to v1.20.1 (PR #101)
- Updated: continuous integration (PR #104, #111), project structure (PR #114, #118), changelog (PR #117)

2.3.2
-----

This is the last version of `hdf5plugin` supporting Python 2.7.

- Enabled SIMD on power9 for bitshuffle filter (PR #90)
- Added github actions continous intergration (PR #99)
- Added debian/ubuntu packaging support (PR #87)
- Fixed compilation under macos10.15 with Python 3.8 (PR #102)
- Fixed `numpy` 1.20 deprecation warning (PR #97)
- Updated CHANGELOG and version (PR #91, #103)

2.3.1
-----

- Fixed support of wheel package version >= 0.35 (PR #82)
- Fixed typo in error log (PR #81)
- Continuous integration: Added check of package description (PR #80)
- Fixed handling of version info (PR #84)

2.3
---

- Added ZFP filter (PR #74, #77)
- Updated README (PR #76, #79)

2.2
---

- Added FCIDECOMP filter (PR #68, #71)

2.1.2
-----

- Fixed OpenMP compilation flag (PR #64)
- Fixed support of `wheel` package version >= 0.34 (PR #64)
- Continuous Integration: Run tests with python3 on macOS rather than python2. (PR #66)

2.1.1
-----

- Fixed `--native` build option on platform other than x86_64 (PR #62)
- Fixed build of the snappy C++11 library for blosc on macOS (PR #60)

2.1.0
-----

- Added `--openmp=[False|True]` build option to compile bitshuffle filter with OpenMP. (PR #51)
- Added `--sse2=[True|False]` build option to compile blosc and bitshuffle filters with SSE2 instructions if available. (PR #52)
- Added `--avx2=[True|False]` build option to compile blosc and bitshuffle filters with AVX2 instructions if available. (PR #52)
- Added `--native=[True|False]` build option to compile filters for native CPU architecture. This enables SSE2/AVX2 support for the bitshuffle filter if available. (PR #52)
- Added snappy compression to the blosc filter if C++11 is available (`--cpp11=[True|False]` build option). (PR #54)
- Improved wheel generation by using root_is_pure=True setting. (PR #49)

2.0.0
-----

- Added compression support for Linux and macOS
- Added blosc filter
- Added helper class (Blosc, Bitshuffle and LZ4) to ease providing compression arguments to h5py
- Added tests
- Updated documentation
- Building from source through setup.py
- No longer use the plugin mechanism via HDF5_PLUGIN_PATH environment variable

1.4.1
-----

- Support Python 3.7 under 64-bit windows

1.4.0
-----

- Manylinux support

1.3.1
-----

- Support Python 3.6 under 64-bit windows.

1.3.0
-----

- Add 64-bit manylinux version LZ4 filter plugin

- Add 64-bit manylinux version bitshuffle plugin

- Implement continuous imtegration testing


1.2.0
-----

- Add LZ4 filter plugin for MacOS

- Add bitshuffle plugin decompressor for MacOS

1.1.0
-----

- Add bitshuffle plugin.

- Document origin and license of the used sources.

1.0.1
-----

- Replace corrupted VS2015 64 bit dll.

1.0.0
-----

- Initial release with LZ4 filter plugin.
