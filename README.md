# Mr-Niko.github.io
*(the place for my personal HTML training)*

## Usefull Extentions

here [settup_to_work.md](settup_to_work.md)

## markdown examples 
*(as said before in other words: it's my testing)*

### Table of Contents

- [VS Code](#VS-Code)
- [javascript code example](#java-ex)
- [image and line break](#image-and-line)
- []()
- []()
- []()



<a name="VS-Code"></a>**VS Code** provides two different scopes for settings:

- **User Settings** - Settings that apply globally to any instance of VS Code you open.
- **Workspace Settings** - Settings stored inside your workspace and only apply when the workspace is opened.

Workspace settings override user settings. Workspace settings are specific to a project and can be shared across developers on a project.

> **Note**: A VS Code "workspace" is usually just your project root folder. Workspace settings as well as [debugging](https://code.visualstudio.com/docs/editor/debugging) and [task](https://code.visualstudio.com/docs/editor/tasks) configurations are stored at the root in a `.vscode` folder. You can also have more than one root folder in a VS Code workspace through a feature called [Multi-root workspaces](https://code.visualstudio.com/docs/editor/multi-root-workspaces)

<a name="java-ex"></a> javascript code example
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

> `This is a block code`
>> and more
>>> some more


```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
<a name="image-and-line"></a>
## the way to insert image and line break\ _this is not work in header_
> `images_folder/img.jpg`  < works\
 `/images_folder/img.jpg`  < this will work on webserver's only (please read the note!)
 
## the way to insert image and line break <br /> _perfect `<br />`_ 
> `images_folder/img.jpg`  < works <br />
 `/images_folder/img.jpg`  < this will work on webserver's only (please read the note!)

temp text:
How to do that? 
- open **VS Code**
- `Ctrl+Shft+X` → in the search field `ritwickdey.liveserver`
- click **install**
- re-open **VS Code** after *extention be installed* 