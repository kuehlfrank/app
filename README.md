# app

## submodules
init (after clone)
```
git submodule update --init --recursive
```
update all submodules with
```
git submodule -q foreach git pull -q origin main
git add .
git commit -m "update submodules"
git push
```
