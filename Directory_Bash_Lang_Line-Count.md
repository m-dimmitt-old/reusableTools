http://stackoverflow.com/questions/4822471/count-number-of-lines-in-a-git-repository

http://stackoverflow.com/questions/7470165/how-to-go-to-each-directory-and-execute-a-command

after downloading cloc through homebrew...
`brew install cloc`
##Cool Bash script 

go through each directory and give the line count for each language and give the line-count-sum for each directory. 

For my use as you will see in the example, My script was the topmost script which was a directory with sub directories. and the output is also shown. This should be scalable to as many sub directories as you would like as long as you continue the nesting statement correctly.
```
for d in ./*/ ; do (cd "$d" && for d in ./*/ ; do (cd "$d" && cloc $(git ls-files)); done); done

for d in ./*/ ; do (cd "$d" && ls); done

for d in ./*/ ; do (cd "$d" && !!); done

Michaels-MacBook-Pro-2:Parl_Comp zen1$ for d in ./*/ ; do (cd "$d" && !!); done
for d in ./*/ ; do (cd "$d" && for d in ./*/ ; do (cd "$d" && cloc $(git ls-files)); done); done
       7 text files.
       7 unique files.                              
       1 file ignored.

github.com/AlDanial/cloc v 1.68  T=0.02 s (390.2 files/s, 25687.6 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
D                                4             61             32            251
Markdown                         1              9              0             38
make                             1              0              0              4
-------------------------------------------------------------------------------
SUM:                             6             70             32            293
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
       7 text files.
       7 unique files.                              
       0 files ignored.

github.com/AlDanial/cloc v 1.68  T=0.02 s (293.0 files/s, 52107.1 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
Go                               7            165            282            798
-------------------------------------------------------------------------------
SUM:                             7            165            282            798
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
      49 text files.
      47 unique files.                              
      13 files ignored.

github.com/AlDanial/cloc v 1.68  T=0.10 s (399.5 files/s, 70409.4 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
Python                          33           1226           1026           3017
C                                4            327            337            888
Markdown                         1             11              0             28
YAML                             1              0              2             12
-------------------------------------------------------------------------------
SUM:                            39           1564           1365           3945
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
      37 text files.
      37 unique files.                              
      17 files ignored.

github.com/AlDanial/cloc v 1.68  T=0.03 s (777.5 files/s, 48746.6 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
R                               17             76            320            461
Markdown                         2            102              0            246
YAML                             1              0              0             49
-------------------------------------------------------------------------------
SUM:                            20            178            320            756
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
      11 text files.
      11 unique files.                              
       4 files ignored.

9 errors:
Unable to read:  include/libs/catch/catch.hpp
Unable to read:  include/libs/catch/catch_runner.hpp
Unable to read:  include/libs/catch/catch_with_main.hpp
Unable to read:  include/libs/exceptionpp
Unable to read:  libs/exceptionpp
Unable to read:  libs/stacktrace
Unable to read:  tutorial/include/libs/exceptionpp
Unable to read:  tutorial/libs/exceptionpp
Unable to read:  tutorial/libs/stacktrace

github.com/AlDanial/cloc v 1.68  T=0.03 s (270.5 files/s, 26546.4 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
C++                              4             94             25            407
Markdown                         1             23              0             65
C/C++ Header                     1             24             31             61
make                             2             20              3             32
-------------------------------------------------------------------------------
SUM:                             8            161             59            565
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
     278 text files.
     278 unique files.                                          
       1 file ignored.

github.com/AlDanial/cloc v 1.68  T=0.12 s (2377.4 files/s, 58619.0 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
JSON                           269              0              0           5884
C                                3             58             20            431
Python                           1             25             13            146
Lua                              2             21              0             79
Markdown                         1             31              0             44
make                             1             17             24             37
-------------------------------------------------------------------------------
SUM:                           277            152             57           6621
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
Saving session...
...saving history...truncating history files...
...completed.
-bash: cd: ./*/: No such file or directory
Saving session...
...saving history...truncating history files...
...completed.
-bash: cd: ./*/: No such file or directory
Saving session...
...saving history...truncating history files...
...completed.
      14 text files.
      14 unique files.                              
       4 files ignored.

github.com/AlDanial/cloc v 1.68  T=0.01 s (724.3 files/s, 21800.4 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
Scala                            9             56              1            209
Markdown                         1             14              0             21
-------------------------------------------------------------------------------
SUM:                            10             70              1            230
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
      57 text files.
      57 unique files.                              
      14 files ignored.

github.com/AlDanial/cloc v 1.68  T=0.07 s (644.5 files/s, 84766.0 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
Scala                           31            998            467           4124
XML                              6              4             15            178
Bourne Shell                     6             27              5            130
HTML                             2             13              0             66
YAML                             1              0              0             23
-------------------------------------------------------------------------------
SUM:                            46           1042            487           4521
-------------------------------------------------------------------------------
Saving session...
...saving history...truncating history files...
...completed.
Saving session...
...saving history...truncating history files...
...completed.
```
