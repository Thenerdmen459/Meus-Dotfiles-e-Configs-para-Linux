
# 💻 Dotfiles e Configs

Repositório com todas as minhas configurações pessoais para Linux Mint:

- ✅ Vim (com plugins e tema Sonokai)
- ✅ Terminal (Linux Mint Terminal ou Terminator, WezTerm, etc.)
- ✅ WezTerm
- ✅ Linguagens: Python, C#, HTML, CSS, JavaScript

---

## 🎨 Plugins do Vim

- [vim-plug](https://github.com/junegunn/vim-plug)
- [Sonokai](https://github.com/sainnhe/sonokai)
- [NERDTree](https://github.com/preservim/nerdtree)
- [fzf](https://github.com/junegunn/fzf)
- [fzf.vim](https://github.com/junegunn/fzf.vim)
- [vim-commentary](https://github.com/tpope/vim-commentary)
- [vim-surround](https://github.com/tpope/vim-surround)
- [vim-gitgutter](https://github.com/airblade/vim-gitgutter)

---

## ⚡ Instalar plugins no Vim

```bash
sudo apt install curl
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

Depois, abra o Vim e rode:

```vim
:PlugInstall
```

---

## 📄 Configuração do Vim (.vimrc)

```vim
" ----------------------------
" Plugins (vim-plug)
" ----------------------------
call plug#begin('~/.vim/plugged')

Plug 'sainnhe/sonokai'
Plug 'preservim/nerdtree'
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
Plug 'junegunn/fzf.vim'
Plug 'tpope/vim-commentary'
Plug 'tpope/vim-surround'
Plug 'airblade/vim-gitgutter'

call plug#end()

syntax on
filetype plugin indent on

set number
set relativenumber
set tabstop=4
set shiftwidth=4
set expandtab
set smartindent
set smartcase
set ignorecase
set incsearch
set scrolloff=8
set signcolumn=yes
set termguicolors

let g:sonokai_style = 'andromeda'
let g:sonokai_enable_italic = 1
let g:sonokai_disable_italic_comment = 0
let g:sonokai_diagnostic_line_highlight = 1
let g:sonokai_current_word = 'bold'

colorscheme sonokai

set splitright
set splitbelow

nnoremap <C-n> :NERDTreeToggle<CR>
nmap <C-/> gcc

set mouse=a
set encoding=utf-8
```

---

## ⚙️ Configuração Linux Mint

### Distro

- Linux Mint 21.x (baseado no Ubuntu 22.04)

### Programas

- Python 3
- Node.js (via nvm)
- Git
- curl
- Vim

### Alias úteis

```bash
alias gs='git status'
alias ga='git add .'
alias gc='git commit -m'
alias gp='git push'
```

### Comandos para atualizar

```bash
sudo apt update && sudo apt upgrade
```

### Instalar curl

```bash
sudo apt install curl
```

### Instalar Python

```bash
sudo apt install python3 python3-pip
```

### Instalar Node.js via nvm

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install --lts
```

### Instalar Vim

```bash
sudo apt install vim
```

---

## 🖥️ Configuração do WezTerm

```lua
local wezterm = require 'wezterm'

return {
  font = wezterm.font 'JetBrains Mono',
  font_size = 12.0,
  color_scheme = 'Sonokai',
  enable_tab_bar = false,
  window_background_opacity = 0.9,
  use_fancy_tab_bar = false,
  default_prog = { "/usr/bin/bash", "-l" },
  default_cwd = "/home/seu-usuario/projetos",
}
```

---

## 🚀 Linguagens que eu uso

- Python
- C#
- HTML & CSS
- JavaScript

---

## ⚡ Comandos úteis no Linux Mint

### Atualizar pacotes

```bash
sudo apt update && sudo apt upgrade
```

### Instalar curl

```bash
sudo apt install curl
```

### Instalar Python

```bash
sudo apt install python3 python3-pip
```

### Instalar Node.js via nvm

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install --lts
```

### Instalar Vim

```bash
sudo apt install vim
```

### Instalar vim-plug

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### Comandos git

```bash
git clone <repo>
git status
git add .
git commit -m "mensagem"
git push
```

---

## ✅ Como subir no GitHub

```bash
git init
git add .
git commit -m "Initial commit: dotfiles completos Linux Mint"
git branch -M main
git remote add origin https://github.com/seu-usuario/dotfiles.git
git push -u origin main
```

---

# 💬 Contato

Se quiser trocar ideias ou sugestões, me chama! 🚀🔥
