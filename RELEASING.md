# Releasing

Once all the changes for a release have been merged to master, ensure the following:

- [ ] version has been updated in `src/opentelemetry/lightstep/version.py`
- [ ] tests are passing
- [ ] user facing documentation has been updated

# Publishing

Publishing to [pypi](https://pypi.org/project/opentelemetry-lightstep/) is automated via GitHub actions. Once a tag is pushed to the repo, a new GitHub Release is created and package is published  via the actions defined here: https://github.com/lightstep/otel-python/blob/master/.github/workflows/release.yml

```
$ git clone git@github.com:lightstep/otel-python && cd otel-python
# ensure the version matches the version beind released
$ cat src/opentelemetry/lightstep/version.py
__version__ = "0.0.1"
$ git tag v0.0.1 && git push origin v0.0.1
```
