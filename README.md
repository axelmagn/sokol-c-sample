# Sokol C Sample

A lightweight, simple starter template for C using [sokol](https://github.com/floooh/sokol) and [Nuklear](https://github.com/Immediate-Mode-UI/Nuklear). It draws a triangle alongside a Nuklear GUI control panel.

No CMake or build systems, just bash scripts.

## Getting Started

### Prerequisites

- **C Compiler**: `clang` (default) or `gcc`
- **Utilities**: `curl` & `tar` (for auto-downloading dependencies)
- **Linux**: OpenGL and X11 dev libraries (`libgl1-mesa-dev`, `libx11-dev`, `libxi-dev`, `libxcursor-dev`)
- **macOS**: Xcode Command Line Tools
- **Web target (optional)**: [Emscripten](https://emscripten.org/) (`emcc`) & `python3`

### Quickstart

Run the app right away:

```bash
./bin/run.sh
```

Dependencies (Sokol, Nuklear, and `sokol-shdc`) will auto-fetch on the first run. **NOTE**: for reliable builds, consider either:

1. configure a recent commit hash in `config.sh` to make sure you get the same files every time.
2. vendor `deps/` by removing it from `.gitinore` and checking it into git.

## Usage

### Building

Build using `bin/build.sh`:

```bash
./bin/build.sh              # build native binary
./bin/build.sh --web        # build web assembly target
./bin/build.sh --fetch-deps # (re)fetch sokol and nuklear
./bin/build.sh --clean      # clean build directory
```

### Running

Build and run in one step using `bin/run.sh`:

```bash
./bin/run.sh                    # build and run native binary
./bin/run.sh --web              # build and serve web target
./bin/run.sh --web --port 3000  # build and serve on a custom port
```

## Project Layout

- `src/main.c`: Application logic & Nuklear UI
- `shaders/`: GLSL shaders and generated header code
- `bin/`: Build, run, and config bash scripts
- `deps/`: Downloaded Sokol & Nuklear headers + `sokol-shdc`


## AI Usage Disclosure

This project was made with the assistance of LLM agents.  I find them useful.  I try to moderate my AI assistance, but if it bums you out then that's fair enough.
