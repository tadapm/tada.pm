+++
title = "Tada - Ada Package Manager"
+++

### About

Tada handles building, testing, and running Ada packages. It wraps GNAT compiler and GPRbuild build system with sensible defaults. Tada uses a simple package manifest (`tada.toml`), so you spend less time writing build scripts and more time writing Ada.

Tada supports:

* Linux x86_64
* Linux aarch64
* MacOS aarch64
* OpenBSD x86_64
* Windows x86_64

### New to Ada?

Start with [Ada Programming on Wikibooks](https://en.wikibooks.org/wiki/Ada_Programming) or [Learn Ada on AdaCore](https://learn.adacore.com).

### Quick start

Prerequisites:

* `curl`
* `gnat`
* `gprbuild`

Download Tada:

<div class="text-center">
    <nav>
        <ul>
            <li><a href="https://github.com/tomekw/tada/releases/download/v0.11.0/tada-0.11.0-linux-x86_64" target="_blank" class="button">Linux x86_64</a></li>
            <li><a href="https://github.com/tomekw/tada/releases/download/v0.11.0/tada-0.11.0-windows-x86_64" target="_blank" class="button">Windows x86_64</a></li>
            <li><a href="https://github.com/tomekw/tada/releases/download/v0.11.0/tada-0.11.0-macos-aarch64" target="_blank" class="button">MacOS aarch64</a></li>
            <li><a href="https://github.com/tomekw/tada/releases/download/v0.11.0/tada-0.11.0-linux-aarch64" target="_blank" class="button">Linux aarch64</a></li>
            <li><a href="https://github.com/tomekw/tada/releases/download/v0.11.0/tada-0.11.0-openbsd7.8-x86_64" target="_blank" class="button">OpenBSD 7.8 x86_64</a></li>
        </ul>
    </nav>
    <span class="text-center"><small>Version 0.11.0</small></span>
</div>

Create a new project:

``` shell
$ tada init --name my_project --type exe
```

Install dependencies:

``` shell
$ tada install
```

Build it:

``` shell
$ tada build --profile debug
```

Test it:

``` shell
$ tada test
```

Run it:

``` shell
$ tada run -p release
```

Full usage:

``` shell
$ tada --help
```

### Adding dependencies

Edit `tada.toml`:

``` toml
[package]
name = "foo"
version = "0.1.0"

[dependencies]
bar = "0.5.2"
baz = "1.2.1"

[dev-dependencies]
testy = "0.2.0"
```

### Packages

| Package | Version | Website | Description |
|---------|---------|---------|-------------|
| `padlock` | `0.3.0` | [https://github.com/tomekw/padlock](https://github.com/tomekw/padlock) | libtls in Ada |
| `tackle` | `0.3.0` | [https://github.com/tomekw/tackle](https://github.com/tomekw/tackle) | Tomek's Ada Class Library |
| `testy` | `0.2.0` | [https://github.com/tomekw/testy](https://github.com/tomekw/testy) | Ada testing framework |

### Existing sofware

| Name | Version | Website | Description |
|---------|---------|---------|-------------|
| `twins` | `0.4.0` | [https://github.com/tomekw/twins](https://github.com/tomekw/twins) | Gemini server |

### Rationale

Tada is a project for personal use. I know Alire exists, is more feature rich and has hundreds of packages. And that's fine. Tada is something I always wanted to build. I write Ada for fun and decided to build many projects in it to understand how the foundational pieces work under the hood. I plan to release more projects in Ada in the near future, and I want to create my own little programming world around the language. I hope someone finds it useful.
