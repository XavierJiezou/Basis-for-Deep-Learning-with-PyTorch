# Extend CommonMark with roles and directives

> https://myst-parser.readthedocs.io/en/latest/syntax/roles-and-directives.html

MyST allows any Sphinx role or directive to be used in a document. These are extensions points allowing for richer features, such as admonitions and figures.

## A block-level extension point

For example, add an `admonition` directive and `sup` role to your Markdown page, like so:

```
    ```{admonition} Here's my title
    :class: tip

    Here's my admonition content.{sup}`1`
    ```
```

```{admonition} Here's my title
:class: tip

Here's my admonition content.{sup}`1`
```

## Using YAML frontmatter

```
    ```{code-block} python
    ---
    lineno-start: 10
    emphasize-lines: 1, 3
    caption: |
        This is my
        multi-line caption. It is *pretty nifty* ;-)
    ---
    a = 2
    print('my 1st line')
    print(f'my {a}nd line')
    ```
```

```{code-block} python
---
lineno-start: 10
emphasize-lines: 1, 3
caption: |
    This is my
    multi-line caption. It is *pretty nifty* ;-)
---
a = 2
print('my 1st line')
print(f'my {a}nd line')
```

## Short-hand options with : characters

```
    ```{code-block} python
    :lineno-start: 10
    :emphasize-lines: 1, 3

    a = 2
    print('my 1st line')
    print(f'my {a}nd line')
    ```
```

```{code-block} python
:lineno-start: 10
:emphasize-lines: 1, 3

a = 2
print('my 1st line')
print(f'my {a}nd line')
```

## MyST parses this content as Markdown

```
    ```{admonition} My markdown link
    Here is [markdown link syntax](https://jupyter.org)
    ```
```

```{admonition} My markdown link
Here is [markdown link syntax](https://jupyter.org)
```

```
    ```{note} Notes require **no** arguments, so content can start here.
    ```
```

```{note} Notes require **no** arguments, so content can start here.
```

## Nesting directives

```
    ````{note}
    The next info should be nested
    ```{warning}
    Here's my warning
    ```
    ````
```

````{note}
The next info should be nested
```{warning}
Here's my warning
```
````

```
    ````{note}
    The warning block will be properly-parsed

    ```{warning}
    Here's my warning
    ```

    But the next block will be parsed as raw text

        ```{warning}
        Here's my raw text warning that isn't parsed...
        ```
    ````
```

````{note}
The warning block will be properly-parsed

   ```{warning}
   Here's my warning
   ```

But the next block will be parsed as raw text

    ```{warning}
    Here's my raw text warning that isn't parsed...
    ```
````

## Markdown-friendly directives

```
:::{note}
This text is **standard** *Markdown*
:::
```

:::{note}
This text is **standard** *Markdown*
:::

```
:::{note}
This text is **standard** _Markdown_
:::

:::{table} This is a **standard** _Markdown_ title
:align: center
:widths: grid

abc | mnp | xyz
--- | --- | ---
123 | 456 | 789
:::
```

:::{note}
This text is **standard** _Markdown_
:::

:::{table} This is a **standard** _Markdown_ title
:align: center
:widths: grid

abc | mnp | xyz
--- | --- | ---
123 | 456 | 789
:::

## An in-line extension point

```
Since Pythagoras, we know that {math}`a^2 + b^2 = c^2`
```

Since Pythagoras, we know that {math}`a^2 + b^2 = c^2`

```
    ```{math} e^{i\pi} + 1 = 0
    ---
    label: euler
    ---
    ```

    Euler's identity, equation {math:numref}`euler`, was elected one of the
    most beautiful mathematical formulas.
```

```{math} e^{i\pi} + 1 = 0
---
label: euler
---
```

Euler's identity, equation {math:numref}`euler`, was elected one of the
most beautiful mathematical formulas.