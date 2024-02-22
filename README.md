# asyncomplete-mocword.vim

Provides intelligent English autocomplete for asyncomplete.vim via mocword.

## Screenshot

![screenshot.gif](images/screenshot.gif)

## Installing

```vim
Plug 'prabirshrestha/asyncomplete.vim'
Plug 'phongnh/asyncomplete-mocword.vim'
```

You also need to install [Mocword](https://github.com/high-moctane/mocword) and
[Mocword-data](https://github.com/high-moctane/mocword-data).

### Registration

```vim
call asyncomplete#register_source(asyncomplete#sources#mocword#get_source_options({
            \   'name': 'mocword',
            \   'allowlist': ['*'],
            \   'args': ['--limit', '100'],
            \   'completor': function('asyncomplete#sources#mocword#completor')
            \   }))
```

Note: `args` is optional. It will be passed as the `mocword` arguments.

## Contributors

- high-moctane ([https://github.com/high-moctane](https://github.com/high-moctane))
- Rafael Bodill ([https://github.com/rafi](https://github.com/rafi))

## License

MIT
