---
layout: post
title: Git project statistic tool
date: 2016-03-20 12:57:35.000000000 -05:00
type: post
published: true
status: publish
comments: true
category: programming
tags: 
  - osx
  - git
author:
  login: miroadamy
  email: miro.adamy+blog@gmail.com
  display_name: miroadamy
  first_name: ''
  last_name: ''
---

# Git project statistic tool

Python based, requires Python 2.6+

Works OOTB on Mac

## Installation

* Download TAR from [Github](https://github.com/ejwa/gitinspector) 
* unzipped to /opt

```
➜  ll /opt/gitinspector-0.3.2
total 52K
-rw-r--r--  1 miro  999 Jul 29  2013 DESCRIPTION.txt
-rw-r--r--  1 miro  32K Jun 14  2013 LICENSE.txt
-rw-r--r--  1 miro   78 Jul  2  2013 MANIFEST.in
-rw-r--r--  1 miro  681 Jan 13  2014 README.txt
drwxr-xr-x 45 miro 1.5K Mar 20  2015 gitinspector
-rw-r--r--  1 miro 1.9K Jan 14  2014 setup.py
-rw-r--r--  1 miro  110 Jul 27  2013 stdeb.cfg
```

* create symlink from ~/bin (or from whatever directory on $PATH)

```
ln -s /opt/gitinspector-0.3.2/gitinspector/gitinspector.py ~/bin/gitinspector.py
  
➜  ~  ll ~/bin | grep gitin
lrwxr-xr-x 1 miro   52 Mar 20 16:06 gitinspector.py -> /opt/gitinspector-0.3.2/gitinspector/gitinspector.py
```

## Example

Look at groovy sources - https://github.com/apache/incubator-groovy

```
gitinspector.py -Tlr --since=2014-01-01 


The following historical commit information, by author, was found in the
repository:

Author                     Commits    Insertions      Deletions    % of changes
Alex Spurling                    1             2              6            0.01
Andre Steingress                 7           581            803            1.11
Andrew Hamilton                  1             9              1            0.01
Andrew Taylor                    3           242              0            0.19
Andrey Bloschetsov               2           699             48            0.60
Andy Wilkinson                   1             1              1            0.00
Anto                             2           119              1            0.10
Bartlomiej Stefanski             1             1              1            0.00
Bloshchetsov Andrey              3           783              0            0.63
Bobby Warner                     1             4              0            0.00
Carsten Lenz                     1            23              8            0.02
Cedric Champeau                347         36714          21247           46.56
Chris Earle                      2            16              6            0.02
Craig Andrews                    7           251             59            0.25
Danny Hyun                       1            10             10            0.02
Dominik Przybysz                 1            45              0            0.04
Esteban                          4            43              4            0.04
Fabio de Matos                   1             1             15            0.01
Frank Pavageau                  13           381            128            0.41
Graeme Rocher                    2           361             84            0.36
Guillaume Laforge               10            59             67            0.10
Gvaneyck                         2            31             55            0.07
Hubert Klein Ikkink              4           733             44            0.62
Jacopo Cappellato                4            89             97            0.15
Jake Gage                        1             1              1            0.00
Jan Matějka                      1             7             30            0.03
Jan Sykora                       2            13              6            0.02
Jason Winnebeck                  1            12              0            0.01
Jeff Sheets                      1           132             41            0.14
Jess Sightler                    1             4              0            0.00
Jim White                       24          1088            397            1.19
Jochen Kemnade                   3            25              1            0.02
Jochen Theodorou                94          2892           1137            3.24
John Hurst                       2            54             13            0.05
John Wagenleitner               31           460            620            0.87
Kamil Szymanski                  1            14             14            0.02
Keegan Witt                     11           565            188            0.60
Keith Suderman                   1             2              4            0.00
Kenneth Endfinger                5             8             12            0.02
Kent                             5           618             42            0.53
Kirill Vlasov                    5            91             95            0.15
Kris Marwood                     1             1              1            0.00
Lari Hotari                      4            49             25            0.06
Luke Daley                       1            44              4            0.04
Luke Kirby                       2            14              7            0.02
Manuel Prinz                     1             4              0            0.00
Marc Bogaerts                    2             8              8            0.01
Marc Guillemot                   1            37              2            0.03
Marcin Grzejszczak               1            56              5            0.05
Marcin Zajaczkowski              1             1              1            0.00
Martin Stockhammer               1             1              1            0.00
Matias Bjarland                  6          1415             98            1.22
Matt Whipple                     1             8              8            0.01
Michal Kordas                    1             1              1            0.00
Nathan Mische                    1            88             13            0.08
Nick Grealy                      2           144              4            0.12
Paolo Di Tommaso                 5           191             91            0.23
Pascal Schumacher               16           161            395            0.45
PascalSchumacher                 2            34              9            0.03
Paul King                      239         13417           8659           17.73
Persi                            1            27             27            0.04
Peter Ledbrook                   1             4              4            0.01
Peter Swire                      1             2              1            0.00
Radovan Synek                    1             1              1            0.00
Rahul Somasunderam               1             6              0            0.00
René Scheibe                     4            52            393            0.36
Richard Hightower                3           263            338            0.48
Sagar Sane                       1             1              1            0.00
Sargis Harutyunyan               7            88             25            0.09
Sergei Egorov                    1           182            141            0.26
Sergey Egorov                    9          1228            522            1.41
Shil S                          11            56             25            0.07
Shil Sinha                      19           220             77            0.24
Søren Berg Glasius               1             3              0            0.00
Thibault Kruse                   7           130            163            0.24
Tim Yates                        1            11              0            0.01
Tobias Schulte                   1             1              1            0.00
UEHARA Junji                     1             4              0            0.00
Wil Selwood                      1             5              1            0.00
Yannick Welsch                   1             3              1            0.00
Yu Kobayashi                    20          2693            202            2.33
aalmiray                         3            27              1            0.02
anand raman                      1             2              0            0.00
asa                              1            10              0            0.01
belkaram                         1             8              0            0.01
bpaulin                          1             1              1            0.00
graemerocher                     6           155             53            0.17
javaboon                        12         11038           2733           11.06
jfranco                          1             1              0            0.00
maciekwiso                       1             1              1            0.00
oreissig                         9           225            497            0.58
pascalschumacher                50           400           1497            1.52
paul-bjorkstrand                 1             1              1            0.00
paulk                           24           858            218            0.86
peter                           41          1865            487            1.89
qxo                              1             2              2            0.00
tomasbartalos                    1            15             15            0.02

Below are the number of rows from each author that have survived and are still
intact in the current revision:

Author                     Rows       % in comments
Alex Spurling                 2              100.00
Andre Steingress            447               44.97
Andrew Hamilton               9                0.00
Andrew Taylor               238               47.06
Andrey Bloschetsov          583               21.27
Andy Wilkinson                1                0.00
Anto                         73               31.51
Bartlomiej Stefanski          1              100.00
Bloshchetsov Andrey         189                7.94
Bobby Warner                  4                0.00
Carsten Lenz                 23                0.00
Cedric Champeau           29009               65.23
Chris Earle                  16               12.50
Craig Andrews               242                8.26
Danny Hyun                   10              100.00
Dominik Przybysz             45               33.33
Esteban                      38               50.00
Fabio de Matos                1                0.00
Frank Pavageau              342               18.71
Graeme Rocher               493               34.28
Guillaume Laforge            44               36.36
Gvaneyck                     31                9.68
Hubert Klein Ikkink         686              100.00
Jacopo Cappellato            29                3.45
Jake Gage                     1              100.00
Jan Matějka                   5               40.00
Jan Sykora                   12                0.00
Jason Winnebeck              12              100.00
Jeff Sheets                 114               57.02
Jess Sightler                 4                0.00
Jim White                   725               39.31
Jochen Kemnade               23               52.17
Jochen Theodorou           2666               13.17
John Hurst                   53                1.89
John Wagenleitner           452               31.42
Kamil Szymanski              14                0.00
Keegan Witt                 547               63.25
Keith Suderman                2                0.00
Kenneth Endfinger             7               28.57
Kent                        537               94.79
Kirill Vlasov                90                3.33
Kris Marwood                  1              100.00
Lari Hotari                  32               12.50
Luke Daley                   32               18.75
Luke Kirby                   14                7.14
Manuel Prinz                  4              100.00
Marc Bogaerts                 3                0.00
Marc Guillemot               37               13.51
Marcin Grzejszczak            5                0.00
Marcin Zajaczkowski           1                0.00
Martin Stockhammer            1                0.00
Matias Bjarland            1039               37.54
Matt Whipple                  2              100.00
Michal Kordas                 1              100.00
Nathan Mische                88               62.50
Nick Grealy                 136               47.06
Paolo Di Tommaso             60               50.00
Pascal Schumacher           552               76.45
Paul King                 11958               37.82
Persi                        27               25.93
Peter Ledbrook                4              100.00
Peter Swire                   2                0.00
Radovan Synek                 1                0.00
Rahul Somasunderam            6               16.67
René Scheibe                 51                7.84
Richard Hightower           122               75.41
Sagar Sane                    1              100.00
Sargis Harutyunyan           75                0.00
Sergey Egorov               923               36.94
Shil S                      199               22.11
Shil Sinha                   68               16.18
Søren Berg Glasius            3                0.00
Thibault Kruse              106               41.51
Tim Yates                    11               54.55
Tobias Schulte                1              100.00
UEHARA Junji                  4                0.00
Wil Selwood                   5                0.00
Yannick Welsch                2              100.00
Yu Kobayashi               2515               66.80
aalmiray                     25               60.00
anand raman                   2              100.00
asa                          10                0.00
belkaram                      8                0.00
bpaulin                       1                0.00
javaboon                   6409               10.45
jfranco                       1                0.00
maciekwiso                    1              100.00
oreissig                    221               20.36
paul-bjorkstrand              1              100.00
peter                      1349                8.30
qxo                           2                0.00
tomasbartalos                15                0.00

The following history timeline has been gathered from the repository:

Author                  2014-01    2014-02    2014-03    2014-04    2014-05 
Andre Steingress                         .          -                       
Andrew Hamilton                                     .                       
Andrey Bloschetsov                                  +          .            
Bloshchetsov Andrey                                                      ++ 
Cedric Champeau       ---++++++         ++   --++++++       -+++        +++ 
Guillaume Laforge                                   .          .          . 
Jan Sykora                                                     .            
Jeff Sheets                   +                                             
Jess Sightler                                                             . 
Jim White                                .          .          .            
Jochen Theodorou             ++          .          .          .         ++ 
John Wagenleitner                                   .                       
Kenneth Endfinger                                              .          . 
Lari Hotari                                                    .            
Luke Kirby                                                                . 
Nathan Mische                                                  .            
Paolo Di Tommaso            -++                                           . 
Pascal Schumacher            -+          .                     .            
Paul King              ---+++++                     +  ---++++++  --+++++++ 
Richard Hightower                        .                                  
Sergey Egorov                                                             . 
Thibault Kruse                -                                             
Tim Yates                                .                                  
Yu Kobayashi                                                              . 
aalmiray                      .                                             
javaboon                          -+++++++                                . 
Modified Rows:             2250      21190       6939      10574       2928 

Author                  2014-06    2014-07    2014-08    2014-09    2014-10 
Bloshchetsov Andrey                                            +            
Cedric Champeau              ++         ++                     +  +++++++++ 
Craig Andrews                ++                                .            
Guillaume Laforge                        .                                  
Jim White                                           +                       
Jochen Theodorou              .          .                     .   -+++++++ 
John Wagenleitner                        .                                  
Keegan Witt                   .                                             
Kenneth Endfinger             .                                             
Kent                                    ++                                  
Luke Daley                                                                + 
Manuel Prinz                                        .                       
Marc Guillemot                .                                             
Martin Stockhammer                                                        . 
Matias Bjarland                             +++++++++                       
Pascal Schumacher                                                    ------ 
Paul King              ----++++  ---++++++        -++  -----++++          . 
Peter Ledbrook                .                                             
Peter Swire                                                               . 
Tobias Schulte                                                 .            
Wil Selwood                   .                                             
Yu Kobayashi                 ++    +++++++                                  
paul-bjorkstrand                                                          . 
Modified Rows:             1706       6066       1233       3663       1017 

Author                  2014-11    2014-12    2015-01    2015-02    2015-03 
Andrew Taylor                                                             . 
Andy Wilkinson                                      .                       
Anto                                                                      . 
Bobby Warner                             .                                  
Carsten Lenz                  .                                             
Cedric Champeau        --++++++       ++++      -++++  --+++++++ ++++++++++ 
Craig Andrews                                                             . 
Frank Pavageau                                                            . 
Jason Winnebeck                                                           . 
Jochen Theodorou              .          .   ---+++++         ++          . 
Kamil Szymanski                                                .            
Marcin Grzejszczak                       .                                  
Marcin Zajaczkowski           .                                             
Matias Bjarland       -++++++++                                             
Paolo Di Tommaso                         .                                  
Pascal Schumacher             .          .                     .          . 
Paul King                     .         ++        -++          .          + 
Radovan Synek                                       .                       
René Scheibe                                                             -- 
Sagar Sane                               .                                  
Sargis Harutyunyan            .          .                                  
Sergey Egorov                                       +                       
UEHARA Junji                                        .                       
Yu Kobayashi                             .         ++      +++++            
peter                             -+++++++                                . 
Modified Rows:             1680       4549       1873        757       2860 

Author                  2015-04    2015-05    2015-06    2015-07    2015-08 
Alex Spurling                 .                                             
Cedric Champeau       ----+++++                    ++          .            
Danny Hyun                                          .                       
Esteban                                  .                                  
Fabio de Matos                                      .                       
Gvaneyck                                            .                       
Jacopo Cappellato                        .                                  
Jochen Theodorou              .                                .            
John Hurst                               .                                  
Keegan Witt                   .                     .          .          . 
Marc Bogaerts                                                  .            
Matt Whipple                                                              . 
Nick Grealy                                         +                       
Paul King                     .  ---++++++  --------+        +++        +++ 
Persi                                                          .            
Shil S                                   .                     .          . 
Shil Sinha                                                                . 
aalmiray                                            .                       
bpaulin                                             .                       
pascalschumacher                                 ----          -            
paulk                                                   ++++++++  --+++++++ 
qxo                                                                       . 
tomasbartalos                                       .                       
Modified Rows:            36249       1842       2104        619        623 

Author                  2015-09    2015-10    2015-11    2015-12    2016-01 
Anto                                                                  +++++ 
Cedric Champeau       --+++++++                                             
Chris Earle                                                    .          . 
Craig Andrews                            .                                  
Dominik Przybysz              .                                             
Esteban                       .                                             
Frank Pavageau                .                    ++        -++            
Graeme Rocher                 .                                             
Jacopo Cappellato                                   .                       
Jochen Kemnade                           .          .                       
Jochen Theodorou                                    .                       
John Wagenleitner                        .  --------+        -++    ---++++ 
Keegan Witt                                         .  --+++++++            
Keith Suderman                           .                                  
Kirill Vlasov                                                        ---+++ 
Michal Kordas                            .                                  
PascalSchumacher                                    .                       
Paul King                                           .                       
Rahul Somasunderam                       .                                  
Sergei Egorov                 .                                             
Sergey Egorov               -++                                             
Shil S                                   .                                . 
Shil Sinha                    .          .          .          .       ++++ 
Søren Berg Glasius                                  .                       
Thibault Kruse                .          +                                  
anand raman                              .                                  
belkaram                                                                  . 
graemerocher                                        .         ++            
jfranco                                             .                       
pascalschumacher                  --------          -          .   -----+++ 
paulk                                   ++          .                       
Modified Rows:             6898       1101        900       1469        820 

Author                  2016-02    2016-03 
Andrew Taylor           +++++++            
Bartlomiej Stefanski          .            
Frank Pavageau                .            
Hubert Klein Ikkink               ++++++++ 
Jake Gage                                . 
Jan Matějka                              . 
John Wagenleitner             +          . 
Kirill Vlasov                            . 
Kris Marwood                             . 
Marc Bogaerts                            . 
PascalSchumacher                         . 
Shil Sinha                    .          . 
Yannick Welsch                .            
asa                           .            
maciekwiso                               . 
oreissig               ---+++++       ---- 
pascalschumacher              .       --++ 
paulk                       -++          . 
Modified Rows:              729       1855 

The following repsonsibilties, by author, were found in the current revision of
the repository (comments are exluded from the line count, if possible):

Andre Steingress is mostly responsible for:
   112 subprojects/groovy-test/src/main/java/groovy/test/GroovyAssert.java
    28 ...ojects/groovy-json/src/main/java/groovy/json/internal/CharScanner.java
    28 src/main/org/codehaus/groovy/classgen/InnerClassCompletionVisitor.java
    18 subprojects/groovy-test/src/main/java/groovy/util/GroovyTestCase.java
    11 src/main/org/codehaus/groovy/classgen/asm/BytecodeHelper.java
     5 src/main/org/codehaus/groovy/runtime/MethodRankHelper.java
     3 subprojects/groovy-ant/src/main/java/org/codehaus/groovy/ant/Groovy.java
     3 ...in/org/codehaus/groovy/runtime/metaclass/MethodSelectionException.java
     3 src/main/groovy/inspect/Inspector.java
     2 src/test/org/codehaus/groovy/runtime/TupleListTest.java

Andrew Hamilton is mostly responsible for:
     9 src/main/groovy/util/Node.java

Andrew Taylor is mostly responsible for:
    47 src/main/org/codehaus/groovy/util/IteratorBufferedIterator.java
    38 src/main/org/codehaus/groovy/util/ListBufferedIterator.java
    19 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
     7 src/main/groovy/util/BufferedIterator.java
     6 ...ojects/groovy-json/src/main/java/groovy/json/internal/NumberValue.java
     6 ...ojects/groovy-json/src/main/java/groovy/json/internal/CharScanner.java
     3 ...cts/groovy-json/src/main/java/groovy/json/internal/JsonFastParser.java

Andrey Bloschetsov is mostly responsible for:
   394 subprojects/groovy-json/src/main/java/groovy/json/JsonOutput.java
    58 subprojects/groovy-json/src/main/java/groovy/json/JsonDelegate.java
     5 ...ojects/groovy-json/src/main/java/groovy/json/internal/CharScanner.java
     1 ...ojects/groovy-json/src/main/java/groovy/json/internal/NumberValue.java
     1 ...src/main/java/groovy/json/internal/JsonParserUsingCharacterSource.java

Andy Wilkinson is mostly responsible for:
     1 ...templates/src/main/groovy/groovy/text/markup/MarkupTemplateEngine.java

Anto is mostly responsible for:
    49 ...test/groovy/org/codehaus/groovy/tools/groovydoc/GroovyDocToolTest.java
     1 src/main/org/codehaus/groovy/control/ResolveVisitor.java

Bloshchetsov Andrey Evgenyevich is mostly responsible for:
    89 ...ojects/groovy-json/src/main/java/groovy/json/StreamingJsonBuilder.java
    85 subprojects/groovy-json/src/main/java/groovy/json/JsonBuilder.java

Bobby Warner is mostly responsible for:
     4 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java

Carsten Lenz is mostly responsible for:
    23 ...ects/groovy-json/src/main/java/groovy/json/internal/JsonParserLax.java

Cedric Champeau is mostly responsible for:
   631 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingVisitor.java
   576 ...oovy/org/codehaus/groovy/macro/matcher/ContextualClassCodeVisitor.java
   478 src/main/org/codehaus/groovy/transform/trait/TraitASTTransformation.java
   414 src/main/org/codehaus/groovy/transform/trait/TraitComposer.java
   405 ...macro/src/main/groovy/org/codehaus/groovy/macro/matcher/ASTFinder.java
   387 ...main/org/codehaus/groovy/transform/trait/TraitReceiverTransformer.java
   384 ...n/org/codehaus/groovy/transform/stc/AbstractTypeCheckingExtension.java
   347 .../groovy-templates/src/main/groovy/groovy/text/markup/BaseTemplate.java
   325 .../groovy/org/codehaus/groovy/macro/transform/TransformingMacroTrap.java
   317 src/main/org/codehaus/groovy/classgen/FinalVariableAnalyzer.java

Chris Earle is mostly responsible for:
     9 src/main/org/codehaus/groovy/vmplugin/v7/IndyInterface.java
     4 src/main/org/codehaus/groovy/control/CompilerConfiguration.java
     1 src/main/org/codehaus/groovy/classgen/asm/WriterController.java

Craig Andrews is mostly responsible for:
    81 src/main/org/codehaus/groovy/reflection/ClassInfo.java
    68 src/main/org/codehaus/groovy/reflection/GroovyClassValuePreJava7.java
    35 src/main/org/codehaus/groovy/reflection/GroovyClassValueFactory.java
    14 src/main/org/codehaus/groovy/reflection/v7/GroovyClassValueJava7.java
    13 src/main/org/codehaus/groovy/reflection/GroovyClassValue.java
     5 src/main/groovy/lang/ExpandoMetaClass.java
     4 src/main/org/codehaus/groovy/runtime/IOGroovyMethods.java
     2 ...roovy-templates/src/main/groovy/groovy/text/GStringTemplateEngine.java

Dominik Przybysz is mostly responsible for:
    30 ...vy-nio/src/main/java/org/codehaus/groovy/runtime/NioGroovyMethods.java

Esteban is mostly responsible for:
    11 subprojects/groovy-json/src/main/java/groovy/json/JsonOutput.java
     8 src/main/org/codehaus/groovy/runtime/ResourceGroovyMethods.java

Fabio de Matos is mostly responsible for:
     1 subprojects/groovy-json/src/main/java/groovy/json/internal/Dates.java

Frank Pavageau is mostly responsible for:
   138 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingSupport.java
    75 ...rg/codehaus/groovy/classgen/asm/sc/bugs/support/Groovy7538Support.java
    33 ...rg/codehaus/groovy/classgen/asm/sc/bugs/support/Groovy7363Support.java
    18 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingVisitor.java
     8 ...rg/codehaus/groovy/classgen/asm/sc/bugs/support/Groovy7365Support.java
     5 src/main/org/codehaus/groovy/ast/ClassNode.java
     1 src/main/org/codehaus/groovy/ast/GenericsType.java

Graeme Rocher is mostly responsible for:
   246 ...ojects/groovy-json/src/main/java/groovy/json/StreamingJsonBuilder.java
    78 subprojects/groovy-json/src/main/java/groovy/json/JsonOutput.java

Guillaume Laforge is mostly responsible for:
    18 ...vy-nio/src/main/java/org/codehaus/groovy/runtime/NioGroovyMethods.java
     7 src/main/org/codehaus/groovy/antlr/AntlrParserPlugin.java
     1 subprojects/groovy-test/src/main/java/groovy/util/GroovyAssert.java
     1 subprojects/groovy-json/src/main/java/groovy/json/internal/CharBuf.java
     1 src/main/org/codehaus/groovy/transform/ASTTransformationVisitor.java

Gvaneyck is mostly responsible for:
    28 ...ovy-json/src/main/java/groovy/json/internal/ReaderCharacterSource.java

Jacopo Cappellato is mostly responsible for:
    18 src/main/org/codehaus/groovy/tools/FileSystemCompiler.java
     7 src/main/groovy/lang/MetaClassImpl.java
     3 src/main/groovy/ui/GroovyMain.java

Jan Matějka is mostly responsible for:
     3 src/main/org/codehaus/groovy/control/CompilerConfiguration.java

Jan Sykora is mostly responsible for:
     8 src/main/org/codehaus/groovy/tools/javac/JavaStubGenerator.java
     2 src/main/org/codehaus/groovy/tools/javac/JavaStubCompilationUnit.java
     2 src/main/org/codehaus/groovy/tools/javac/JavaAwareCompilationUnit.java

Jeff Sheets is mostly responsible for:
    49 subprojects/groovy-sql/src/main/java/groovy/sql/Sql.java

Jess Sightler is mostly responsible for:
     4 src/main/groovy/lang/GroovyShell.java

Jim White is mostly responsible for:
    90 src/main/org/codehaus/groovy/transform/SourceURIASTTransformation.java
    43 src/main/groovy/lang/GroovyShell.java
    39 src/main/groovy/ui/GroovySocketServer.java
    31 src/main/groovy/ui/GroovyMain.java
    30 src/main/org/codehaus/groovy/transform/BaseScriptASTTransformation.java
    25 src/main/org/codehaus/groovy/runtime/InvokerHelper.java
    19 src/main/org/codehaus/groovy/ast/ClassNode.java
    18 src/main/org/codehaus/groovy/ast/ModuleNode.java
    16 src/test/groovy/lang/ScriptTest.java
    16 src/main/groovy/transform/SourceURI.java

Jochen Kemnade is mostly responsible for:
     5 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
     5 src/main/groovy/util/BuilderSupport.java
     1 src/main/org/codehaus/groovy/runtime/NullObject.java

Jochen Theodorou is mostly responsible for:
   367 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingSupport.java
   192 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingVisitor.java
   130 src/main/org/codehaus/groovy/ast/tools/GenericsUtils.java
   129 src/main/org/codehaus/groovy/vmplugin/v7/Selector.java
    97 src/main/org/codehaus/groovy/vmplugin/v7/IndyArrayAccess.java
    96 ...rg/codehaus/groovy/runtime/typehandling/DefaultTypeTransformation.java
    79 src/main/org/codehaus/groovy/classgen/asm/InvocationWriter.java
    78 src/main/org/codehaus/groovy/control/ResolveVisitor.java
    71 src/main/org/codehaus/groovy/vmplugin/v7/Java7.java
    66 ...main/org/codehaus/groovy/runtime/metaclass/MultipleSetterProperty.java

John Hurst is mostly responsible for:
    27 src/main/org/codehaus/groovy/transform/AbstractASTTransformation.java
    17 src/main/org/codehaus/groovy/ast/tools/GeneralUtils.java
     2 src/main/org/codehaus/groovy/transform/SortableASTTransformation.java
     2 .../org/codehaus/groovy/transform/EqualsAndHashCodeASTTransformation.java
     1 src/main/org/codehaus/groovy/transform/ImmutableASTTransformation.java
     1 ...rg/codehaus/groovy/transform/ExternalizeVerifierASTTransformation.java
     1 ...org/codehaus/groovy/transform/ExternalizeMethodsASTTransformation.java
     1 src/main/org/codehaus/groovy/transform/AutoCloneASTTransformation.java

John Wagenleitner is mostly responsible for:
    37 src/main/org/codehaus/groovy/runtime/ConversionHandler.java
    31 ...ects/groovy-json/src/main/java/groovy/json/internal/JsonParserLax.java
    29 ...cts/groovy-json/src/main/java/groovy/json/internal/JsonFastParser.java
    29 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
    28 subprojects/groovy-sql/src/main/java/groovy/sql/Sql.java
    28 subprojects/groovy-json/src/main/java/groovy/json/JsonBuilder.java
    18 src/main/org/codehaus/groovy/util/ListHashMap.java
    17 .../groovy-console/src/main/groovy/groovy/ui/SystemOutputInterceptor.java
    17 src/main/groovy/util/GroovyScriptEngine.java
    13 src/main/org/codehaus/groovy/util/ReferenceManager.java

Kamil Szymanski is mostly responsible for:
     2 subprojects/groovy-xml/src/main/java/groovy/xml/dom/DOMCategory.java
     2 ...rojects/groovy-json/src/main/java/groovy/json/internal/Exceptions.java
     2 src/main/org/codehaus/groovy/vmplugin/v7/Selector.java
     2 src/main/org/codehaus/groovy/transform/SynchronizedASTTransformation.java
     2 src/main/org/codehaus/groovy/transform/PackageScopeASTTransformation.java
     1 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingVisitor.java
     1 src/main/org/codehaus/groovy/tools/GroovyStarter.java
     1 src/main/org/codehaus/groovy/classgen/InnerClassVisitor.java
     1 src/main/org/codehaus/groovy/antlr/AntlrParserPlugin.java

Keegan Witt is mostly responsible for:
    81 ...vy-nio/src/main/java/org/codehaus/groovy/runtime/NioGroovyMethods.java
    67 src/main/org/codehaus/groovy/runtime/ResourceGroovyMethods.java
    44 src/main/org/codehaus/groovy/runtime/IOGroovyMethods.java
     6 src/main/org/codehaus/groovy/classgen/asm/WriterController.java
     1 .../src/main/java/org/codehaus/groovy/tools/groovydoc/FileOutputTool.java
     1 src/main/org/codehaus/groovy/control/CompilerConfiguration.java
     1 src/main/org/codehaus/groovy/classgen/ClassCompletionVerifier.java

Keith Suderman is mostly responsible for:
     2 src/main/org/codehaus/groovy/runtime/GroovyCategorySupport.java

Kenneth Endfinger is mostly responsible for:
     1 ...src/main/java/groovy/json/internal/JsonParserUsingCharacterSource.java
     1 ...ects/groovy-json/src/main/java/groovy/json/internal/JsonParserLax.java
     1 ...roovy-json/src/main/java/groovy/json/internal/JsonParserCharArray.java
     1 ...cts/groovy-json/src/main/java/groovy/json/internal/JsonFastParser.java
     1 src/main/groovy/lang/ClosureException.java

Kent is mostly responsible for:
    14 src/test/org/codehaus/groovy/runtime/DefaultGroovyStaticMethodsTest.java
     5 src/main/groovy/lang/MetaClassImpl.java
     4 src/main/org/codehaus/groovy/runtime/DefaultGroovyStaticMethods.java
     2 src/main/groovy/lang/MetaMethod.java
     2 src/main/groovy/lang/MetaBeanProperty.java
     1 src/main/groovy/lang/MetaClassRegistry.java

Kirill Vlasov is mostly responsible for:
     6 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
     5 src/main/org/codehaus/groovy/antlr/AntlrParserPlugin.java
     4 src/main/org/codehaus/groovy/vmplugin/v7/IndyInterface.java
     4 src/main/org/codehaus/groovy/transform/AnnotationCollectorTransform.java
     4 src/main/org/codehaus/groovy/tools/shell/util/Logger.java
     4 src/main/groovy/util/FactoryBuilderSupport.java
     3 src/main/org/codehaus/groovy/transform/ImmutableASTTransformation.java
     3 src/main/org/codehaus/groovy/tools/javac/JavaAwareCompilationUnit.java
     3 src/main/org/codehaus/groovy/ast/VariableScope.java
     2 subprojects/groovy-sql/src/main/java/groovy/sql/DataSet.java

Lari Hotari is mostly responsible for:
    28 src/main/org/codehaus/groovy/reflection/ClassInfo.java

Luke Daley is mostly responsible for:
    12 ...vy/tools/groovydoc/testfiles/staticInit/JavaWithFailingStaticInit.java
    12 ...test/groovy/org/codehaus/groovy/tools/groovydoc/GroovyDocToolTest.java
     2 ...ain/java/org/codehaus/groovy/tools/groovydoc/SimpleGroovyClassDoc.java

Luke Kirby is mostly responsible for:
    12 src/main/org/codehaus/groovy/control/ResolveVisitor.java
     1 subprojects/groovy-ant/src/main/java/org/codehaus/groovy/ant/Groovyc.java

Marc Bogaerts is mostly responsible for:
     1 src/main/org/codehaus/groovy/transform/BuilderASTTransformation.java
     1 src/main/groovy/transform/builder/InitializerStrategy.java
     1 src/main/groovy/transform/builder/DefaultStrategy.java

Marc Guillemot is mostly responsible for:
    32 ...jects/groovy-xml/src/main/java/groovy/xml/NamespaceBuilderSupport.java

Marcin Grzejszczak is mostly responsible for:
     5 src/main/groovy/transform/builder/InitializerStrategy.java

Marcin Zajaczkowski is mostly responsible for:
     1 src/main/org/codehaus/groovy/ast/AnnotationNode.java

Martin Stockhammer is mostly responsible for:
     1 subprojects/groovy-json/src/main/java/groovy/json/internal/IO.java

Matias Bjarland is mostly responsible for:
   582 ...ovy-templates/src/main/groovy/groovy/text/StreamingTemplateEngine.java
    38 ...oovy-templates/src/main/groovy/groovy/text/TemplateParseException.java
    29 ...-templates/src/main/groovy/groovy/text/TemplateExecutionException.java

Nathan Mische is mostly responsible for:
    33 subprojects/groovy-sql/src/main/java/groovy/sql/Sql.java

Nick Grealy is mostly responsible for:
    28 src/main/org/codehaus/groovy/control/CompilerConfiguration.java
    14 subprojects/groovy-ant/src/main/java/org/codehaus/groovy/ant/Groovyc.java
    10 src/main/org/codehaus/groovy/tools/FileSystemCompiler.java
     8 subprojects/groovy-ant/src/main/java/org/codehaus/groovy/ant/Groovy.java
     6 src/main/org/codehaus/groovy/classgen/AsmClassGenerator.java
     4 src/test/org/codehaus/groovy/control/CompilerConfigurationTest.java
     2 src/main/groovy/ui/GroovyMain.java

Paolo Di Tommaso is mostly responsible for:
    27 ...vy-nio/src/main/java/org/codehaus/groovy/runtime/NioGroovyMethods.java
     3 src/main/groovy/lang/GString.java

Pascal Schumacher is mostly responsible for:
    23 src/main/org/codehaus/groovy/vmplugin/v7/IndyArrayAccess.java
    12 src/main/org/codehaus/groovy/transform/DelegateASTTransformation.java
    11 src/main/groovy/transform/builder/ExternalStrategy.java
    10 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
     9 subprojects/groovy-json/src/main/java/groovy/json/internal/Sys.java
     9 src/main/org/codehaus/groovy/control/CompilerConfiguration.java
     7 src/main/org/codehaus/groovy/transform/BuilderASTTransformation.java
     7 src/main/groovy/transform/builder/SimpleStrategy.java
     5 ...test/groovy/org/codehaus/groovy/tools/groovydoc/GroovyDocToolTest.java
     4 subprojects/groovy-sql/src/main/java/groovy/sql/Sql.java

Paul King is mostly responsible for:
   649 src/main/org/codehaus/groovy/runtime/StringGroovyMethods.java
   614 src/main/org/codehaus/groovy/ast/tools/GeneralUtils.java
   532 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
   309 src/main/groovy/transform/builder/InitializerStrategy.java
   258 src/main/org/codehaus/groovy/transform/AbstractASTTransformation.java
   237 src/main/org/codehaus/groovy/transform/ImmutableASTTransformation.java
   202 src/main/org/codehaus/groovy/transform/BuilderASTTransformation.java
   198 ...ain/org/codehaus/groovy/transform/MapConstructorASTTransformation.java
   186 src/main/org/codehaus/groovy/transform/SortableASTTransformation.java
   180 src/main/groovy/transform/builder/DefaultStrategy.java

Persi is mostly responsible for:
    16 src/main/groovy/lang/GroovyClassLoader.java
     4 src/main/groovy/ui/GroovyMain.java

Peter Swire is mostly responsible for:
     2 src/main/org/codehaus/groovy/tools/shell/IO.java

Radovan Synek is mostly responsible for:
     1 src/main/org/codehaus/groovy/control/ClassNodeResolver.java

Rahul Somasunderam is mostly responsible for:
     5 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java

René Scheibe is mostly responsible for:
    14 ...vy-nio/src/main/java/org/codehaus/groovy/runtime/NioGroovyMethods.java
     9 subprojects/groovy-json/src/main/java/groovy/json/internal/CharBuf.java
     6 ...s/groovy-servlet/src/main/java/groovy/servlet/AbstractHttpServlet.java
     4 ...ojects/groovy-json/src/main/java/groovy/json/internal/CharScanner.java
     3 subprojects/groovy-json/src/main/java/groovy/json/internal/Sys.java
     2 ...roovy-json/src/main/java/groovy/json/internal/JsonParserCharArray.java
     1 ...groovy-nio/src/main/java/org/codehaus/groovy/runtime/WritablePath.java
     1 ...ojects/groovy-json/src/main/java/groovy/json/internal/NumberValue.java
     1 subprojects/groovy-json/src/main/java/groovy/json/internal/LazyMap.java
     1 ...ects/groovy-json/src/main/java/groovy/json/internal/JsonParserLax.java

Richard Hightower is mostly responsible for:
    15 ...ts/groovy-json/src/main/java/groovy/json/internal/FastStringUtils.java
     5 subprojects/groovy-json/src/main/java/groovy/json/internal/CharBuf.java
     4 ...ts/groovy-json/src/main/java/groovy/json/internal/CharacterSource.java
     3 subprojects/groovy-json/src/main/java/groovy/json/internal/ValueMap.java
     1 ...ojects/groovy-json/src/main/java/groovy/json/internal/SimpleCache.java
     1 ...ects/groovy-json/src/main/java/groovy/json/internal/JsonParserLax.java
     1 ...roovy-json/src/main/java/groovy/json/internal/JsonParserCharArray.java

Sargis Harutyunyan is mostly responsible for:
    25 src/main/groovy/util/GroovyScriptEngine.java
    25 src/main/groovy/util/ConfigObject.java
    14 src/main/org/codehaus/groovy/transform/trait/TraitASTTransformation.java
     8 src/main/org/codehaus/groovy/transform/MemoizedASTTransformation.java
     3 src/main/org/codehaus/groovy/runtime/memoize/Memoize.java

Sergey Egorov is mostly responsible for:
   135 ...in/groovy/org/codehaus/groovy/macro/transform/MacroInvocationTrap.java
    89 src/main/org/codehaus/groovy/ast/MethodCallTransformation.java
    80 ...ro/src/main/groovy/org/codehaus/groovy/macro/runtime/MacroBuilder.java
    77 ...ain/groovy/org/codehaus/groovy/macro/runtime/MacroSubstitutionKey.java
    61 src/main/org/codehaus/groovy/runtime/ResourceGroovyMethods.java
    55 src/main/org/codehaus/groovy/ast/MethodInvocationTrap.java
    30 .../main/groovy/org/codehaus/groovy/macro/runtime/MacroGroovyMethods.java
    17 ...in/groovy/org/codehaus/groovy/macro/transform/MacroTransformation.java
    14 src/main/org/codehaus/groovy/ast/tools/ClosureUtils.java
    12 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingSupport.java

Shil S is mostly responsible for:
    58 ...vy/classgen/asm/sc/StaticTypesBinaryExpressionMultiTypeDispatcher.java
    35 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingVisitor.java
    27 src/main/org/codehaus/groovy/transform/sc/StaticCompilationVisitor.java
     7 src/main/org/codehaus/groovy/tools/javac/JavaStubGenerator.java
     5 src/main/org/codehaus/groovy/classgen/asm/ClosureWriter.java
     4 src/main/groovy/lang/DelegatesTo.java
     3 ...us/groovy/transform/sc/transformers/VariableExpressionTransformer.java
     3 src/main/org/codehaus/groovy/antlr/AntlrParserPlugin.java
     2 ...in/org/codehaus/groovy/transform/sc/StaticCompilationMetadataKeys.java
     2 src/main/org/codehaus/groovy/classgen/asm/sc/StaticInvocationWriter.java

Shil Sinha is mostly responsible for:
    27 src/main/org/codehaus/groovy/classgen/ExtendedVerifier.java
    13 src/main/org/codehaus/groovy/classgen/asm/sc/StaticInvocationWriter.java
     6 ...org/codehaus/groovy/transform/ExternalizeMethodsASTTransformation.java
     3 ...in/org/codehaus/groovy/classgen/asm/sc/StaticTypesStatementWriter.java
     2 src/main/org/codehaus/groovy/transform/stc/StaticTypeCheckingVisitor.java
     2 ...rg/codehaus/groovy/runtime/typehandling/DefaultTypeTransformation.java
     2 src/main/org/codehaus/groovy/classgen/Verifier.java
     1 subprojects/groovy-json/src/main/java/groovy/json/JsonSlurper.java
     1 src/main/org/codehaus/groovy/control/ResolveVisitor.java

Søren Berg Glasius is mostly responsible for:
     3 src/main/org/codehaus/groovy/vmplugin/v5/Java5.java

Thibault Kruse is mostly responsible for:
    53 src/main/groovy/lang/ObjectRange.java
     6 src/main/groovy/lang/IntRange.java
     1 subprojects/groovy-test/src/main/java/groovy/util/GroovyTestCase.java
     1 src/main/org/codehaus/groovy/runtime/InvokerHelper.java
     1 src/main/groovy/time/BaseDuration.java

Tim Yates is mostly responsible for:
     5 src/main/org/codehaus/groovy/runtime/NullObject.java

UEHARA Junji is mostly responsible for:
     4 ...templates/src/main/groovy/groovy/text/markup/MarkupTemplateEngine.java

Wil Selwood is mostly responsible for:
     5 ...cts/groovy-json/src/main/java/groovy/json/internal/BaseJsonParser.java

Yu Kobayashi is mostly responsible for:
   723 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
    85 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethodsSupport.java
    11 src/main/groovy/lang/Tuple.java
    10 src/test/groovy/lang/TupleTest.java
     6 src/main/groovy/util/PermutationGenerator.java

aalmiray is mostly responsible for:
     6 src/main/org/codehaus/groovy/runtime/StringGroovyMethods.java
     4 src/main/groovy/util/FactoryBuilderSupport.java

asa is mostly responsible for:
    10 src/main/org/codehaus/groovy/ast/tools/GeneralUtils.java

belkaram is mostly responsible for:
     8 src/main/org/codehaus/groovy/reflection/stdclasses/CachedSAMClass.java

bpaulin is mostly responsible for:
     1 subprojects/groovy-json/src/main/java/groovy/json/internal/Dates.java

javaboon is mostly responsible for:
   773 subprojects/groovy-json/src/main/java/groovy/json/internal/CharBuf.java
   590 ...ects/groovy-json/src/main/java/groovy/json/internal/JsonParserLax.java
   427 ...ojects/groovy-json/src/main/java/groovy/json/internal/CharScanner.java
   356 ...roovy-json/src/main/java/groovy/json/internal/JsonParserCharArray.java
   305 subprojects/groovy-json/src/main/java/groovy/json/JsonSlurperClassic.java
   276 ...cts/groovy-json/src/main/java/groovy/json/internal/JsonFastParser.java
   267 ...src/main/java/groovy/json/internal/JsonParserUsingCharacterSource.java
   256 .../groovy-json/src/main/java/groovy/json/internal/CharSequenceValue.java
   213 ...ovy-json/src/main/java/groovy/json/internal/ReaderCharacterSource.java
   198 ...cts/groovy-json/src/main/java/groovy/json/internal/BaseJsonParser.java

jfranco is mostly responsible for:
     1 ...aus/groovy/control/customizers/builder/SecureASTCustomizerFactory.java

oreissig is mostly responsible for:
    29 src/main/org/codehaus/groovy/transform/ImmutableASTTransformation.java
    28 src/main/org/codehaus/groovy/runtime/DefaultGroovyMethods.java
     9 ...in/org/codehaus/groovy/transform/IndexedPropertyASTTransformation.java
     9 src/main/org/codehaus/groovy/transform/AutoCloneASTTransformation.java
     6 src/main/org/codehaus/groovy/transform/trait/TraitASTTransformation.java
     6 src/main/org/codehaus/groovy/transform/PackageScopeASTTransformation.java
     6 src/main/org/codehaus/groovy/transform/DelegateASTTransformation.java
     5 ...g/codehaus/groovy/transform/ASTTransformationCollectorCodeVisitor.java
     4 ...ovy-test/src/main/java/groovy/mock/interceptor/MockProxyMetaClass.java
     4 src/main/org/codehaus/groovy/vmplugin/v7/IndyInterface.java

peter is mostly responsible for:
   206 src/main/org/codehaus/groovy/ast/decompiled/DecompiledClassNode.java
   161 src/main/org/codehaus/groovy/ast/decompiled/AsmDecompiler.java
   127 src/main/org/codehaus/groovy/ast/decompiled/MemberSignatureParser.java
   108 src/main/org/codehaus/groovy/ast/decompiled/Annotations.java
   102 src/main/org/codehaus/groovy/ast/decompiled/TypeSignatureParser.java
    94 src/test/org/codehaus/groovy/ast/decompiled/AsmDecompilerTestData.java
    92 src/main/org/codehaus/groovy/ast/decompiled/ClassStub.java
    70 src/main/org/codehaus/groovy/control/ClassNodeResolver.java
    66 src/main/org/codehaus/groovy/ast/decompiled/AsmReferenceResolver.java
    63 src/main/org/codehaus/groovy/ast/decompiled/ClassSignatureParser.java

qxo is mostly responsible for:
     2 ...jects/groovy-servlet/src/main/java/groovy/servlet/TemplateServlet.java

tomasbartalos is mostly responsible for:
     6 src/main/org/codehaus/groovy/util/AbstractConcurrentMapBase.java
     5 src/main/org/codehaus/groovy/util/AbstractConcurrentMap.java
     4 src/main/org/codehaus/groovy/util/AbstractConcurrentDoubleKeyMap.java

The extensions below were found in the repository history (extensions used
during statistical analysis are marked):
htm tex conf ExtensionModule txt xml [java] log ASTTransformation foogroovy ExtensionModuleSpec html policy xhtml yml css bnd gvy adoc [c] [js] Extensions mps placeholder properties groovy md bat g tpl eps gradle rdf Runners xsd ScriptEngineFactory xsl 

```

