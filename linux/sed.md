# SED Cheat-Sheet
**sed** ("stream editor") is a **Linux ([[linux]])**, and Unix utility that parses and transforms text, using a simple, compact programming language.

TMP
Replace the first occurrence of the pattern Steven with Kate in the file some.txt. Pass the `-i` option to update the some.txt file: 
```
sed -i 's/Steven/Kate/' some.txt
```

Replace the all occurrences of the pattern Steven with Kate in the file some.txt append `/g` to the search pattern. Here the `/` acts as a delimiter and `g` let's sed know to replace globally:
```
sed 's/Steven/Kate/g' some.txt
```

Replace the all occurrences of the pattern Steven with Kate in the file some.txt regradless of character case append `/gI` to the search pattern. Here the `/` acts as a delimiter and `g` let's sed know to replace globally & `I` to ignorecase:
```
sed 's/Steven/Kate/gI' some.txt
```

#find-replace