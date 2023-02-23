## sam-app

### Build and Run

`make build`

All your binaries will end up in this app, in the `.aws-sam/build` folder.

This is because the template.yaml files for those applications are referred to in the template.yaml file at the base of this app.

In shared envs, instead of referring to local file paths, we'll refer to `hello-world` and `goodbye-world`'s arns. We'll build all the apps separately.

This will require that we build `hello-world` and `goodbye-world` separately, put their arns into this app's template.yaml file, and then build this app.

run `make start-api`

Then hit

`http:localhost:3000/hello` and `http:localhost:3000/goodbye`