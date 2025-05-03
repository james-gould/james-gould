# 🏃💨 Visual Studio Code Snippets

Code snippets are a fundamental part of any IDE, you likely use them without knowing. `ctor` will create a `constructor` in a new class, `prop` will create a property with accessors done for you. 

The snippets in the [CodeSnippets](https://github.com/james-gould/james-gould/tree/main/CodeSnippets) directory automate some more repetitive tasks, such as argument validation or created defaulted properties.

I predict exactly 0 people will be reading this but should you wish to contribute a snippet, or create your own, the template [SnippetTemplate.snippet](https://github.com/james-gould/james-gould/blob/main/SnippetTemplate.snippet) is available for creating new ones without having to figure it out yourself.

## Installation

1. Clone the directory, or copy the contents of each `.snippet` to a new file in the same folder on your machine.
2. Open Visual Studio, navigate to the menu bar and select `tools -> Code Snippet Manager`
3. Change the dropdown from `ASP.NET Web Forms` (by default) to `CSharp`
4. Click `Import` and select the folder containing your `.snippet` files.
5. Confirm the dialogue boxes and close the `Code Snippet Manager`
6. Restart Visual Studio.

## The Snippets Included

Below is a list and explaination of the snippets I've created. The title is formatted as `shortcut - snippet name`. The snippets I create will set your cursor position to a specific place, making them even easier to use when you're zooming; this is denoted by the `|` character 🏃💨

Once imported press the keys in the `shortcut` section and press `TAB` twice to autofill the contents of the `snippet name`.

### ar - ArgumentExceptionNullEmpty.snippet 

Validates a string, appending a new line to the bottom.

```cs
public void MyFunction(string name)
{
    ArgumentException.ThrowIfNullOrEmpty(|);

}
```

### an - ArgumentNullException

Validates a `Nullable<T>` and appends a new line to the bottom.

```cs
public void MyFunction(MyCustomClass className)
{
    ArgumentNullException.ThrowIfNull(|);

}
```

### sn - IfStringIsNullOrEmpty

Creates a conditional block based on a string, appending a new line with an indent.

```cs
public void MyFunction(string name)
{
    if(string.IsNullOrEmpty(name))
        |
}
```

### st - DefaultedString

Creates a `string` property with a default value.

```cs
public string | { get; set; } = string.Empty;
```

### jp - JsonPropertyName

Creates an attribute from the `System.Text.Json` namespace for a serializable property.

```cs
[JsonPropertyName("|")]
```
