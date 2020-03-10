```bash
# sudo passwd
sudo apt update
sudo apt install nodejs build-essential cmake
sudo apt install python-dev python-pip python3-dev python3-pip
curl https://install.meteor.com/ | sh
sudo apt install npm
sudo npm install -g express-generator typescript gulp
sudo apt install unzip zsh
sudo sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

# for dialog with db:
# git clone https://github.com/cromaLab/dialog2db
# wget -O file "https://drive.google.com/uc?export=download&id=11icoH_EA-NYb0OrPTdehRWm_d7-DIzWX"
# unzip file

# open .zshrc:
# ZSH_THEME="agnoster"
# DEFAULT_USER=$USER

# install nvim:
sudo add-apt-repository ppa:neovim-ppa/stable
sudo apt-get update
sudo apt-get install neovim
curl -fLo ~/.config/nvim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
# open nvim and install plug #
cd ~/.local/share/nvim/plugged/youcompleteme
python3 install.py --clang-completer --ts-completer

git config --global user.name "lizihan"
git config --global user.email "lizihan@umich.edu"
```

.init.vim

```bash
call plug#begin('~/.local/share/nvim/plugged')
Plug 'patstockwell/vim-monokai-tasty'
Plug 'scrooloose/nerdtree'
Plug 'tiagofumo/vim-nerdtree-syntax-highlight'
Plug 'jistr/vim-nerdtree-tabs'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
Plug 'jiangmiao/auto-pairs'

Plug 'terryma/vim-multiple-cursors'
Plug 'scrooloose/nerdcommenter'
Plug 'tpope/vim-surround'
Plug 'junegunn/fzf'
Plug 'valloric/youcompleteme'

"for html"
Plug 'mattn/emmet-vim'
Plug 'digitaltoad/vim-jade'
Plug 'elzr/vim-json'
Plug 'pangloss/vim-javascript'

call plug#end()

set encoding=UTF-8

syntax enable
let g:vim_monokai_tasty_italic = 1
colorscheme vim-monokai-tasty

set list listchars=extends:❯,precedes:❮,tab:▸\ ,trail:˽
set number
set wrap linebreak nolist
set breakindent
set breakindentopt=shift:2

"tab related"
set smarttab
set tabstop=4
set shiftwidth=4
set expandtab

let g:NERDTreeFileExtensionHighlightFullName = 1
let g:NERDTreeExactMatchHighlightFullName = 1
let g:NERDTreePatternMatchHighlightFullName = 1
let g:NERDTreeWinSize=20
let g:nerdtree_tabs_open_on_console_startup=1

"key mapping:
map <C-j> <C-W>j
map <C-k> <C-W>k
map <C-h> <C-W>h
map <C-l> <C-W>l

nnoremap <C-o> :m .+1<CR>==
nnoremap <C-i> :m .-2<CR>==
inoremap <C-o> <Esc>:m .+1<CR>==gi
inoremap <C-i> <Esc>:m .-2<CR>==gi
vnoremap <C-o> :m '>+1<CR>gv=gv
vnoremap <C-i> :m '<-2<CR>gv=gv

map <C-Left> <Esc>gT
map <C-Right> <Esc>gt

```

.screenrc

```
term screen-256color
```

