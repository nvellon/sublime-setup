Sublime 3 Setup
===============


Install Package Control
-----------------------

Follow instructions from https://sublime.wbond.net/installation


Install Extra Packages
----------------------

- Color Highlighter
- ColorPicker
- Phpcs
- PhpDoc
- SFTP
- SublimeCodeIntel
- Theme - Phoenix


Theme
-----

- Phoenix: https://sublime.wbond.net/packages/Theme%20-%20Phoenix
- Scheme: Phoenix Dark Blue


Custom Settings
---------------

Settings - User:

    {
        "color_scheme": "Packages/Theme - Phoenix/Color Scheme/Phoenix Dark Blue.tmTheme",
        "draw_white_space": "all",
        "ignored_packages":
        [
            "Vintage"
        ],
        "show_encoding": true,
        "show_line_endings": true,
        "tab_size": 4,
        "theme": "Phoenix Dark.sublime-theme",
        "translate_tabs_to_spaces": true,
        "trim_trailing_white_space_on_save": true,
        "use_tab_stops": true
    }

Key Bindings - User:

    [
        { "keys": ["ctrl+tab"], "command": "next_view" },
        { "keys": ["ctrl+shift+tab"], "command": "prev_view" },
        { "keys": ["ctrl+space"], "command": "auto_complete" },
        { "keys": ["ctrl+space"], "command": "replace_completion_with_auto_complete", "context":
            [
                { "key": "last_command", "operator": "equal", "operand": "insert_best_completion" },
                { "key": "auto_complete_visible", "operator": "equal", "operand": false },
                { "key": "setting.tab_completion", "operator": "equal", "operand": true }
            ]
        }
    ]

Package Settings - PHP Code Sniffer - Settings - User:

    {
        "show_debug": true,

        "phpcs_php_path": "/usr/bin/php",

        "phpcs_executable_path": "/home/nvellon/.composer/vendor/bin/phpcs",

        "phpcs_additional_args": {
            "--standard": "/home/nvellon/repos/ruleset.xml"
        }
    }

Package Settings - SublimeCodeIntel - Settings - User:

    {
        "codeintel_config": {
            "JavaScript": {
                "javascriptExtraPaths": [],
                "codeintel_scan_files_in_project": false,
                "codeintel_max_recursive_dir_depth": 2
            },
            "PHP": {
                "phpExtraPaths": [],
                "codeintel_scan_files_in_project": true,
                "codeintel_max_recursive_dir_depth": 10
            }
        }
    }