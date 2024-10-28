# Atajos para Sublime Text

---
## Edición de texto

| **Atajo**                           | **Descripción**                                                  |
| ----------------------------------- | ---------------------------------------------------------------- |
| ctrl + d                            | Seleccionar palabras iguales del documento                       |
| ctrl + d                            | Duplicar la línea actual                                         |
| ctrl + l                            | Seleccionar la línea actual                                      |
| ctrl + shift + l                    | Seleccionar varias líneas                                        |
| ctrl + shift + j                    | Unir la línea actual con la siguiente                            |
| ctrl + shift + k                    | Eliminar la línea actual                                         |
| ctrl + clic                         | Editar múltiples líneas en ubicaciones específicas de las mismas |
| Shift + teclas direccionales        | Seleccionar texto en una de las cuatro direcciones               |
| alt + shift + teclas direccionales  | Editar multiples líneas                                          |
| ctrl + shift + teclas direccionales | Mover una línea de lugar                                         |

## Manipulación de archivos

| Atajo            | Descripción                |
| ---------------- | -------------------------- |
| ctrl + n         | Nuevo archivo              |
| ctrl + shift + t | Reabrir la pestaña cerrada |

## Búsqueda y remplazo

| Atajo            | Descripción                       |
| ---------------- | --------------------------------- |
| ctrl + f         | Buscar en el archivo actual       |
| ctrl + shift + f | Buscar en todo el proyecto        |
| ctrl + h         | Remplazar en el archivo actual    |
| ctrl + r         | Buscar selectores en archivos CSS |

## Configuraciones de Sublime Text
```json
// Settings in here override those in "Default/Preferences.sublime-settings",
// and are overridden in turn by syntax-specific settings.
{
	"font_size": 14,
	"font_face": "JetBrainsMono Nerd Font",
	"save_on_focus_lost": true,
	"highlight_line": true,
	"caret_style": "phase",
	"word_wrap": true,
	"line_padding_bottom": 12,
	"line_padding_top": 12,
	"theme": "Adaptive.sublime-theme",
	"color_scheme": "Packages/Aura Theme Color Scheme/aura-theme.tmTheme",
	"translate_tabs_to_spaces": true,
	"trim_trailing_white_space_on_save": "none",
	"ignored_packages":
	[
		"Package Control",
		"Vintage",
	],
	"index_files": true,
}
```

## Extensiones Sublime Text

- A File Icon
- All Autocomplete
- Auto File Name
- Bracket Highlighter
- Color Highlight
- CSS3
- GitGutter
- Emmet
- HTML-CSS-JS Prettify
- Javascript & NodeJS Snippets
- JsLint
- SideBarEnhancements
- SublimeCodeIntel
- SublimeLinter
- SublimeLinter-gcc
- Terminus
- SublimeLinter-html-tidy

### Terminus para `c`
```json
{
    "target": "terminus_exec",
    "cancel": "terminus_cancel_build",
    "shell_cmd": "gcc \"${file}\" -o \"${file_path}/${file_base_name}\"",
    "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir": "${file_path}",
    "selector": "source.c",

    "variants":
    [
        {
            "name": "Run",
            "shell_cmd": "gcc \"${file}\" -o \"${file_path}/${file_base_name}\" && \"${file_path}/${file_base_name}\""
        }
    ]
}
```