To test, run:

```sh
$ npm run api-extractor
```

Note that `dist/index.d.ts` contains:

```ts
declare namespace ns {
    export {
        internalFunction
    }
}
export { ns }

export { }
```

But it should be:

```ts
declare namespace ns {
    export {}
}
export { ns }

export { }
```

(or similar).
