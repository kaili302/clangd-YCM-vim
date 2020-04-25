### Installation
**Install clangd**
```bash
sudo apt install clangd
```
**Install YouCompleteMe in vim with vundle**

Plugin 'Valloric/YouCompleteMe'

**Compile YCM with clangd as completion engine**
```bash
cd ~/.vim/bundle/YouCompleteMe
python3 install.py --clangd-completer
```

### Setup LSP for C++
**Use cmake to generate compilation database**
Add -DCMAKE_EXPORT_COMPILE_COMMANDS=ON when configuring (or add set( CMAKE_EXPORT_COMPILE_COMMANDS ON ) to CMakeLists.txt) and copy or symlink the generated database, *compile_commands.json*, to the root of the project.

### Use YCM
