```postscript
%!PS-Adobe-2.0
%Infinitely Printable Maze
%FBI FEM-CUT Quine Division
(/code;?;/suffix;?;realtime;srand;/h1;(%!PS-Adobe-2.0)!;/h2;
(%Infinitely;Printable;Maze)!;/h3;(%FBI;FEM-CUT;Quine;;;;;;;
Division)!;/page;[595;842]!;/margin;30;!;/w;30;!;/h;30;!;/t;
true;!;/f;false;!;/&;{and}!;/-;{sub}!;/*;{mul}!;/@;{3;1;;;;;
roll;get;~;get}!;/@@;{4;2;roll;get;3;-2;roll;put}!;/!!;{~;;;
/dict;/begin;4;-1;roll;/exec;/end;6;array;astore;{cvx};map;;
cvx;def}!;/grid;5;{;/v;?;/xs;w;array;!;0;1;w;1;-;{;/x;?;/ys;
h;array;!;0;1;h;1;-;{;/y;?;ys;y;v;put;};for;xs;x;ys;put;};;;
for;xs;}!!;/x0;margin;!;/x1;page;0;get;margin;-;!;/cells;;;;
{x1;x0;-;w;div;*}!;/y0;margin;3.5;cells;+;!;/cell;{cells;y0;
+;~;cells;x0;+;~}!;/y1;y0;h;cells;+;!;/neighbors;2;{;/y;?;;;
/x;?;[[x;1;-;y][x;1;+;y][x;y;1;-][x;y;1;+]];}!!;/shuffle;;;;
{aload;pop;4;rand;roll;4;array;astore}!;/v-walls;t;grid;!;;;
/h-walls;t;grid;!;/erase;4;{;/y1;?;/x1;?;/y0;?;/x0;?;x0;x1;;
eq;{;h-walls;x0;y0;y1;lt;{y1};{y0};ifelse;f;@@;};{;v-walls;;
x0;x1;lt;{x1};{x0};ifelse;y0;f;@@;};ifelse;}!!;/visited;f;;;
grid;!;/frontiers;f;grid;!;/traces;0;grid;!;/trace;0;!;;;;;;
/visit;5;{;/y;?;/x;?;/ns;0;!;visited;x;y;t;@@;frontiers;x;y;
t;@@;x;y;x;y;neighbors;shuffle;{;aload;pop;/ny;?;/nx;?;nx;0;
ge;ny;0;ge;&;nx;w;lt;&;ny;h;lt;&;ns;0;eq;&;{;visited;nx;ny;;
@;not;{;traces;nx;ny;trace;@@;frontiers;nx;ny;t;@@;visited;;
nx;ny;t;@@;/ns;ns;1;+;!;x;y;nx;ny;erase;pop;pop;nx;ny;};if;;
};if;};forall;ns;0;eq;{;frontiers;x;y;f;@@;pop;pop;find;;;;;
visit;};if;}!!;/find;6;{;/rx;rand;!;/ry;rand;!;/fx;-1;!;/fy;
-1;!;0;1;w;1;-;{;/x;~;rx;+;w;mod;!;0;1;h;1;-;{;/y;~;ry;+;h;;
mod;!;frontiers;x;y;@;{;/fx;x;!;/fy;y;!;};if;};for;};for;fx;
fy;}!!;/next;2;{;/y;?;/x;?;frontiers;x;y;@;{x;y};{find};;;;;
ifelse;}!!;/walk;{w;h;*;1;-;{next;visit;/trace;trace;1;+;!};
repeat}!;/x;w;2;idiv;!;/y;0;!;v-walls;x;y;t;@@;v-walls;x;1;;
-;y;t;@@;h-walls;x;y;f;@@;frontiers;x;y;t;@@;x;y;walk;/gray;
{w;h;*;div;.85;*;.85;~;-;setgray};def;/trim;3;{;/in;?;/out;;
in;len;string;!;/i;0;!;in;{;(;);search;{;/pre;?;pre;len;0;;;
gt;{;out;i;pre;$;out;i;pre;len;+;(;);$;/i;i;pre;len;+;1;+;!;
};if;pop;};{;out;i;3;-1;roll;$;out;exit;};ifelse;};loop;}!!;
/header;{trim;show}!;<<;/PageSize;page;>>;setpagedevice;2;;;
setlinewidth;1;setlinecap;/font;{/Courier-Bold;findfont;~;;;
scalefont;setfont}!;24;font;newpath;traces;w;2;idiv;h;1;-;@;
gray;x0;740;moveto;h1;header;x0;720;moveto;h2;header;x0;700;
moveto;h3;header;10;font;/space;<3b>;!;/lpar;<28>;!;/rpar;;;
<29>;!;/wrap;1;{;/in;?;/out;in;len;2;+;string;!;out;0;lpar;;
$;out;1;in;$;out;in;len;1;+;rpar;$;out;}!!;/move;2;{;/y;?;;;
/x;?;x;2;div;.1;+;y;2;div;.1;+;cell;moveto;x;2;idiv;w;lt;y;;
2;idiv;h;lt;&;x;0;ge;&;y;0;ge;&;{;traces;x;2;idiv;y;2;idiv;;
@;gray;};{;0;gray;};ifelse;}!!;/x;0;!;/y;h;2;*;1;-;!;code;;;
wrap;{;(;);search;{;dup;len;/l;?;l;x;+;w;2;*;ge;{;x;1;w;2;*;
1;-;{y;move;space;show};for;/y;y;1;-;!;/x;0;!;};if;0;1;l;1;;
-;{;/i;?;x;i;+;y;move;dup;i;1;getinterval;show;};for;l;0;ne;
{;x;l;+;y;move;space;show;/x;x;l;+;1;+;!;};if;pop;pop;};{;;;
pop;exit;};ifelse;};loop;y;-1;0;{;/y;?;x;1;w;2;*;1;-;{;/x;?;
x;y;move;y;0;eq;x;w;2;*;1;-;eq;&;{rpar};{space};ifelse;show;
};for;/x;0;!;};for;/x;0;!;/y;-2;!;suffix;{wrap;trim};map;{;;
x;y;move;show;/y;y;1;-;!;};forall;x;y;move;(dup;cvx;exec;5;;
array;astore;dup;{cvx;exec};map;quine);trim;show;0;setgray;;
newpath;x0;y1;moveto;w;2;idiv;cells;0;rlineto;1;cells;0;;;;;
rmoveto;x1;y1;lineto;x1;y0;lineto;stroke;/draw;4;{;;;;;;;;;;
/vertical;?;/horizontal;?;/y;?;/x;?;newpath;x;y;cell;moveto;
horizontal;{1;cells;0;rlineto};if;x;y;cell;moveto;vertical;;
{0;1;cells;rlineto};if;stroke;}!!;0;1;w;1;-;{;/x;?;0;1;h;1;;
-;{;/y;?;x;y;h-walls;x;y;@;v-walls;x;y;@;draw;};for;};for;;;
showpage;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;)
(/! {def} def /~ {exch}! /? {~ !}! /+ {add}! /$ {putinterval}! /len {length}!)
(/str {/s ? /i ? /pre ? s i pre $ s i pre len + ( ) $ /i i pre len + 1 + !}!)
(/rep {/t ? /s ? /i 0 ! s {t search {i s str pop} {pop s exit} ifelse} loop}!)
(/quine {pop ~ <3b> rep <0d> rep <0a> rep dup cvx exec}!)
(/map {mark 3 1 roll forall counttomark array astore exch pop} def)
dup cvx exec 5 array astore dup {cvx exec} map quine
```
