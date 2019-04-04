# vuecv

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## Surge

Allow hosting static web sites

### Upload to surge

1. Go to the folder where are files you want to updload.
2. In terminal run command
   surge
   You will be asked to register and after you will be provided by rundom url.
   You can change subdomen if is free.

### Deploy to surge by travis ci

1. Login in Travis by github gredentials.
2. You will see all your public projects.
3. Chose one that you want to setup CI.
4. In variables add surge token and surge login.
   Surge token you can get by running next command
   surge token
   Surge login is your email.