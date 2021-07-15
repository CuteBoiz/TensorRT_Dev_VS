## Add TensorRT and OpenCV to Project

- Open Visual Studio and Change to `Release` or `Debug` which you've built OpenCV.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/Vsyi8Df.png">
</p>

- Right click on `Solution Name` -> `Properties`. Set `Configuration` to `All Configurations` and `Platform` to `Active(x64)` -> OK.
<p align="center">
  <img width="70%" height="70%" src="https://i.imgur.com/fHGQCrO.png">
</p>

- Right click on `Solution Name` -> `Build Dependencies` -> `Build Customization...`.

- Select `CUDA 1x.x` built OpenCV and TensorRT -> `OK`
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/kYEDy7M.png">
</p>

- Right click on `Solution Name` -> `Properties`.

- At `CUDA C/C++` tab change `Target Machine Platform` to `64-bit (--machine 64)`.
<p align="center">
  <img width="70%" height="70%" src="https://i.imgur.com/ohU5v61.png">
</p>

- At `C/C++` Tab -> `General` -> `Additional Include Directories` -> `<Edit...>`.
<p align="center">
  <img width="70%" height="70%" src="https://i.imgur.com/lcGAWVR.png">
</p>

- Add `TensorRT\include` and `OpenCV\build\install\include` folders:
<p align="center">
  <img width="40%" height="40%" src="https://i.imgur.com/Otj0bgN.png">
</p>

- At `Linker` Tab -> `Input` -> `Additional Dependencies` -> `<Edit...>`
<p align="center">
  <img width="70%" height="70%" src="https://i.imgur.com/GO6hPuZ.png">
</p>

- Add `cudart.lib`, `TensorRT\lib\*.lib` and `OpenCV\build\install\x64\vc15\lib\*.lib` files:
<p align="center">
  <img width="40%" height="40%" src="https://i.imgur.com/3ZRkff8.png">
</p>

- At `C/C++` Tab -> `Preprocessor` -> `Preprocessor Definitions` -> Add `_CRT_SECURE_NO_WARNINGS`.
<p align="center">
  <img width="40%" height="40%" src="https://i.imgur.com/kzC8OyF.png">
</p>

- Done!
