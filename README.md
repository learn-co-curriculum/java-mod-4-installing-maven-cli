# Installing Maven

## Learning Goals

- Install Maven on your machine.

## Introduction

Maven can be installed manually or by using a package manager tool like `brew`
(Mac). We’ll first walk through the manual installation process where we
download the archive from the Maven website and add the executable to our PATH.

## Manual Installation

Here are the steps we’ll follow:

- Download and extract the bin archive.
- Add Maven to our PATH.

### Getting the Maven Archive

- Visit
  [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi).
- If you’re on Windows, download the
  [apache-maven-3.8.6-bin.zip](https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.zip)
  file.
- If you’re on Mac, download the
  [apache-maven-3.8.6-bin.tar.gz](https://dlcdn.apache.org/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz)
  file.
- You can extract the archive to any folder on your machine. We’ll be extracting
  it in the `C:/developer` directory on Windows and `~/developer` directory on a
  Mac.

### Add Maven to PATH

The `bin` file in the extracted folder is used to run Maven. If we add this
file’s path to our PATH variable, we’ll be able to use the `mvn` command from
anywhere on our machine.

For Windows, run the following command:

```bash
setx path "%path%;c:\developer\apache-maven-3.8.6\bin"
```

For Mac, run the following commands:

```bash
export PATH="~/developer/apache-maven-3.8.6/bin:$PATH"
source ~/.zshrc
```

## Installing with Brew (Mac)

We can also use Homebrew to install Maven on our machine.

```bash
brew install maven
```

## Testing Maven Installation

If the above steps worked, you should be able to access the `mvn` command from
your command line or terminal. Run the following command to check if it was
installed.

```bash
mvn -version
```

You should get an output like this:

```bash
Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
Maven home: /opt/homebrew/Cellar/maven/3.8.5/libexec
Java version: 17.0.2, vendor: Homebrew, runtime: /opt/homebrew/Cellar/openjdk/17.0.2/libexec/openjdk.jdk/Contents/Home
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "12.3.1", arch: "aarch64", family: "mac"
```

This particular machine is running `3.8.5` but yours should list `3.8.6`.

## Conclusion

Now that we have a working Maven installation on our machine, we will look into
creating projects with Maven and understanding the core concepts in the next
lessons.
