## OpenCV from source with CUDA support in Window

### I. Download.

- Create OpenCV folder at install place.

- Open Folder and Right Click.

- Choose `Git Bash Here`.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/1l8Jy5Z.png">
</p>

- Type `git clone https://github.com/opencv/opencv.git`.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/fmBWacp.png">
</p>

- Type `git clone https://github.com/opencv/opencv_contrib.git`.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/JCeDERJ.png">
</p>

- **Change Version (Optional):**
  - Use Git Bash in downloaded `opencv` folder Type `git checkout 4.4.0`.
  <p align="center">
    <img width="50%" height="50%" src="https://i.imgur.com/IzPcVdU.png">
  </p>
  
  - Use Git Bash in downloaded `opencv-contrib` folder Type `git checkout 4.4.0`.
  **Note:** Must be same version with above opencv version.
  <p align="center">
    <img width="50%" height="50%" src="https://i.imgur.com/OxAcxx8.png">
  </p>
  
### II. Install.

- Create build folder in OpenCV root folder.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/n5HyWdb.png">
</p>

- Open CMake. Set `Source code` is the downloaded opencv and `Where to build the binaries` is the build folder.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/wGOntHd.png">
</p>

- Click `Configure`. Choose Visual Studio version and `Optional platfrom for generator` is `x64`. Click `Finish`.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/4v4kl8r.png">
</p>

- Select `ENABLE_FAST_MATH`, `OPENCV_DNN_CUDA`, `WITH_CUDA`.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/iEMPEzM.png">
</p>

-	In `OPENCV_EXTRA_MODULES_PATH` Click on `...` sign and choose the downloaded **opencv_contrib/modules**.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/HCBBep2.png">
</p>

- Click `Configure`.

- Select `CUDA_FAST_MATH`.

- In CUDA_ARCH_BIN select compatible compute architectures for your model of GPU or all. Check the Compute capability (version) table [here](https://en.wikipedia.org/wiki/CUDA)
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/4I3aZJb.png">
</p>

- Click `Configure` again.

- `Generate`.
<p align="center">
  <img width="50%" height="50%" src="https://i.imgur.com/ei3lu5o.png">
</p>

- Close Cmake then go to **build** folder and open the `OpenCV.sln`.

-	Choose `Debug` or `Release` mode with `x64`.
<p align="center">
  <img src="https://i.imgur.com/ciyy7ry.png">
</p>

- Open solution explorer at right hand side. Expand the CmakeTargets. Right click on `ALL_BUILD` and select `build`.
<p align="center">
  <img  src="https://i.imgur.com/p02uyCX.png">
</p>

- Wait `ALL_BUILD` building complete. Then build the `INSTALL`.
- Set Path:
  - Open `Window + R` type `sysdm.cpl`
  
  - Open `Advanced` Tab.
  
  - `Environment Variables...`  
  
  -  In `System Variables` Tab find `Path`:
    <p align="center">
      <img width="50%" height="50%" src="https://i.imgur.com/6CYg60Q.png">
    </p>
  
  - Click `New` and Add the OpenCV_Directory/build/install/x64/vc15/bin 
  <p align="center">
    <img width="50%" height="50%" src="https://i.imgur.com/v97CPZq.png">
  </p>
  
  -  `Ok` 
  
  -  `Apply`
  
- Done!
