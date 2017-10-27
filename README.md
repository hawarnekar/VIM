# vim-config

Install following VIM plugins/scripts

* [pathogen](https://github.com/tpope/vim-pathogen)
* [Vundle](https://github.com/VundleVim/Vundle.vim)
* [NERDTree](https://github.com/scrooloose/nerdtree.git)
* [taglist.vim](http://www.vim.org/scripts/script.php?script_id=273)

Update (or create and edit) ~/.vimrc file as follows:

'''
" Required for Vundle                                
set nocompatible                                     
filetype off                                         
set rtp+=~/.vim/bundle/Vundle.vim                    
call vundle#begin()                                  
Plugin 'VundleVim/Vundle.vim'                        
call vundle#end()                                    

" Required for pathogen
execute pathogen#infect()

" Basic vim setup
set shell=/bin/bash
set path+=**       
set nowrap         
set ts=4           
set sts=4          
set sw=4           
set expandtab      
set cin            
set incsearch      
set nowrapscan     
set showcmd        
set ignorecase     
set autoindent
set smartindent
set showmatch
set nofoldenable
set nobackup
set nowb
set noswapfile
filetype plugin indent on
color desert
set cursorline
hi CursorLine term=bold cterm=bold guibg=Grey40

" Initializations
autocmd vimenter * NERDTree | wincmd p
autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTree") && b:NERDTree.isTabTree()) | q | endif
let g:NERDTreeWinPos="right"
let g:NERDTreeWinSize=30

" Colors and syntax setup
syntax enable
set background=light
let g:solarized_termcolors=256
colorscheme solarized

" Key mapping
nnoremap <silent> > :exe "vertical resize +20 " <CR>
nnoremap <silent> < :exe "vertical resize -20 " <CR>
nnoremap <silent> ++ :exe "resize +10 " <CR>
nnoremap <silent> -- :exe "resize -10 " <CR>
nnoremap <silent> <c-up> <C-W><C-K>
nnoremap <silent> <c-down> <C-W><C-J>
nnoremap <silent> <c-left> <C-W><C-H>
nnoremap <silent> <c-right> <C-W><C-L>
nnoremap <silent> <c-s> :w!<CR>
nnoremap <silent> <c-q> :q!<CR>
map <F2> :TlistToggle <CR>
map <F3> *
map <F4> :NERDTreeToggle <CR>
map <F1> :sh <CR>
'''
