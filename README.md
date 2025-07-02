# SmartComments

This module extends the options for **StripTags** in the input settings of text fields with the option of inserting single or multi-line comments, which are either only visible in the input field or are also output as HTML comments in the markup. The syntax corresponds to HTML or PHP, as would be used in hard-coded source text.

By default, ProcessWire allows HTML tags, which enables the use of HTML comments. If Markdown is used as Textformatter, one-line comments can also be entered with the Markdown syntax: `[//]: # “comment”` or `[//]: # (comment)`  These are not output in the markup.

Without this module, it is not possible to add multi-line comments that were not output. It is also not possible to remove HTML but exclude comments from beeing stripped, which might be useful for input fields that use Markdown text formatting.

## Syntax & Visibility
Behavior when the **‘Allow comments’** option is selected for **StripTags** in the input field settings.

|Syntax|ProcessPageEdit (Inputfield)|formatted output|ProcessPageEdit (headline)[^1]|ProcessPageList (label)[^2]|
|:-|:-:|:-:|:-:|:-:|
|`<!-- comment -->`|✓|✓|✓|×|
|`<?/* comment */?>`|✓|×|×|×|

[^1]: if the option is used in the system field **‘title’**.
[^2]: if the field is used as a label in **ProcessPageList** according to the settings in the module or template.