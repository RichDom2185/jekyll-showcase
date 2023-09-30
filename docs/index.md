---
layout: demo
---
<!-- markdownlint-disable-file first-line-h1 -->
<!-- markdownlint-disable-file blanks-around-fences -->

> {{ site.description }}
{: style="font-size: 1.5em" }

For the full guide (usages, etc.), view the project on [GitHub]({{ site.github.repository_url }}).

<!-- markdownlint-disable-next-line blanks-around-headers -->
## Table of Contents
{: .no_toc}

* toc
{:toc}

## Jekyll Admonitions

Converts markdown as follows:

* ````markdown
  ```note
  This is a note.
  ```
  ````

* ````markdown
  ```tip
  This is a tip.
  ```
  ````

* ````markdown
  ```info
  This is a info.
  ```
  ````

* ````markdown
  ```warning
  This is a warning.
  ```
  ````

* ````markdown
  ```danger
  This is a danger.
  ```
  ````

Into the corresponding admonition boxes:

* ```note
  This is a note.
  ```
  
* ```tip
  This is a tip.
  ```
  
* ```info
  This is a info.
  ```
  
* ```warning
  This is a warning.
  ```
  
* ```danger
  This is a danger.
  ```
  
## Jekyll Fancy Tables

{% capture table %}
```table
| Check out this _fancy_ :sparkles: table!                                               \\|
|----------|-----------------------------------------------------------------|-------------|
| Doe      | A deer, a female...                                             | Deer        |
| Oh wait, \ this cell spans two columns! Here's an orange :tangerine:       | Two rows!   |
| Four...  | Bananas forever :banana: :banana: :banana:                      | ^^          |
| ^^       | Oops, forgot one more :banana:                                  \             |
| Testing  | This is <strong>HTML bold</strong>, not markdown                | _center_    |
| This row would be center-aligned                                          \| Hello,      |
| ^^ Hey! How are you? :eyes:                                               \| ^^          |
| Sponge?  | Imagination :rainbow:  &#124; ( • ) ( • ) &#124; :rainbow:      | ^^ _world?_ |
| Thirteen | Some text I will break here,<br>and oh, it also has **markdown** styling!    \|
```alignment
c LLL Lr LL L LLc cL   ll lR
```

{% endcapture %}

Converts Markdown code like follows:

{% capture newline %}
{% endcapture %}

{% assign as_code = '' | split: '' %}
{% assign lines = table | split: newline %}
{% for line in lines %}{% assign as_code = as_code | push: line %}{% endfor %}

````markdown
{{- as_code | join: newline }}
````

To a table like follows:

{{ table }}

## Jekyll-PlantUML

Converts your code blocks tagged with either the `plantuml` or `puml` language into the correspoding PlantUML diagram.

* Markdown

  ````markdown
  ```puml
  Alice -> Bob: Hi there!
  Bob --> Alice: Hello to you too!
  ```
  ````

* Result:

  ```puml
  Alice -> Bob: Hi there!
  Bob --> Alice: Hello to you too!
  ```
