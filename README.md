### Running with CLJS
```bash
clj -M --main cljs.main --compile app.core
```
Should result in no output.

### Running with shadow-cljs
```bash
npm i
npx shadow-cljs watch main
```
Should result in something like:
```
[:main] Configuring build.
[:main] Compiling ...
[:main] Build failure:
------ ERROR -------------------------------------------------------------------
 File: jar:file:/home/p-himik/.m2/repository/com/taoensso/encore/3.36.0/encore-3.36.0.jar!/taoensso/encore.cljc:478:3
--------------------------------------------------------------------------------
 475 | ;;;; Truss aliases (for back compatibility, convenience)
 476 | 
 477 | (do
 478 |   (defalias taoensso.truss/have)
---------^----------------------------------------------------------------------
null
Unable to resolve var: have in this context at line 478 taoensso/encore.cljc
--------------------------------------------------------------------------------
 479 |   (defalias taoensso.truss/have!)
 480 |   (defalias taoensso.truss/have?)
 481 |   (defalias taoensso.truss/have!?)
 482 |   (defalias get-truss-data  taoensso.truss/get-data)
--------------------------------------------------------------------------------
```
