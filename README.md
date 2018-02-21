# postcss_bootstrap_4

in order to reproduce, run:

docker run --rm -v $(pwd):/app --workdir "/app" node:9 /bin/bash -c "npm install && npm run build:scss"



```sh
➜  tmp (master) ✗ docker run --rm -v $(pwd):/app --workdir "/app" node:9 /bin/bash -c "npm install && npm run build:scss"
npm WARN bootstrap@4.0.0 requires a peer of jquery@1.9.1 - 3 but none is installed. You must install peer dependencies yourself.
npm WARN bootstrap@4.0.0 requires a peer of popper.js@^1.12.9 but none is installed. You must install peer dependencies yourself.
npm WARN app No description
npm WARN app No repository field.
npm WARN app No license field.

up to date in 6.155s

> @ build:scss /app
> node-sass app.scss --output-style compress | postcss --use autoprefixer -o app.css

events.js:137
      throw er; // Unhandled 'error' event
      ^

Error: EAGAIN: resource temporarily unavailable, write
CssSyntaxError: /app/app.css:2473:25: Unclosed string

  2471 |
  2472 | .custom-checkbox .custom-control-input:checked ~ .custom-control-label::after {
> 2473 |   background-image: url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 8 8'%3E%3Cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.1
       |                         ^

npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! @ build:scss: `node-sass app.scss --output-style compress | postcss --use autoprefixer -o app.css`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the @ build:scss script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /root/.npm/_logs/2018-02-21T14_26_50_028Z-debug.log
```
