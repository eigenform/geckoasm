Scripts/experiments for compiling Gecko codehandler input.

## Usage

Read `geckoasm --help` for more details. `geckoasm` expects assembly files to have a header with
some supporting information. For example:

```
# @name: my gecko code
# @author: meta
# @code: c2
# @addr: 0x80063748

< assembly >
....
```

Only `C2` and `06` codehandler commands are supported right now.
If you want to patch single instructions and include the corresponding `04` commands 
in the output, you can also include comments like this anywhere in the file:

```
# @80f347ac: nop
# @80093334: nop

# @803647fc: blr 0x80043650
# @801a5544: lis r1, 0x3000
# @801a5548: nop
```
