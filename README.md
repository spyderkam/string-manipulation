# String Manipulation for Boeing

The `Text` class takes in string data and gives out needed data.

## Finding Strings
The `find_word` method returns a tuple of the number of times a word of interest appears in a text as well as the starting position of the first charachter of that word.

```
text = Text(input_text)
finder = text.find_word
```

Here, applying `finder(word)[0]` will return the number of times `word` appears in `input_text` and `finder(word)[1]` will return the starting positions of the first charachter of `word` in `input_text`. <br>

## Dividing Large Files Into Smaller Files
The `create_smaller_files` method of the `Text` class divides the input file into a desired amount of smaller files. It can make the output files into any desired extension.

```
with open("big.txt", "r") as f:
    file_lines = f.readlines()

file_lines = [lines.replace("\n", '') for lines in file_lines]
lines = Text(file_lines)
lines.create_smaller_files(NO_lines=len(file_lines), divfiles=12, extension='dat')
```
`NO_lines` is the number of lines in the input files and `divfiles` is the number of files the input file will be divided into. The file could potential be divided into one more than `divfiles` depending on the number of lines in the input file. The new files will be named `𝚤_file.extension` where `𝚤` starts from `0`. <br>
&nbsp;&nbsp;&nbsp;&nbsp;To start, please make sure a directory named `new_files` is in the directory which `string_manipulator` is executed.
