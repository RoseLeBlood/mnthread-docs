# Mini Thread 2.10.x Documentation
Mini Thread is a library for creating secure threads for the esp32 microcontroller. 
With variable condition support if required. 
And wrappers for:  
   +  Mutex (recursive and standard)
   +  Semaphore (binary and counting)
   +  Queues (deque, binary-queue and the standard queue)
   +  workqueues (multithreaded and singlethreaded workqueues)
   +  Timers, Protothreads and event groups

The license that applies to the library is the LGPL.The license texts of these
licenses can be found in the files [LICENSE](https://github.com/RoseLeBlood/mnthread/LICENSE.md) of the
source code archive.

More On github: [mnthread](https://github.com/RoseLeBlood/mnthread) Version 2.10

## Using 
Build from git from
1. ```sh ./configure or ./configure --prefix=<path> # without prefix then install to /opt```
2. ```sh make build ```
3. ```sh sudo or doas make install ```
4. add  "lib_deps = /opt/miniThread/miniThread-2.*.tar.gz"  to your platformio.ini
 
### Example
```ini
[env:esp-wrover-kit]
platform = espressif32
board = esp-wrover-kit
framework = espidf
lib_deps = /opt/miniThread/miniThread-2.*.tar.gz

```
## Using from platformio
```ini
# platformio.ini – project configuration file

[env:my_build_env]
platform = espressif32
framework = espidf
lib_deps =
  # RECOMMENDED
  # Accept new functionality in a backwards compatible manner and patches
  roseleblood/mini Thread @ ^2.10.7

  # Accept only backwards compatible bug fixes
  # (any version with the same major and minor versions, and an equal or greater patch version)
  roseleblood/mini Thread @ ~2.10.7

  # The exact version
  roseleblood/mini Thread @ 2.10.7

```
