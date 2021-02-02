
## 1. `go mod init`
Run the `go mod init` command, giving it the path of the module your code will be in. Here, use `example.com/greetings` for the module path -- in production code, this would be the URL from which your module can be downloaded.

```bash
$ go mod init example.com/greetings
go: creating new go.mod: module example.com/greetings
```

## 2. use local module

Edit your  `go.mod` file and make it looks like this:
```bash
module hello

go 1.14

replace example.com/greetings => ../greetings
```

## 3. `go build`

Run `go build` to make Go locate the module and add it as a dependency to the go.mod file.
