Bug reproduction.

```bash
git clone git@github.com:brillout/vps-vite3.1-bug
cd vps-vite3.1-bug/
pnpm install
pnpm run build
```

Same as single line (copy-paste me):

```shell
git clone git@github.com:brillout/vps-vite3.1-bug && cd vps-vite3.1-bug/ && pnpm install && pnpm run dev
```

Then go to [localhost:3000](http://localhost:3000) and observe following error in the browser's dev console.

```
Uncaught (in promise) TypeError: Cannot read properties of undefined (reading 'accept')
    at Counter.vue:23:17
```

The failing JavaScript line `Counter.vue:23:17` is:

```js
import_meta.hot.accept((mod) => {
```
