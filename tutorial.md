### Requirements
- vim (with vundle)
- clang as c++ compiler
- clangd
- YCM
- Python3

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

### Vim configuration
" Let clangd fully control code completion
let g:ycm_clangd_uses_ycmd_caching = 0

" Use installed clangd, not YCM-bundled clangd which doesn't get updates.
let g:ycm_clangd_binary_path = exepath("clangd")



