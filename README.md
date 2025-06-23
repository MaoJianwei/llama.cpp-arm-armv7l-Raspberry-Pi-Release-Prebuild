# llama.cpp-arm-armv7l-Raspberry-Pi-Release-Prebuild

**On [the Releases page](https://github.com/MaoJianwei/llama.cpp-arm-armv7l-Raspberry-Pi-Release-Prebuild/releases), you can download pre-built binaries for arm, armv7l and Raspberry pi.**

.

Built on official codes @ [b5736](https://github.com/ggml-org/llama.cpp/releases/tag/b5736) tag.

Built on Respberry Pi 2B, adapt to all devices with **Arm CPU** (objective):
* CPU: **armv7l**
* OS: Raspbian 1:6.12.25-1+rpt1 (2025-04-30), Raspbian GNU/Linux **12 (bookworm)**
* Memory: **1G (ram)** + 4G (swap for build) 
* GLIBC version: ldd (Debian GLIBC 2.36-9+rpt2+deb12u12) **2.36**
* Device: Raspberry Pi 2B rev 1.1
* Device SoC: BCM2836

.

Build script obeys [official manual](https://github.com/ggml-org/llama.cpp/blob/master/docs/build.md), as follow:
```
cmake -B build -DBUILD_SHARED_LIBS=OFF
cmake --build build --config Release -j 3
```

![image](https://github.com/user-attachments/assets/7610d9b8-36cc-4f7b-9d67-f9ad6965942c)

![image](https://github.com/user-attachments/assets/2edbc3c4-d014-4e35-ab9f-3f9f386353ad)

.

**sha256sum ./build/bin/llama-server** output:
```
cfd32bd6d79f4954955cea7e9041f991bcd8ea5ab00485115c4ca8722be8bf50  ./build/bin/llama-server
```

**sha256sum ./build/all_bin.tar.gz** output:
```
76313f962c6795ff18948e2fa2ff06f1884ef1f4196f03256a5fcb8852d12f1d  ./build/all_bin.tar.gz
```

.

**ldd ./build/bin/llama-server** output:
```
        linux-vdso.so.1 (0x7edab000)
        /usr/lib/arm-linux-gnueabihf/libarmmem-${PLATFORM}.so => /usr/lib/arm-linux-gnueabihf/libarmmem-v7l.so (0x76fa0000)
        libcurl.so.4 => /lib/arm-linux-gnueabihf/libcurl.so.4 (0x76f02000)
        libgomp.so.1 => /lib/arm-linux-gnueabihf/libgomp.so.1 (0x76ec5000)
        libstdc++.so.6 => /lib/arm-linux-gnueabihf/libstdc++.so.6 (0x76d0d000)
        libm.so.6 => /lib/arm-linux-gnueabihf/libm.so.6 (0x76cc6000)
        libgcc_s.so.1 => /lib/arm-linux-gnueabihf/libgcc_s.so.1 (0x76ca9000)
        libc.so.6 => /lib/arm-linux-gnueabihf/libc.so.6 (0x76b30000)
        libnghttp2.so.14 => /lib/arm-linux-gnueabihf/libnghttp2.so.14 (0x76b0a000)
        libidn2.so.0 => /lib/arm-linux-gnueabihf/libidn2.so.0 (0x76adb000)
        librtmp.so.1 => /lib/arm-linux-gnueabihf/librtmp.so.1 (0x76ab0000)
        libssh2.so.1 => /lib/arm-linux-gnueabihf/libssh2.so.1 (0x76a60000)
        libpsl.so.5 => /lib/arm-linux-gnueabihf/libpsl.so.5 (0x76a4d000)
        libssl.so.3 => /lib/arm-linux-gnueabihf/libssl.so.3 (0x769c0000)
        libcrypto.so.3 => /lib/arm-linux-gnueabihf/libcrypto.so.3 (0x76670000)
        libgssapi_krb5.so.2 => /lib/arm-linux-gnueabihf/libgssapi_krb5.so.2 (0x7662e000)
        libldap-2.5.so.0 => /lib/arm-linux-gnueabihf/libldap-2.5.so.0 (0x765dd000)
        liblber-2.5.so.0 => /lib/arm-linux-gnueabihf/liblber-2.5.so.0 (0x765d0000)
        libzstd.so.1 => /lib/arm-linux-gnueabihf/libzstd.so.1 (0x76531000)
        libbrotlidec.so.1 => /lib/arm-linux-gnueabihf/libbrotlidec.so.1 (0x76500000)
        libz.so.1 => /lib/arm-linux-gnueabihf/libz.so.1 (0x764e8000)
        /lib/ld-linux-armhf.so.3 (0x76fbd000)
        libunistring.so.2 => /lib/arm-linux-gnueabihf/libunistring.so.2 (0x76330000)
        libgnutls.so.30 => /lib/arm-linux-gnueabihf/libgnutls.so.30 (0x7613e000)
        libhogweed.so.6 => /lib/arm-linux-gnueabihf/libhogweed.so.6 (0x760e0000)
        libnettle.so.8 => /lib/arm-linux-gnueabihf/libnettle.so.8 (0x76070000)
        libgmp.so.10 => /lib/arm-linux-gnueabihf/libgmp.so.10 (0x75fe0000)
        libatomic.so.1 => /lib/arm-linux-gnueabihf/libatomic.so.1 (0x76aa6000)
        libkrb5.so.3 => /lib/arm-linux-gnueabihf/libkrb5.so.3 (0x75f32000)
        libk5crypto.so.3 => /lib/arm-linux-gnueabihf/libk5crypto.so.3 (0x75f08000)
        libcom_err.so.2 => /lib/arm-linux-gnueabihf/libcom_err.so.2 (0x7652d000)
        libkrb5support.so.0 => /lib/arm-linux-gnueabihf/libkrb5support.so.0 (0x76522000)
        libsasl2.so.2 => /lib/arm-linux-gnueabihf/libsasl2.so.2 (0x75ed0000)
        libbrotlicommon.so.1 => /lib/arm-linux-gnueabihf/libbrotlicommon.so.1 (0x75e90000)
        libp11-kit.so.0 => /lib/arm-linux-gnueabihf/libp11-kit.so.0 (0x75d70000)
        libtasn1.so.6 => /lib/arm-linux-gnueabihf/libtasn1.so.6 (0x75d5e000)
        libkeyutils.so.1 => /lib/arm-linux-gnueabihf/libkeyutils.so.1 (0x75d30000)
        libresolv.so.2 => /lib/arm-linux-gnueabihf/libresolv.so.2 (0x760d1000)
        libffi.so.8 => /lib/arm-linux-gnueabihf/libffi.so.8 (0x75d00000)
```
