# Go Web Starter

A Go web app structure, that you can use to build your web app using Go with plain `http/net`, or frameworks such as `Gin`, `Echo`, `Fiber`, or others. The folder are divided based on their functionalities, in such way that make your creating the app easier and organizable. Nothing force you to go with it as it is, you're free to update the structure as you like. The way in this starter is taken from experience of building web app in different tech stack.

## How to use

The easiest way is to clone the repo with `git clone https://github.com/mbougarne/go-web-starter.git`, then update the `go.mod` `module name` to match your own. You can go manually and start creating the files and their folders in your machine, after initializing a `Go module` with `go mod init {the-name-of-the-module}`.

### About Structure

This structure are intended to be used as a RESTFul app, not a full-stack app with front and back-end in the same place. No views should be here.

| Directory Name   | Use Case   |
| --- | --- |
| `configs`    | All the configurations of the app should be here, like the `database` configs.      |
| `controllers`    | The functions handler of the incoming http request, and all the http stuff.    |
| `middlewares`    | The middlewares of the app to pre process the incoming http request before jumping to the main handler function     |
| `models` | The db tables, with their schema and pre/post hooks should be in this directory |
| `security` | All the stuff of authentication, and authorization should be here |
| `services` | The functions that work as a middleware between the `controller` and `models` to manage the `db CRUD` should live here |
| `types` | All the `type StructName struct` should be here, with an exception of the `model tables`, you can put then in `model` directory  |
| `validation` | The functions to validate data, or http requests should live in this directory |
