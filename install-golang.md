#Getting Started with Golang

Getting started with Golang does takes a few steps that may seem a little more complicated than other installations you might have run. We'll walk through the steps here as well as provide helpful links in case you run into trouble with your particlar environment. 

### How to get started with Golang:

1. Install Golang on your machine
2. Organize your projects, Go-style
3. Set up your `$GOPATH`
4. Using `godep` as your dependency manager
 
We'll walk through these steps together and then demonstrate the traditional `Hello, World` program to ensure everything works.

### Run into trouble? Join the club!
At times it may seem that setup is the hardest part of getting started with a new language or framework. Luckily, the Golang community has takes a very proactive approach to welcoming new developers and supports a variety of forums in Slack, Google+ and other sites. 

[Join the community on the platform of your choice](https://golang.org/help/) and you will likely find someone willing to help you during installation and beyond.

## 1. Install Golang on your machine

### Linux
Use your standard package manager to install Golang:
* Ubunto : `$ apt-get install golang`
* Debian : `$ dpkg install golang`
* Fedora/CentOS/RHEL : `$ yum install golang`

Refer to documentation for your installation if you run into trouble here. Ask XModulo has a more detailed post about [installing Golang on various Linux distributions](http://ask.xmodulo.com/install-go-language-linux.html) that might prove useful as well.

### Mac
Homebrew makes installing Golang very easy:
`$ brew install go`

If you don't use Homebrew, follow this link to [Golang's official download page](https://golang.org/dl/) and download the current package installer version for OSX.  

### Windows
Unfortunately, Windows remains fairly uncooperative when it comes to supporting package managers. Your best bet is to visit [Golang's official download page](https://golang.org/dl/) and download the Windows version. 

## Organize your Golang projects

Golang requires us to organize all our code (our own and imported) within a single directory, referred to as the _workspace_. 
Why??

Well, Golang operates by linking modules of code together to build your app. You specify the modules that you need based on the scope of your app by adding `import <module-name>` to your files. To build your app before running, the Go compiler must know where to find the code for these modules at compile time. By design, it expects to find the necessary code under `$GOPATH/src` where `$GOPATH` is an [environment variable](https://www.gnu.org/software/bash/manual/html_node/Shell-Parameter-Expansion.html) that we will set in the next step.

Any time you run `go get` or `go install`, the compiler will download required modules to your `$GOPATH/src` and then compile those modules into `$GOPATH/pkg`. If applicable, it then builds a binary under `$GOPATH/bin`.

All of this means that improperly organizing your Golang _workspace_ directory will cause serious problems when you attempt to build to your program. You may read that using a _workspace_ is done "by convention" which implies it is optional-- not so! 

Note that third-party tools that apply other approaches rely on significant hacking of Golang defaults to work, twisting against the core design of the compiler and [other critical tools provided by Google](https://github.com/golang/tools). Employ them at your own peril.

To follow the proper setup design, simply dedicate a parent directory to Golang called something intuitive like `/go` wherever you put other coding projects. When we first run `go install <package-name>` after setting up our `$GOPATH`, the compiler will create the proper subdirectories within our _workspace_ and run our program.

Of course, you will have many project written in Golang! Each will get its own subdirectory within `go/src`. We can trust Golang's superb compiler to do the rest. In fact, we will see others ways our compiler helps us to write clean code.   

## Set up your `$GOPATH`

## `Hello, World`

## A word about Documentation
