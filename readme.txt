Add BSD license to source code

1) Install licensecheck
sudo apt-get install devscript

2) Check for files with missing license with:
find . -name "*.py" | xargs licensecheck

3) Use ros_add_license to add license information
./ros_add_license --help
usage: ros_add_license [-h] [-f] [-t TYPE] [-l LICENSE] [-d DIRECTORY] file

Utility to add license information to source files.

positional arguments:
  file                  source file

optional arguments:
  -h, --help            show this help message and exit
  -f, --force           Dont ask
  -t TYPE, --type TYPE  source type (auto/python/cpp)
  -l LICENSE, --license LICENSE
                        license file (default license_[mode].txt)
  -d DIRECTORY, --directory DIRECTORY
                        location of license files

Just add -d to define where the license files are.
E.g.
./ros_add_license -d ../licenses ~/my_source_file.cpp
