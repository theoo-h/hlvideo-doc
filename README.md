# hlvideo

Hashlink video support

### Requirements
- AOM
- Visual Studio
- HashLink

## Building Dependencies
#### Windows Setup

- Download and build AOM from hlvideo root directory

for x64

```
git clone https://aomedia.googlesource.com/aom
mkdir aom_x64
cd aom_x64
cmake ../aom -DCMAKE_BUILD_TYPE=Release -G "Visual Studio xx 20xx" -T host=x64 -A x64
cmake --build . --config Release
```

or for win32

```
git clone https://aomedia.googlesource.com/aom
mkdir aom_x32
cd aom_x32
cmake ../aom -DCMAKE_BUILD_TYPE=Release -G "Visual Studio xx 20xx" -T host=x64
cmake --build . --config Release
```

- Define HASHLINK_SRC env var to point to your `hashlink` directory

#### OSX / Linux Setup

Just call make

```
make

## Building the Library

- Define HL_VIDEOPATH env var to point your `hlvideo` directory, normally %HAXEPATH%\libs\hlvideo\git

- Open `video.sln` with Visual Studio, then compile, once its complete, copy `video.hdll` and `video.lib` (which are going to be in x64/Debug) to your hashlink directory