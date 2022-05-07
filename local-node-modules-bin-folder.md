# Exploring `node_modules/.bin` folder. 

> This is just learning journal for myself to improve my understanding.

Whether a globally or locally installed module, eventually it will reside within a `node_modules` directory. The contents of this gist is scopped within the local `node_modules` of an application's directory. Now within the local `node_modules` there should always exist a `.bin` folder that houses all the excutable files.

What I've gathered thus far:

1. On Unix/macOs, this files have the `chmod` 755 or 777 permissions to run as scripts.
2. All of these files start with `#!/usr/bin/env node` on the very first line.
3. These files do not require any file extensions (perhaps they are scripts).

**Experimented with**

* Created a file `Foo` in a local `./node_modules/.bin`

  ```javascript
  #!/usr/bin/env node
  
  console.log("Hello ${process.argv[2]}") //Because process.argv's first and second element are reserved for Node.js
  ```
  
* From a shell session, run `chmod 755 ./node_modules/.bin/foo` from the application's directory.
* Include `"foo": "foo World!"` in the associated `package.json`
* Run `npm run foo` in shell. This should return `Hello World!` in the terminal
