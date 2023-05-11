# go-course

This is a hands-on async course/workshop for learning how to build APIs with Go.

How to participate in this course:
1. Create a github repository.
2. Copy the content of this repository in your repo.
3. Start implementing the services step by step.

## 1. Todo API

We are going to implement an API that manages TODOs.  
Think of it as the backend for something like this: https://reactjsexample.com/github-lilia-obushenko-todo-react-app/

- [ ] Install Go - https://go.dev/doc/install

- [ ] Learn the basics (syntax, data types, structs, interfaces) - https://gobyexample.com/ 

- [ ] Clone, build and run the project as is. e.g. `go run ./cmd/todoapi/...`
  https://blog.devgenius.io/go-build-vs-go-run-baa3da9715cc

- [ ] Define todo struct under `model/` package.
  https://gobyexample.com/structs

- [ ] Implement in-mem repo layer under `repo/` package. Should support at least Create and Get.
https://gobyexample.com/interfaces 
```go
// example
type MyRepo interface {
	Create(todo model.Todo) error
	Get(name string) (model.Todo, error)
}

type InMemRepo struct {
	...
}
```

- [ ] Unit test your repo layer. https://go.dev/doc/tutorial/add-a-test

- [ ] Implement service layer. Service layer has access to `repo/` methods (via the interface) to perform at least the following operation
`Get Or Create`.

- [ ] Unit test your service layer.

- [ ] Unit test your API layer. Yes, now that you have experience writing unit tests, first write the tests then write the code, TDD!.

- [ ] Implement api layer. API layer does not has access to any other package (service interface is defined under API layer).
  https://gobyexample.com/http-servers

- [ ] Initialize everything under `cmd/todoapi/` and start the http API.

Ask help/questions in telegram @eoozs
