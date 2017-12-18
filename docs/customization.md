# Customization
We do not support customization outside of regulated by style variables and
configuration options.

---
## Logo
You can set the logo from `General > Publication Logo` settings inside your theme. <br>
> We suggest usage of transparent logo with optimal size of 280x100 pixels or a `svg`
logo with size of 140x50 pixels.

---
## Background
You can set the background from `General > Publication Cover` settings inside your theme. <br>
> We suggest using less contrast backgrounds with the highest possible size that
your hosting plans is comfortable with and ratio 16:9

Take a note that the background for your blog is used as background for the
'Subscribe' block and the custom Error & Subscribe pages.

---
## Social Accounts
You can set the background from `General > Social Accounts` settings inside your theme. <br>
If you don't select such the 2 icons from the footer will disappear. The social icons
located in author profile pages & inside every post are controlled by the **User**
details.

---
## Styling
We support small range of styling options, for which you need to recompile the
template yourself. To recompile it you need:
- Source directory `vega/src`
- Nodejs with package manager `npm` or `yarn`

The recompilation process handles both CSS & JavaScript files.<br>
Here is the file structure for the styling:
<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th>File Name</th>
      <th>Description</th>
    </tr>
    </thead>
  <tbody>
    <tr>
      <td><code>vega/src/scss/config.scss</code></td>
      <td>Stylesheet configuration `This is the file we support only for editing`</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/app.scss</code></td>
      <td>Main stylesheet file, including all others</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/general.scss</code></td>
      <td>HTML functionalities and normalization</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/main.scss</code></td>
      <td>Basic styling for the theme</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/main_post.scss</code></td>
      <td>Basic styling for the posts</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/main_editor.scss</code></td>
      <td>Styling for custom tags and editor</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/footer.scss</code></td>
      <td>Footer styling</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/navigation.scss</code></td>
      <td>Navigation styling</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/layouts/responsive_max-.....scss</code></td>
      <td>Responsive fixes</td>
    </tr>
    <tr>
      <td><code>vega/src/scss/components/&#42;</code></td>
      <td>Vendor component libraries</td>
    </tr>
    </tr>
    <tr>
      <td><code>vega/src/scss/plugins/&#42;</code></td>
      <td>Vendor plugin libraries</td>
    </tr>
  </tbody>
</table>

Supported configuration is only `/vega/scss/config.scss`. Here is basic configuration:
```scss
// Fonts
$header-font:       'Open Sans', sans-serif;
$body-font:         'Merriweather', sans-serif; //Libre Baskerville
$nav-font:          'Maven Pro', sans-serif;
// Colors
$main-color:        #29177d;
$secondary-color:   #fde428;
$dark-color-bg:     #222222;
$light-color:       #fbfbfb;
// Responsive
$vertical: "only screen and (max-height: 750px)";
$width-small: "only screen and (max-width: 500px)";
$width-medium: "only screen and (max-width: 800px)";
$width-large: "only screen and (max-width: 1000px)";
```
We suggest editing colors with the current contrast and using readable fonts.
Do not edit the 'Responsive' variables.

---
## Recompile
In order to recompile please get to know npm's scripts block. Open your command
prompt and use

```bash
cd <YOUR_GHOST_FOLDER>/content/themes/vega/
yarn install
yarn build
```
Copy and paste the `assets` folder inside your uploaded vega theme. It must contain
- app.css
- app.js
