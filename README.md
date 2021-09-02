# libaptX
Open source replacement for proprietary Qualcomm aptX libraries on Android

## Building with Android
1. `git clone https://github.com/notmyst33d/libaptX external/aptx`
2. Add following to your `device.mk`:
```
PRODUCT_PACKAGES += \
    libaptX_encoder \
    libaptXHD_encoder
```

## Building with NDK
You should have Android NDK installed on your system
1. `git clone https://github.com/notmyst33d/libaptX`
2. `cd libaptX`
3. `mkdir build`
4. `cd build`
5. `cmake -DCMAKE_TOOLCHAIN_FILE=(path to Android NDK)/build/cmake/android.toolchain.cmake -DANDROID_PLATFORM=21 -DANDROID_ABI=arm64-v8a ..`
6. `make`

After this you should get `libaptX_encoder.so` and `libaptXHD_encoder.so` library  
Note: Change `-DANDROID_ABI=arm64-v8a` to `-DANDROID_ABI=armeabi-v7a` if you want to build this library for ARM instead of ARM64

## Credits
libaptX_encoder: https://github.com/Arkq/openaptx/tree/master/src/aptx422  
libaptXHD_encoder: https://github.com/Arkq/openaptx/tree/master/src/aptxhd100
