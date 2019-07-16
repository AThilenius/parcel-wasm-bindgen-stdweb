## Repro steps:

- Install [the Rust tools](https://www.rust-lang.org/tools/install)
- Install [wasm-pack](https://rustwasm.github.io/wasm-pack/installer/)
- Run
  ```sh
  git clone https://github.com/AThilenius/parcel-wasm-bindgen-stdweb.git
  cd parcel-wasm-bindgen-stdweb/web
  yarn install
  npx parcel index.js
  ```

## Sample Error
The following error is produced on my machine (Win 10, AMD64):
```
Server running at http://localhost:1234
×  C:\Users\Alec\local_dev\parcel-wasm-bindgen-stdweb\web\node_modules\parcel-plugin-wasm.rs\wasm-loader.js:1:77: Cannot resolve dependency './snippets/rust-6826ff9a52c09b34/inline0.js' at 'C:\Users\Alec\local_dev\parcel-wasm-bindgen-stdweb\web\node_modules\parcel-plugin-wasm.rs\snippets\rust-6826ff9a52c09b34\inline0.js'
> 1 | import { __cargo_web_snippet_14097f70c739ef4a180a6ad82cadc458d11e85dc } from './snippets/rust-6826ff9a52c09b34/inline0.js';
    |                                                                             ^
  2 | import { wasm_bindgen_initialize } from './snippets/stdweb-fdcd3965c5b71088/inline258.js';
  3 | import { __cargo_web_snippet_72fc447820458c720c68d0d8e078ede631edd723 } from './snippets/stdweb-fdcd3965c5b71088/inline363.js';
    4 | import { __cargo_web_snippet_97495987af1720d8a9a923fa4683a7b683e3acd6 }
    from './snippets/stdweb-fdcd3965c5b71088/inline364.js';
  ```

This file does however appear to exist.
