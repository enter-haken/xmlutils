xmltools
========

The *xmltools* project is a collection of tiny tools, which helps processing json data within console


### prettyXml

```
usage: prettyXml [-h] [-o FILENAME]

pretty prints xml

optional arguments:
  -h, --help            show this help message and exit
  -o FILENAME, --fileName FILENAME
                        load xml from stdin or from file. read one xml per
                        line. (default: -)
```

#### Example

```
$ echo "<?xml version=\"1.0\" ?><Test><a att=\"Test\">Content of a</a><foo>foo content</foo></Test>" | prettyXml
<?xml version="1.0" ?>
<Test>
        <a att="Test">Content of a</a>
        <foo>foo content</foo>
</Test>

```

### Contact

Jan Frederik Hake, <jan_hake@gmx.de>. [@enter\_haken](https://twitter.com/enter_haken) on Twitter.
