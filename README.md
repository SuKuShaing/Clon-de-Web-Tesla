# Clon de la web de Tesla

Siguiendo el tutorial de Midudev
https://youtu.be/S_oLr_np4S8?si=R9F4o9aJ5ZlVelrX





## EPERM: operation not permitted, rmdir
Con esto se solucionan el error
```
$ npm run build

> generador-de-sitios-estaticos---fazt@0.0.1 build
> astro build
EPERM: operation not permitted, rmdir 'D:\Progra\Youtube\Astro\Generador de sitios estáticos - Fazt\node_modules\.vite\deps'
  Stack trace:

```

ejecutando los 5 pasos de aquí, se soluciona (ojo comandos para consola windows, no funcionan en bash porque emula comandos Linux)

1) clean npm cache
npm cache clean --force

2) (Windows) delete node_modules and package-lock.json
rd /s /q "node_modules"
del package-lock.json
del -f yarn.lock

3) update your npm version
npm install -g npm@latest --force

4) clean npm cache
npm cache clean --force

5) install packages
npm install
