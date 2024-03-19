# Inisialisasi Project
> npm init
akan menghasilkan package json

# installasi Typescript
> npm i -D typescript ts-node
-D artinya hanya digunakan untuk development

# Konfigurasi typescript
> npx tsc --init
maka menghasilkan tsconfig.json
- aktifkan moduleResolutin, resolveJsonMode, sourceMap, outDir, baseUrl, "paths": { "*" : ["*node_modules/*"] }, "typeRoots": ["./src/types", "./node_modules/@types"],     di file tsconfig.json

```"outDir": "build", maksudnya ketika program dibuild maka akan diarahkan ke folder build```

diluar compilerOption bikin objek baru
```
 "include": ["src/**/*"],
  "exclude": ["node_modules/*"]
```

- buat file baru bernama index.ts dalam folder src
- tambahkan 
```
    "start": "npx tsx -w",
    "dev": "npx nodemon",
    "build" : "tsc"
```
dalam package.json dan jangan lupa 
> npm i nodemon

kemudian konfigurasi nodemon di nodemon.json 
```
{
    "watch" : ["src"],
    "ext": "ts",
    "exec": "npx ts-node ./src/index.ts"
}
```

- tambahkan hello world di index.ts kemudian jalankan 
> npm run dev

# Installasi Express
dalam projek ini akan digunakan untuk restApi
>npm i express

karna menggunakan typescript maka perlu install lagi karena terkadang tidak support 
> npm i -D @types/express


