
# modified
- Add open waveform by gtkwave command/button.
- Work on systemverilog too.


# Verilog Testbench Runner
[![](https://img.shields.io/badge/license-MIT-orange.svg?style=flat-square)](http://opensource.org/licenses/MIT)
[![](https://img.shields.io/static/v1?label=Icarus&message=Verilog&color=f368e0&style=flat-square)](https://github.com/steveicarus/iverilog)

**Currently, only `iverilog` is supported.**

A simple extension to run single file Verilog testbenches with GTKWave integration. Hassle-free, portable, easy to configure. Combines the best bits of everything out there.

## Usage

This extension adds two buttons, which will appear in the titlebar of any Verilog file, and a status item positioned in the lower-right corner.

Be sure you have `iverilog` and `gtkwave` added to your environment PATH variable. If you need help, check out the installation guide [here](https://iverilog.fandom.com/wiki/Installation_Guide) (and for [Windows](http://bleyer.org/icarus/)).

## Features

### 1. Simple to use buttons:

<img src="https://raw.githubusercontent.com/TheOneKevin/icarusext/master/images/screen1.PNG"></img>

### 2. Live rough logic gate estimates:

<img src="https://raw.githubusercontent.com/TheOneKevin/icarusext/master/images/screen2.PNG"></img>

<img src="https://raw.githubusercontent.com/TheOneKevin/icarusext/master/images/screen3.PNG"></img>

### 3. Simple GTKWave integration:

<img src="https://raw.githubusercontent.com/TheOneKevin/icarusext/master/images/screen4.PNG"></img>

## Configuration

- `verilog.gtkwaveWatchGlob`: GTKWave will be summoned when a file satisfying the glob is created (glob is relative to the build directory).
- `verilog.icarusCompileArguments`: Arguments passed to Verilog compiler.
- `verilog.icarusBuildDirectory`: Build folder path relative to workspace root.
- `verilog.icarusPersistentBuild`: True if build folder should not be cleared before each compilation.

## Commands

- `icarusext.run` : Compiles and runs current file
- `icarusext.stop` : Stops and kills any running processes.
- `icarusext.tsizer` : Obtains **very rough** estimates for logic components. Will run on these events:
    - `window.onDidChangeActiveTextEditor`
    - `workspace.onDidSaveTextDocument`
    - Status item click (will show modal in this case)
    - When command `icarusext.run` is run

## License

Code is licensed under MIT.

> "Logo made by Freepik from www.flaticon.com (Flaticon license with attribution)"
