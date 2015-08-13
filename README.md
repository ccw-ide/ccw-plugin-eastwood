# ccw-plugin-eastwood

This Counterclockwise plugin integrates the Eastwood lint tool (https://github.com/jonase/eastwood) with Counterclockwise.

This plugin's state is production ready.

## Install

The `~/.ccw/` folder is where Counterclockwise searches for User Plugins.

It is recommended to layout User Plugins inside this folder by mirroring Github's namespacing. So if you clone ccw-ide/ccw-plugin-eastwood, you should do the following:

- Create a folder named `~/.ccw/ccw-ide/`
- Clone this project from `~/.ccw/ccw-ide/`

        mkdir -p ~/.ccw/ccw-ide
        cd ~/.ccw/ccw-ide
        git clone https://github.com/ccw-ide/ccw-plugin-eastwood.git

- If you have already installed ccw-plugin-manager (https://github.com/ccw-ide/ccw-plugin-manager.git), then type `Alt+U S` to re[S]tart User Plugins (and thus ccw-plugin-eastwood will be found and loaded)
- If you have not already installed ccw-plugin-manager, restart your Eclipse / Counterclockwise/Standalone instance.

## Usage

Use `Cmd+U E` on OS X, `Ctrl+U E` on Windows/Linux when the focus is on the Package Explorer or on an Editor.

This will start Leiningen for the project, and run the 'eastwood' task. A console view will be created, and you'll be able to see the output from the `lein eastwood` task. The plugin will then automatically convert Eastwood hints to Eclipse Problem Markers with a `warning` severity.

## License

Copyright © 2009-2015 Laurent Petit

Distributed under the Eclipse Public License, the same as Clojure.

