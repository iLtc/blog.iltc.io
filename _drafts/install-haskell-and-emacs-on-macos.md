# Install Haskell and Emacs on macOS

[Haskell](https://www.haskell.org/) is a purely functional programming language. I learned how to use it in my Programming Language Concepts class. Our professor asked us to use [Emacs](https://www.gnu.org/software/emacs/) to edit all the Haskell and [Agda](https://en.wikipedia.org/wiki/Agda_(programming_language)) code since there are plugins such as [Haskell Mode](https://github.com/haskell/haskell-mode) that can let Emacs highlight Haskell code and compile them when needed.

In this blog post, I will talk about how to install Haskell and Emacs on Mac. There are some tricky things we need to notice in order to be able to use Haskell Mode on Mac. If you are using Windows, you can download the single installer for everything provided by my professor [Aaron Stump](http://homepage.cs.uiowa.edu/~astump/) from [here](http://homepage.cs.uiowa.edu/~astump/agda/Agda2.5.2.msi).

We will also use [Homebrew](https://brew.sh/) to install Haskell and Emacs here. If you have not installed Homebrew yet, please copy and past the following code to terminal to install Homebrew:

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
``` 
 

## Install Haskell

I recommend installing Haskell Platform directly. It includes GHC, Cabal, and some other tools we may need to use later.

Copy and past the following code to Terminal to install Haskell Platform:

```bash
$ brew cask install haskell-platform
```

To make sure that Haskell is working correctly, we need to try ghci in terminal. Open a new terminal and type `ghci`. You should see something like this:

```bash
$ ghci
GHCi, version 8.2.2: http://www.haskell.org/ghc/  :? for help
Prelude>
```

Now let's try some command:

```bash
Prelude> 1 + 2
3
Prelude> 2 * 3
6
```

In the end, you can type `:q` to quit:

```bash
Prelude> :q
Leaving GHCi.
$
```

## Install Emacs

There are two ways to install Emacs.

The [Emacs download page](https://www.gnu.org/software/emacs/download.html#macos) recommends using Homebrew:

```bash
$ brew install emacs --with-cocoa
```

Meanwhile, if you install Emacs through Homebrew, it will take about five  to ten minutes to compile. If you do not want to wait for the compiling time, you can download a compiled version from [Emacs For Mac OS X](https://emacsformacosx.com/) website.

## Install and Set Up Haskell Mode

