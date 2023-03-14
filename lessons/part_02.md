# Go lessons

## Starting with GO. Intallation.

> The best way to learn GO is to start coding in it.

### Common way

To install Go, you can follow these steps:

1. Go to the official Go website (https://golang.org/) and download the appropriate installation package for your
   operating system.

2. Follow the installation instructions for your operating system. For example, on Linux, you can typically install Go
   by extracting the downloaded archive to /usr/local.

3. Once Go is installed, you need to set up your Go environment by setting the GOPATH environment variable. This
   variable specifies the location of your Go workspace, which is where Go will look for your source code and where it
   will place the compiled binaries. You can set the GOPATH variable to any directory you like, but it is common to set
   it to $HOME/go (i.e., a directory called "go" in your home directory).

4. Finally, you should add the Go binary directory to your system's PATH environment variable, so that you can use the
   Go tools from any directory. On Linux, you can do this by adding the following line to your ~/.bashrc file (assuming
   you installed Go to /usr/local/go):
    ```bash
    export PATH=$PATH:/usr/local/go/bin
    ```

Once you have completed these steps, you should be able to start using Go. You can test your installation by opening a
terminal window and typing `go version`. This should display the version number of the installed Go compiler.

### Install Go with Homebrew on a macOS

To install Go with **Homebrew on a macOS** system, follow these steps:

Open a Terminal window.
Install Homebrew by running the following command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Homebrew is installed, run the following command to install Go:

```bash
brew install go
```

Verify that Go is installed correctly by running the following command:

```bash
go version
```

This should print the version of Go that you just installed.

That's it! You now have Go installed on your macOS system using Homebrew.

### Linux

To install Go with Homebrew on Ubuntu, you need to perform the following steps:

Install Homebrew on Ubuntu by running the following command in the terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Homebrew is installed, update your Homebrew installation and formulae by running the following command:

```bash
brew update
```

Install Go using Homebrew by running the following command:

```bash
brew install go
```

After the installation is complete, verify that Go is installed by running the following command:

```bash
go version
```

This should output the version of Go that you just installed.

That's it! You have successfully installed Go with Homebrew on Ubuntu.

### Windows

To install Go on Windows, you can follow these steps:

1. Download the Go installer for Windows from the official Go website (https://golang.org/dl/).

2. Run the installer executable (.msi file) and follow the prompts to install Go.

3. Once the installation is complete, open the Windows Command Prompt (cmd) or PowerShell.

4. Verify that Go has been installed correctly by typing the following command:
   ```cmd
   go version
   ```
   If Go has been installed correctly, the version number of the installed Go will be displayed in the command prompt.
5. You're ready to start using Go on Windows!

> Note: Make sure that the directory where Go is installed is added to your system's PATH environment variable so that
> you can run Go commands from anywhere in the command prompt.

Since in most cases you will use the Linux environment to run the applications you develop, I would not recommend using
Windows specifically for development. 