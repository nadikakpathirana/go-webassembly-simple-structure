## Project Setup
1. Clone github repo
2. Go to the path cmd/wasm and run below code on terminal
``` console
 GOOS=js GOARCH=wasm go build -o ../../assets/main.wasm
 ```
3. To compile go code in to wasm.
4. Finaly start the server using 
``` console
    go run cmd/server/main.go
```
5. Open in browser

## Optional
> If you want you can copy wasm_exec.js in to assest folder by running
``` console
cp "$(go env GOOROOT)/misc/wasm/wasm_exec.js" .
```


## If there is an import error indicating on vscode do followings
1. go to vs code and search globaly as Go tools

2. click on Go: Tools Env Vars

3. Update settings.json by adding below code to rest of the json file.

``` json
"go.toolsEnvVars": {
    "GOOS": "js",
    "GOARCH": "wasm"
}
```