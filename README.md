# learning-go-module
A sample project to demonstrate using Go2 Modules for starting a project

Steps:
1. Initialize go Modules.
```
go mod init github.com/rahul26goyal/learning-go-module
```

2. create `main.go` file and write a `main` function.

3. Create a new folder `hellopkg` which is a package.

4. create 2 files - `hello.go` and `hello_test.go` with some code.

5. Go Build locally: This will download all remote dependency and update `go.sum` file.
This is nothing but the `lock` file.
```
go  build
```

6. Run all the unit test.
```
go test ./...
```
This should pass without any error.

7. Push changes to master.
```
git add .
git commit -m ""
git push origin master
```

8. Create a Version of your package using `git tag`.
```
git tag v0.1.0
git push origin v0.1.0
```

9. Verify the package is available at remote:
```
>  go list -m github.com/rahul26goyal/learning-go-module@v0.1.0
github.com/rahul26goyal/learning-go-module v0.1.0
```

10. Use this dependency on a different project if as required.

Reference: https://blog.golang.org/publishing-go-modules
