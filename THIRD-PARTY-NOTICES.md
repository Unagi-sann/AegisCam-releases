# Third-Party Notices

Aegis Camera includes the following open-source components. Each is used under its own licence,
which applies to that component only; Aegis Camera itself is under the [beta licence](LICENSE.md).

All of them are licensed under the **Apache License, Version 2.0**; its full text is in
[LICENSES/Apache-2.0.txt](LICENSES/Apache-2.0.txt) and at <https://www.apache.org/licenses/LICENSE-2.0>.

| Component | Copyright |
| --- | --- |
| Android Jetpack (AndroidX): Activity, Annotation, Arch Core, Autofill, Collection, Concurrent, Core, CustomView, Emoji2, ExifInterface, Graphics, HeifWriter, Interpolator, Lifecycle, ProfileInstaller, SavedState, Startup, Tracing, VersionedParcelable | The Android Open Source Project |
| Jetpack Compose: Runtime, UI, Foundation, Animation, Material, Material 3, Material Icons | The Android Open Source Project |
| Guava ListenableFuture | The Guava Authors |
| Kotlin standard library | JetBrains s.r.o. and Kotlin Programming Language contributors |
| kotlinx.coroutines | JetBrains s.r.o. and contributors |
| JetBrains Java Annotations | JetBrains s.r.o. |

Material Icons are by Google, under the Apache License 2.0.

The app's native image processing (HDR+ and Super-res merges, denoising, tone mapping, styles)
is Aegis Camera's own code, written from published research:

- S. W. Hasinoff et al., "Burst photography for high dynamic range and low-light imaging on
  mobile cameras", ACM Transactions on Graphics 35(6), 2016.
- B. Wronski et al., "Handheld multi-frame super-resolution", ACM Transactions on Graphics
  38(4), 2019.

It links only to Android's own system libraries; the C++ runtime it includes (LLVM libc++) is
under the Apache License 2.0 with LLVM Exceptions, which requires no notice in compiled form.
