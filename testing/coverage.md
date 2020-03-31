# Coveralls

# To build coverage info
```bash
cmake -DCMAKE_BUILD_TYPE=DEBUG -DCI=ON -DHIGHS_COVERAGE=ON ..
make -j4
make ci_cov
```

