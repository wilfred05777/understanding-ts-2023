# Explore NodeJS , Typescript, Express + MongoDB

- Node.js API From Scratch Using TypeScript, Express And MongoDB #1 : [video1](https://www.youtube.com/watch?v=1o9YOHeKhNQ&t=3399s)
- Node.js API From Scratch Using TypeScript, Express And MongoDB #1 : [video2](https://www.youtube.com/watch?v=FXzsv2BJLKs)

  - github: [link](https://github.com/JasonMerrett/nodejs-api-from-scratch)

- video source: [resource2](https://www.udemy.com/course/understanding-typescript/learn/lecture/16999296#overview)

- article source: [resource3](https://auth0.com/blog/node-js-and-typescript-tutorial-build-a-crud-api/)

- NPM Docs source: [Typescript-node-package](https://www.npmjs.com/package/ts-node)

<hr>

- mkdir dir_name
- npm init -y
- npm i -D typescript tsc-watch eslint prettier eslint-config-prettier eslint-plugin-prettier @typescript-eslint/parser @typescript-eslint/eslint-plugin @types/node @types/express

- npm i express dotenv
- npx tsc --init

<hr>

- /src/.prettierrc

```
{
  "singleQuote": true,
  "bracketSpacing": true,
  "printWidth": 120
}
```

<hr>

- src/tsconfig.json

  - src/code

            ```
                "target": "es2018",
                "moduleResolution": "node",
                 "outDir": "./dist",
                 "rootDir": "./src",

            ```

- package installation
<hr>

- npm i --save express body-parser
- npm i --save-dev nodemon

<hr>

- tsc -w

```.json
"start": "nodemon dist/app.js"
```

<hr>

<!-- Max  -->

###### keep take aways -02-06-2023 MOnday

```
//app.ts
import express, { Request, Response, NextFunction } from 'express';

app.use((err: Error, req: Request, res: Response, next: NextFunction) => {
res.json({ message: err.message });
});

```

```js
//  Pwede anion para di na magbutang ug tagsa2 ka types pero sa express ra pud,
// How about other approach kung dili na express gamiton?

// import { Request, Response, NextFunction } from 'express';
import { RequestHandler } from 'express';

export const createTodo: RequestHandler = (req, res, next) => {};
```
