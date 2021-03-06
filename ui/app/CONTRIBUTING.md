# Contributing

This document describes how to:

- Set up your dev environment
- Become familiar with [Elm](http://elm-lang.org/)
- Develop against AlertManager

## Dev Environment Setup

- Elm is [installed](https://guide.elm-lang.org/install.html#install)
- Your editor is [configured](https://guide.elm-lang.org/install.html#configure-your-editor)
- [elm-format](https://github.com/avh4/elm-format) is installed

**All submitted elm code must be formatted with `elm-format`**. Install and
execute it however works best for you. We recommend having formatting the file
on save, similar to how many developers use `gofmt`.

If you prefer, there's a make target available to format all elm source files:

```
# make format
```

Once you've installed Elm, install the dependencies listed in
`elm-package.json`:

```
# elm package install -y
```

## Elm Resources

- The [Official Elm Guide](https://guide.elm-lang.org/) is a great place to
  start. Going through the entire guide takes about an hour, and is a good
  primer to get involved in our codebase. Once you've worked through it, you
  should be able to start writing your feature with the help of the compiler.
- Check the [syntax reference](http://elm-lang.org/docs/syntax) when you need a
  reminder of how the language works.
- Read up on [how to write elm code](http://elm-lang.org/docs/style-guide).
- Watch videos from the latest [elm-conf](https://www.youtube.com/channel/UCOpGiN9AkczVjlpGDaBwQrQ)
- Learn how to use the debugger! Elm comes packaged with an excellent
  [debugger](http://elm-lang.org/blog/the-perfect-bug-report). We've found this
  tool to be invaluable in understanding how the app is working as we're
  debugging behavior.

## Local development workflow

At the top level of this repo, follow the HA AlertManager instructions. Compile
the binary, then run with `goreman`. Add example alerts with the file provided
in the HA example folder.

```
# cd ui/app
# elm-reactor -p <port>
```

Your app should be available at `http://localhost:<port>`. Navigate to
`src/Main.elm`. Any changes to the file system are detected automatically,
triggering a recompile of the project.
