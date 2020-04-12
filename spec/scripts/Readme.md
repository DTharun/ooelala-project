Utility scripts for running SPEC CPU 2017 benchmarks

1. Copy scripts to SPEC CPU 2017 install directory
2. ./<script>

moveStats.sh - move .stats files generated inside the benchmark build directories to specified directory
Note - it will move ALL the stats files and separate them according to the config "label" and "tuning" they were generated by

buildSpec.sh - build SPEC CPU 2017 intrate and fprate benchmarks and move the stats the generated to \<pwd\>/intrate_\<timestamp\> and \<pwd\>/fprate_\<timestamp\>

runSpec.sh - run the SPEC CPU 2017 intrate and fprate benchmarks (3 iterations each)
Note - add `--rebuild` to the runcpu commands to regenerate build files (will also regenerate the stats)

buildUBS.sh - build SPEC CPU 2017 intrate and fprate benchmarks with UBSAN checks and without optimisation passes. Move the stats the generated to \<pwd\>/intrate_\<timestamp\> and \<pwd\>/fprate_\<timestamp\>

runUBS.sh - run the SPEC CPU 2017 intrate and fprate benchmarks (3 iterations each), which have been built with UBSAN checks and without optimisations. Note - add `--rebuild` to the runcpu commands to regenerate build files (will also regenerate the stats)

compareStats.py - compare stat files generated by clang and ooelala(clang-unseq)
Note - use `python compareStats.py -h` for usage instructions