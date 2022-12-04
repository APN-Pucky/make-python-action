# make-python-action

A simple action to build, test, doc and publish python packages mainly through Makefile commandos.

## Flow and Options

|     | step                          | with condition           |  default       
|-----|-------------------------------|--------------------------|-----------------
|1.   | `make build`                  | `build:`                 | `true` 
|2.   | `make install`                | `install: `              |  `true`
|3.   | `make test`                   |  `test: `                |    `true`
|4.   | `make doc`                    |   `doc: `                |       `false`
|5.   | Report to Coveralls           |    `coveralls: `         |        `false`
|6.   | Report to Codacy              |    `codacy-api-token: `  |         
|     |                               |   `coverage-reports:`    |  `coverage.xml`                
|7.   | Deploy to Test PyPi           |  `test-pypi-token: `     |              
|8.   | Deploy to PyPi                |      `pypi-token: `      |           
|9.   | Upload Test to Github Pages   |   `test-gh-pages: `      |     `false`
|10.  | Upload to Github Pages        |   `gh-pages: `           |        `false`
|     |                               |   `gh-pages-branch:`     |  `gh-pages`    
|     |                               |   `gh-pages-folder:`     |  `docs/build/html`    
