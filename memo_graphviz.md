
# Memo graphviz

à consulter : [GraphViz Pocket Reference](https://graphs.grevian.org/example)
et [attributs graphviz](http://www.graphviz.org/doc/info/attrs.html)
```graphviz
digraph simple_example {
   step_1 -> step_2;
   step_1 -> step_3;
   step_2 -> step_3;}

```
 #### Arborescence des fichiers

```graphviz
digraph hierarchy {
  nodesep=1 // Increases the separation between nodes

  node [color=Grey,fontname=Optima,shape=box] // All nodes will this shape and colour
  edge [color=Lightblue] // All the lines look like this

  Test->{rep1 rep2 rep3};
  rep1->"fichier1.txt";
 
  rep2->rep5;
  rep3->{rep6 rep7};
   rep7->"fichier1.txt ";
  {rank=same;  } // Put them on the same level
}
```
```graphviz

digraph structs {
  node [shape=record];
  struct1 [shape=record,label="<f0> left|<f1> middle|<f2> right"];
  struct2 [shape=record,label="<f0> one|<f1> two"];
  struct3 [shape=record,label="hello\nworld |{ b |{c|<here> d|e}| f}| g | h"];
  struct1:f1 -> struct2:f0;
  struct1:f2 -> struct3:here;
  ##struct1 -> struct2;
  ##struct1 -> struct3;
}
```
```graphviz

digraph clusters {
  subgraph cluster0 {
    node [style=filled,color=white];
    style=filled;
    color=lightgrey;
    a0 -> a1 -> a2 -> a3;
    label = "process #1";
  }

  subgraph cluster1 {
    node [style=filled];
    b0 -> b1 -> b2 -> b3;
    label = "process #2";
    color=blue
  }

  start -> a0;
  start -> b0;
  a1 -> b3;
  b2 -> a3;
  a3 -> a0;
  a3 -> end;
  b3 -> end;
  start [shape=Mdiamond];
  end [shape=Msquare];
}
```
```graphviz
digraph git{
  subgraph master {
    m1 -> m2 -> m3 -> m4 -> m5;
    m1 -> m5;
  }
  subgraph branch {
    m2 -> b1; // branch from master
    b1 -> b2 -> b3;
    b3 -> m4; // merge into master
    b3 -> b1;
  }
  {rankdir=LR; rank=same; m1;m2;m3;m4;m5;}
  {rankdir=LR; rank=same; b1;b2;b3;}
}
```
```graphviz
digraph game {
  label = "Game history";
  labelloc = t;
  rankdir = LR;

  node[shape = plaintext];
  1995 -> 1996 -> 1997 -> 1998 -> 1999 -> 2000 -> 2001;

  node[shape = box, style = filled];
  WAR3 -> Xhero -> Footman -> DOTA;
  WAR3 -> Battleship;

  {rank = same; 1996; WAR3;}
  {rank = same; 1998; Xhero; Battleship;}
  {rank = same; 1999; Footman;}
  {rank = same; 2001; DOTA;}
}

```
```graphviz
digraph G {
  label = "Dot demo";  // graph name
  labelloc = t;  // name location, b for bottom, t for top
  labeljust = l;  // name location, l for left, r for right
  main -> parse -> execute;
  main -> init;
  main -> cleanup;
  execute -> make_string;
  execute -> printf
  init -> make_string;
  main -> printf;
  execute -> compare;
}
```
