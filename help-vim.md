# Help comandos

# Vim
Navegar entre janelas do vim:

Navegar entre arquivos

* Vai para o proximo: bn
* Volta  para anterior: bp
* Salva e vai para o proximo: wn
* Vai para o proximo da lista: wp

Tabs

:tabedit {file}   edit specified file in a new tab
:tabfind {file}   open a new tab with filename given, searching the 'path' to find it
:tabclose         close current tab
:tabclose {i}     close i-th tab
:tabs         list all tabs including their displayed windows
:tabm {i}     move current tab to position i+1
:tabn         go to next tab
:tabp         go to previous tab
gt            go to next tab
gT            go to previous tab
{i}gt         go to tab in position i

Abrir arquivo no vim: e [caminho do arquivo]

Copiando linha atual: yy

Copiando 5 linhas: 5yy

Colando : "+p

Colando o que estiver no clipboard: <Shift + Insert>

Deletando linha atual: dd

Deletando 5 linhas: 5dd

Desfaser: u

Desfazer nudanças na ultima linha editada: U

Refazer: <Ctrl + r>

Susbestituir palavras em todo o arquivo: % s/[antigo]/[novo]

Substituir palavras na linha atual: s/[antigo]/[novo]

Substituir palavras da linha 1 a 10: 1,10 s/[antigo]/[novo]

Substituir palavras da linha 1 até o final: 1,$ s/[antigo]/[novo]

Ignorando maisculas e minusculas na pesquisa: /\c[palavra]

n #next
N #previus

:noh #off marcação

plugins:

[pathogen.vim](https://github.com/tpope/vim-pathogen)
[ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)
[nerdtree](https://github.com/scrooloose/nerdtree)
[syntastic](https://github.com/scrooloose/syntastic)
[vim-hybrid](https://github.com/w0ng/vim-hybrid)
[vim-javascript](https://github.com/pangloss/vim-javascript)
[vim-javascript-syntax](https://github.com/jelera/vim-javascript-syntax)


## vimrc

execute pathogen#infect()                                                       

syntax on                                                                       
set t_Co=256                                                                    
filetype plugin indent on                                                       

set colorcolumn=80                                                              
set textwidth=80                                                                
autocmd BufRead *.md,*.txt set tw=100                                           
autocmd FileType c,cpp,java,groovy,javascript autocmd BufWritePre <buffer> %s/\s\+$//e

set tabstop=4                                                                   
set shiftwidth=4                                                                
set softtabstop=4                                                               
set expandtab                                                                   

set background=dark                                                             
colorscheme hybrid                                                              

let g:javascript_plugin_jsdoc = 1                                               

set statusline+=%#warningmsg#                                                   
set statusline+=%{SyntasticStatuslineFlag()}                                    
set statusline+=%*                                                              

let g:syntastic_always_populate_loc_list = 1                                    
let g:syntastic_auto_loc_list = 1                                               
let g:syntastic_check_on_open = 1                                               
let g:syntastic_check_on_wq = 0  
