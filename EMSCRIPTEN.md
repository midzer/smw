# Emscripten

## Build

```
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions src/*.o src/snes/*.o smb1/*.o smbll/*.o third_party/gl_core/*.o -o index.html -sUSE_SDL=2 -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@funcs.txt -sENVIRONMENT=web --preload-file smw_assets.dat --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate','ALLOC_NORMAL']
```
