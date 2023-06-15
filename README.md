# jekyll-showcase

A showcase of my Jekyll creations. Most of these (except ["fancy tables"](https://github.com/RichDom2185/jekyll-fancy-tables)) were co-developed together with _[FoodRem](https://github.com/RichDom2185/tp)_, a school project undertaken in late 2022, as part of my efforts to streamline our team's developer experience with regards to documentation.

This repository simply consolidates all of my Jekyll creations into one place; feel free to browse through each submodule's repository for more information.

## Contents

All of the below submodules do not require extra gems, and are therefore **GitHub Pages-compatible**. This means that you don't have to pre-generate your Jekyll sites before pushing them to GitHub Pages.

Ocassionally, I may add more Jekyll creations to this repository. For now, the following are available:

### [jekyll-fancy-tables](https://github.com/RichDom2185/jekyll-fancy-tables)

A Jekyll plugin that allows you to create tables with a bit more flair than the default Markdown table syntax.

<table>
<thead>
<tr>
<th>Example 1</th>
<th>Example 2</th>
</tr>
</thead>
<tbody>
<tr>
<td>

Markdown code like this...

````markdown
```table
| OMG, I span 3 columns! \      \      |
|------------------------|------|------|
| That's...              | very | nice |
```
````

becomes HTML like this...

<table>
  <thead>
    <tr>
      <th colspan="3" data-nth-cell="1" align="left">OMG, I span 3 columns!</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="1" rowspan="1" data-nth-cell="2" align="left">That’s…</td>
      <td colspan="1" rowspan="1" data-nth-cell="3" align="left">very</td>
      <td colspan="1" rowspan="1" data-nth-cell="4" align="left">nice</td>
    </tr>
  </tbody>
</table>

</td>

<td>

Markdown code like this...

````markdown
```table
|------------------------|---------|
| Look, I span two rows! | Looks   |
| ^^                     | pretty! |
```
````

becomes HTML like this...

<table>
  <tbody>
    <tr>
      <td colspan="1" rowspan="2" data-nth-cell="1" align="left">Look, I span two rows!</td>
      <td colspan="1" rowspan="1" data-nth-cell="2" align="left">Looks</td>
    </tr>
    <tr>
      <td colspan="1" rowspan="1" data-nth-cell="3" align="left">pretty!</td>
    </tr>
  </tbody>
</table>

</td>
</tr>
</tbody>
</table>
