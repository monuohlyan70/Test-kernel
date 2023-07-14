# veux-kernelbuilder
## **Basic configuration**
Whether you're building on remote server or locally, you ***must*** set basic variables before running. They are located at the top of `build.config.veux`
- Recommended config:  
```
KERNEL_SOURCE=https://github.com/MiCode/Xiaomi_Kernel_OpenSource
KBRANCH="-b veux-r-oss"
DEFCONFIG=qgki_defconfig
```

## Build using Actions
1. Clone your source and run these:
```
git remote add bscript https://github.com/cachiusa/veux-kernelbuilder
git fetch bscript
git checkout <your-branch>
git merge bscript
git push
```
2. Settings tab > Actions > General > Allow all actions and reusable workflows > Save
3. Actions tab > Run workflow
4. Download the artifact. Flash it with your custom recovery
  
## Build on local host
```
git clone https://github.com/cachiusa/veux-kernelbuilder  
cd veux-kernelbuilder && ./build.sh
```
### Usage for `build.sh`:
- (leave empty)  => run everything from start to end
- `getsource`/`gettools`/`startbuild`/`finalize` => run a specific section of build process