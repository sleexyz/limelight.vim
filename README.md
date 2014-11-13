limelight.vim ![travis-ci](https://travis-ci.org/junegunn/limelight.vim.svg?branch=master)
=============

Hyperfocus-writing in Vim.

![](https://raw.github.com/junegunn/i/master/limelight.gif)

Best served with [Goyo.vim](https://github.com/junegunn/goyo.vim).
Works on 256-color terminal or on GVim.

## note
Forked from [junegunn/limelight.vim](https://github.com/junegunn/limelight.vim), to recognize `^#` as the delimiter for blocks for Markdown files.

In other words, for markdown files, blocking by sections defined by octothorpe-defined headers.

Doesn't support `=====` or `----` defined headers yet.

Hmm... maybe blocking specifications should be abstracted...

*To be continued...*


Usage
-----

- `Limelight [0.0 ~ 1.0]`
    - Turn Limelight on
- `Limelight!`
    - Turn Limelight off
- `Limelight!! [0.0 ~ 1.0]`
    - Toggle Limelight

### Options

For some color schemes, Limelight may not be able to calculate the color for
dimming down the surrounding paragraphs. In that case, you need to define
`g:limelight_conceal_ctermfg` or `g:limelight_conceal_guifg`.

```vim
" Color name (:help cterm-colors) or ANSI code
let g:limelight_conceal_ctermfg = 'gray'
let g:limelight_conceal_ctermfg = 240

" Color name (:help gui-colors) or RGB color
let g:limelight_conceal_guifg = 'DarkGray'
let g:limelight_conceal_guifg = '#777777'

" Default: 0.5
let g:limelight_default_coefficient = 0.7
```

Goyo.vim integration
--------------------

```vim
autocmd User GoyoEnter Limelight
autocmd User GoyoLeave Limelight!
```

Acknowledgement
---------------

Thanks to [@Cutuchiqueno](https://github.com/Cutuchiqueno) for [suggesting
the idea](https://github.com/junegunn/goyo.vim/issues/34).

License
-------

MIT
