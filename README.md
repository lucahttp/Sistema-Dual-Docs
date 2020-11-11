# Resumen

It is recommended to install `docsify-cli` globally, which helps initializing and previewing the website locally.

```bash
npm i docsify-cli -g
```

## Materias

If you want to write the documentation in the `./docs` subdirectory, you can use the `init` command.

```bash
docsify init ./docs
```

| Grupo              | Materia                                  | Tipo     | Año | Mail                                           |
| ------------------ | ---------------------------------------- | -------- | --- | ---------------------------------------------- |
| Gestión            | Analisis y procesos de sistemas          | Anual    | 1   | bdelafare@gmail.com                            |
| Gestión            | Economia y gestion de las organizaciones | Anual    | 1   | ezequieloscarescobar2@gmail.com                |
| Gestión            | Metodologías de Gestión de Proyectos     | No Anual | 1   | leandro.sanchezzarfino@gmail.com               |
| Idiomas            | Ingles tecnico I                         | Anual    | 1   | uberto.r.m@gmail.com                           |
| Idiomas            | Aleman Tecnico I                         | Anual    | 1   | sandra.grego1@gmail.com                        |
| Infraestructura IT | Electronica general                      | Anual    | 1   | hampelmatias@gmail.com                         |
| Infraestructura IT | Arquitectura de computadoras             | Anual    | 1   | ezequieljsosa@gmail.com                        |
| Infraestructura IT | Redes de datos                           | No Anual | 1   | jm.soto9@gmail.com                             |
| Sistemas IT        | Bases de datos                           | Anual    | 1   | nperez@frba.utn.edu.ar                         |
| Sistemas IT        | Desarrollo de Software I                 | Anual    | 1   | ezequieloscarescobar2@gmail.com                |
| Sistemas IT        | Diseño y maquetado web                   | No Anual | 1   | melubrandao@gmail.com;mailen.brandao@gmail.com |
| Gestión            | Aspectos legales                         | No Anual | 2   | fede.sabbatini@gmail.com                       |
| Gestión            | Gestion de los procesos productivos      | Anual    | 2   | bdelafare@gmail.com                            |
| Idiomas            | Aleman tecnico II                        | Anual    | 2   | sandra.grego1@gmail.com                        |
| Idiomas            | Ingles tecnico II                        | Anual    | 2   | uberto.r.m@gmail.com                           |
| Infraestructura IT | Administracion de sistemas               | Anual    | 2   | ezequieljsosa@gmail.com                        |
| Infraestructura IT | Automatizacion industrial                | No Anual | 2   | jm.soto9@gmail.com                             |
| Infraestructura IT | Redes Industriales                       | No Anual | 2   | jm.soto9@gmail.com                             |
| Infraestructura IT | Seguridad Informática                    | No Anual | 2   | maritamason74@gmail.com                        |
| Sistemas IT        | Arquitectura de software                 | Anual    | 2   | saclier@gmail.com                              |
| Sistemas IT        | Calidad de software                      | Anual    | 2   | leandro.sanchezzarfino@gmail.com               |
| Sistemas IT        | Desarollo de software II                 | Anual    | 2   | ezequieloscarescobar2@gmail.com                |
| Sistemas IT        | Inteligencia artificial                  | Anual    | 2   | tajerianmatias@gmail.com                       |
| Sistemas IT        | Inteligencia de negocios                 | Anual    | 2   | nperez@frba.utn.edu.ar                         |
|                    | Integracion de sistemas                  | Anual    | 2   | saclier@gmail.com                              |

## Writing content

After the `init` is complete, you can see the file list in the `./docs` subdirectory.

- `index.html` as the entry file
- `README.md` as the home page
- `.nojekyll` prevents GitHub Pages from ignoring files that begin with an underscore

You can easily update the documentation in `./docs/README.md`, of course you can add [more pages](more-pages.md).

## Preview your site

Run the local server with `docsify serve`. You can preview your site in your browser on `http://localhost:3000`.

```bash
docsify serve docs
```

?> For more use cases of `docsify-cli`, head over to the [docsify-cli documentation](https://github.com/docsifyjs/docsify-cli).

## Manual initialization

If you don't like `npm` or have trouble installing the tool, you can manually create `index.html`:

```html
<!-- index.html -->

<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="//unpkg.com/docsify/themes/vue.css" />
  </head>
  <body>
    <div id="app"></div>
    <script>
      window.$docsify = {
        //...
      };
    </script>
    <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
  </body>
</html>
```

If you installed python on your system, you can easily use it to run a static server to preview your site.

```bash
cd docs && python -m SimpleHTTPServer 3000
```

## Loading dialog

If you want, you can show a loading dialog before docsify starts to render your documentation:

```html
<!-- index.html -->

<div id="app">Please wait...</div>
```

You should set the `data-app` attribute if you changed `el`:

```html
<!-- index.html -->

<div data-app id="main">Please wait...</div>

<script>
  window.$docsify = {
    el: "#main"
  };
</script>
```
