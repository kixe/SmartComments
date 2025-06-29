# SmartComments

Dieses Modul erweitert die Optionen für **StripTags** in den Eingabeeinstellungen von Textfeldern um die Möglichkeit, ein- oder mehrzeilige Kommentare einzufügen, die entweder nur im Eingabefeld sichtbar sind, oder auch als HTML-Kommentare im Markup ausgegeben werden. Die Syntax entspricht HTML bzw. PHP, wie sie auch in hart kodiertem Quelltext Anwendung findet.

ProcessWire erlaubt standardmäßig HTML-Tags, was die Verwendung von HTML-Kommentaren ermöglicht. Wenn Markdown als Textformatter verwendet wird, können einzeilige Kommentare auch mit der Markdown-Syntax eingegeben werden: `[//]: # „comment“` oder `[//]: # (comment)` Diese werden nicht im Markup ausgegeben.

Ohne dieses Modul ist es nicht möglich, mehrzeilige Kommentare hinzuzufügen, die nicht ausgegeben wurden. Es ist auch nicht möglich, HTML zu entfernen, aber Kommentare davon auszuschließen, was für Eingabefelder, die Markdown-Textformatierung verwenden, nützlich sein könnte.

## Syntax & Sichtbarkeit

Verhalten, wenn die Option **‚Kommentare zulassen‘** für **StripTags** in den Eingabefeld-Einstellungen ausgewählt ist.

|Syntax|ProcessPageEdit (Inputfield)|formatierter Output|ProcessPageEdit (Headline)[^1] |ProcessPageList (Label)[^2] |
|:-|:-:|:-:|:-:|:-:|
|`<!-- comment -->`|✓|✓|✓|×|
|`<?/* comment */?>`|✓|×|×|×|

[^1]: wenn die Option im Systemfeld **‚title‘** angewendet wird.
[^2]: wenn das Feld, entsprechend den Einstellungen im Modul oder Template als Label in **ProcessPageList** verwendet wird.

