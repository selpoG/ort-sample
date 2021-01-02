# ort-sample

- [ort-sample](#ort-sample)
	- [Get `onnxruntime`](#get-onnxruntime)
	- [Build](#build)
	- [Run](#run)

## Get `onnxruntime`

Download `onnxruntime-<os>-<arch>(-gpu)-1.6.0.zip` from
[here](https://github.com/microsoft/onnxruntime/releases/tag/v1.6.0),
and extract it to anywhere you like.

## Build

```sh
git clone https://github.com/selpoG/ort-sample
mkdir ort-sample/build
cd ort-sample/build
cmake -DONNXRUNTIME_ROOT=<path to onnxruntime> ..
cmake --build .
```

## Run

Linux:

```sh
$ ./ort-sample
hello
```

Windows:

```pwsh
> ./Debug/ort-sample.exe
```
