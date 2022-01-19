[![Netlify Status](https://api.netlify.com/api/v1/badges/a474499e-4612-4a49-b8cb-1c9d27cf2f7e/deploy-status)](https://app.netlify.com/sites/relaxed-galileo-64e9d4/deploys)

# P4: Bootstrap

Website template by freewebsitetemplates.com

- Original template: [ecothunder-template](https://freewebsitetemplates.com/preview/ecologicalwebsitetemplate/index.html)

- Netlify deploy: [ecothunder](https://relaxed-galileo-64e9d4.netlify.app/)

## Elements de Bootstrap utilitzats

### Layout

- **Breackpoints:** S'han fet servir _breakpoints_, principalment `md` i `lg`, a diferents parts de la web per tal de aconseguir que les diferents pàgines de la web, per exemple per canviar el nombre de columnes que faran servir alguns dels elements en función del tamany de la pantalla, o també per canviar l'amplada d'algun botó en funció de l'amplada de la pantalla.

- **Containers, Grid & Columns:** S'han fet servir containers en algunes parts de la web per tal de repartir els elements dins dins un espai determinat. Per exemple, s'ha fet servir per les cards de la _Home page_, a la pàgina _about us_, a la pàgina _contact us_, com també al _footer_. Dins dels _containers_, s'han fet servir les classes _row_ i _col_ per tal de distribuir els diferents elements dins el _container_.

### Content

- **Typography:** S'han fet servir algunes classe per modificar els textos originals, com per exemple, `text-muted`, `lead`, entre d'altres.

- **Images:** Per tal de que les imatges tinguin un comportament correcte amb els canvis d'amplada de la pantalla, s'ha fet servir la classe `img-fluid`.

- **Table:** A la pàgina _Why choose us?_ s'ha afegit una taula amb la classe `table` per tenir una millor visualització del contingut.

### Forms

- **Form control, Checks, Validation, ...:** S'ha creat un formulari a la pàgina _Contact us_ fent servir algunes classes com per exemple, `needs-validation` per les validacions, `form-label` per les etiquetes _label_, `form-control` pels _input_ o `form-check` per tenir _checkbox_.

### Components

- S'han fet servir alguns components com ara `buttons`, `cards`, `carousel`, `nav` i `navbar`.

### Helpers

- S'ha fet servir algun _helper_ com ara `Colored links`, _position_ `fixed-top` per el header o `position-sticky` per el _aside_ de la pàgina _Blog_.

### Utilities

- **Backgroud:** S'ha fet servir alguna classe `bg-_color_` per tal de definir el color de fons d'algun element.

- **Borders:** S'han fet servir algunes _utilities_ de _border_ per definir aquest paràmetre, com per exemple, la classe `border-_num_` per definir el gruix o la classe `rounded` per arrodonir els cantons.

- **Colors:** S'han fet servir aquestes _utilities_ per definir colors de texte, colors dels botons, etc.

- **Flex:** Per tal de organitzar el contingut d'algun element o algun _container_, s'ha fet servir la classe `d-flex` juntament amb `justify-content-center` o alguna similar, per tal de centrar els elements o distribuir-los dins l'element contenidor. Per exemple, a la _Home page_ s'han fet servir les classes `d-flex` i `justify-content-around` perquè les _cards_ es distribueixin de forma ordenada dins el contenidor.

- **Overflow:** S'ha fet servir la classe `overflow-hidden` a la _Home page_, a la imatge de la primera secció, per evitar que es solapi amb la segona secció de la pàgina.

- **Shadows:** S'han fet servir sombres en les imatges i a les _cards_, per donar un sombrejat i una estètica més agradable.

- **Spacing:** En alguns casos s'ha hagut d'afegir algun _margin_ i/o _padding_ per tal de col.locar algun element o afegir alguna separació entre elements.

## Customització i Paleta de colors

- $primary: #2a973a;
- $secondary: #98e633;
- $warning: #cdaf09;
- $danger: #ca1c1e;
- $header: linear-gradient(to top right, $secondary, $primary);

S'ha provat a afegir _custom colors_ fent servir variables i maps de SASS, però no s'ha aconseguit. Abaix es mostren dues formes que s'han provat per afegir colors customitzats.

```CSS
/* Imports para tratar de añadir custom colors y usar maps */
@import '../../node_modules/bootstrap/scss/functions';
@import '../../node_modules/bootstrap/scss/variables';
@import '../../node_modules/bootstrap/scss/mixins';
@import '../../node_modules/bootstrap/scss/utilities';

/* Intento de añadir custom colors 1 */
// Own colors
$custom-colors: (
  "footer": #1e2429,
  "white-letter": #e4e1e1
);
// Merge the maps
$theme-colors: map-merge($theme-colors, $custom-colors);
```

```CSS
/* Imports para tratar de añadir custom colors y usar maps */
@import '../../node_modules/bootstrap/scss/functions';
@import '../../node_modules/bootstrap/scss/variables';
@import '../../node_modules/bootstrap/scss/mixins';
@import '../../node_modules/bootstrap/scss/utilities';

/* Intento de añadir custom colors 2 */
$footer: #1e2429;
$white-letter: #e4e1e1;

$custom-colors: (
  "footer": $footer,
  "white-letter": $white-letter
);

$colors: map-merge($colors, $custom-colors);
$theme-colors: map-merge($theme-colors, $custom-colors);
$utilities-colors: map-merge($utilities-colors, $custom-colors);
```

## Ampliacions

- S'han fet tres pàgines més a més de les obligatòries, que són _About Us_, _Contact Us_ i _Why Choose Us_.
- S'han afegit altres components a més de `cards` i `navbar` com `buttons`, `carousel`, `collapse` i `tables`.
- S'han modificat completament les diferents pàgines de la web, per tal de donar un aire més modern i una vista més elegant i agradable. A més, totes les pàgines són responsive.
