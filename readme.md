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
### queryXml

```
usage: queryXml [-h] [-o FILENAME] -n NODE [-x] [-a]

querys xml data for nodes and attributes

optional arguments:
  -h, --help            show this help message and exit
  -o FILENAME, --fileName FILENAME
                        choose file containing bson data. (default: -)
  -n NODE, --node NODE  print all node content (default: None)
  -x, --innerXml        get inner xml (default: False)
  -a, --attributes      get tag arguments (default: False)
```

#### Example

```
$ echo "<?xml version=\"1.0\" ?><Test><a att=\"Test\">Content of a</a><foo>foo content</foo></Test>" | queryXml -n a
Content of a

$ echo "<?xml version=\"1.0\" ?><Test><a att=\"Test\">Content of a</a><foo>foo content</foo></Test>" | queryXml -n a -x
<a att="Test">Content of a</a>

$ echo "<?xml version=\"1.0\" ?><Test><a att=\"Test\">Content of a</a><foo>foo content</foo></Test>" | queryXml -n a -a
Content of a | attributes: att:Test
```

### Contact

Jan Frederik Hake, <jan_hake@gmx.de>. [@enter\_haken](https://twitter.com/enter_haken) on Twitter.
