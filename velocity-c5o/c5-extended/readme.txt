This is a collection of c/5 orthogonal rakes in Conway's Game of Life 
constructed by Paul Tooke from November to December 2004.  The files
are in RLE format and should be readable by most Life viewing programs.
Each file is named according to the period of the rake it contains.
(e.g. c5-r075.rle contains a period-75 rake)

Detailed explanations of the construction methods are given in the
following two emails by Tooke (edited to remove irrelevant content):

-----------------------------------------------------------------------

From: Paul Tooke
Date: Tue Nov 30, 2004
Subject: c/5 (orthogonal) tech
  	
Recently, I began a search for c/5 orthogonal puffers and high
period spaceships using gfind and my puffer filter program....

The gfind search has rediscovered one known c/5 spaceship and found
tagalongs for it along with some other spaceships which I believe
to be new...

One of these ships can convert a forward glider into an r-pentomino.
This is useful because an r-pentomino can be sparked by spiders to
produce a Herschel amongst other things:

#C c/5 'Fast' Forward glider turner.
#C Minimum repeat time: 85 generations.
x = 87, y = 101, rule = S23/B3
46bo$45bobo$44bo3bo$42b2o2bo2b2o$38b2obo9bob2o$37bo3bobo5bobo
3bo$37bobobobo5bobobobo$38b2obobo2bo2bobob2o$40bo3bo3bo3bo$40b
ob3o3b3obo$43b2o3b2o$43bobobobo$43bobobobo$42b2obobob2o$41bob
obobobobo$40b2obobobobob2o$39bo3bobobobo3bo$40b2obobobobob2o$
44bo3bo2$43bo5bo$39bob2obo3bob2obo$38bobobo2bobo2bobobo$43bob
obobo$38bo3b2obobob2o3bo$39bo2bob2ob2obo2bo$40bo2bobobobo2bo$
39bo5bobo5bo2$40bo3bo3bo3bo$41bo2bo3bo2bo$42b9o$42bobobobobo$
43b2o3b2o$43b2o3b2o2$40b3o7b3o$42bo7bo$39bo3bo5bo3bo$39bo4bo3b
o4bo$39bo13bo$39b5o5b5o4$43b3o$43bo$44bo$9b2o5b2o$b4obobobo5b
obobob4o$3obobob2obo3bob2obobob3o$o3bobo13bobo3bo$bob3o5b2ob2o
5b3obo$b2o21b2o$b5o15b5o$4b2o15b2o29$62bo5b2o5b2o5bo$60bo2b2o
b2o2bo3bo2b2ob2o2bo$58b3o4bobo3bobo3bobo4b3o$58b2o2bo2b3ob2o3b
2ob3o2bo2b2o$58b3o2b3o4bo3bo4b3o2b3o$59bobo2bo15bo2bobo$11b2o
5b2o40bo23bo$3b4obobobo5bobobob4o$2b3obobob2obo3bob2obobob3o$
2bo3bobo13bobo3bo26b2o5b2o$3bob3o5b2ob2o5b3obo19b4obobobo5bob
obob4o$3b2o21b2o18b3obobob2obo3bob2obobob3o$3b5o15b5o18bo3bob
o13bobo3bo$6b2o15b2o22bob3o5b2ob2o5b3obo$47b2o21b2o$47b5o15b5o
$50b2o15b2o$!

#C c/5 Herschel based forward glider turner
#C Minimum repeat time: 50 generations
x = 87, y = 106, rule = S23/B3
63bo$62bobo$61bo3bo$59b2o2bo2b2o$55b2obo9bob2o$54bo3bobo5bobo
3bo$54bobobobo5bobobobo$55b2obobo2bo2bobob2o$57bo3bo3bo3bo$57b
ob3o3b3obo$60b2o3b2o$60bobobobo$60bobobobo$59b2obobob2o$58bob
obobobobo$57b2obobobobob2o$56bo3bobobobo3bo$57b2obobobobob2o$
61bo3bo2$60bo5bo$56bob2obo3bob2obo$55bobobo2bobo2bobobo$60bob
obobo$55bo3b2obobob2o3bo$56bo2bob2ob2obo2bo$57bo2bobobobo2bo$
56bo5bobo5bo2$57bo3bo3bo3bo$58bo2bo3bo2bo$59b9o$59bobobobobo$
60b2o3b2o$60b2o3b2o2$57b3o7b3o$59bo7bo$56bo3bo5bo3bo$56bo4bo3b
o4bo$56bo13bo$56b5o5b5o4$60b3o$60bo$61bo2$12bo5b2o5b2o5bo$10b
o2b2ob2o2bo3bo2b2ob2o2bo$8b3o4bobo3bobo3bobo4b3o$8b2o2bo2b3ob
2o3b2ob3o2bo2b2o$8b3o2b3o4bo3bo4b3o2b3o$9bobo2bo15bo2bobo33bo
7bo$10bo23bo28b2obobob2o3b2obobob2o$60b3obob3o9b3obob3o$60bo3b
obo5bobo5bobo3bo$64b2o6bobo6b2o$61b2o9bobo9b2o$61b2ob2o15b2ob
2o$4b2o5b2o5b2o5b2o38bo15bo$2bo3bo3bo2bo3bo2bo3bo3bo$2bo3bobo
b3o5b3obobo3bo$2bo5b2o2b3ob3o2b2o5bo28bo5b2o5b2o5bo$2b2ob3o15b
3ob2o26bo2b2ob2o2bo3bo2b2ob2o2bo$2bo25bo24b3o4bobo3bobo3bobo4b
3o$3bo3bo15bo3bo25b2o2bo2b3ob2o3b2ob3o2bo2b2o$4bo2bo15bo2bo26b
3o2b3o4bo3bo4b3o2b3o$54bobo2bo15bo2bobo$55bo23bo28$9bo7bo$3b2o
bobob2o3b2obobob2o$3obob3o9b3obob3o$o3bobo5bobo5bobo3bo$4b2o6b
obo6b2o$b2o9bobo9b2o$b2ob2o15b2ob2o$5bo15bo$!

#C A c/5 Herschel-based forward glider duplicator which outputs one
#C forward glider to either side.
#C Herschel -> double glider reaction by David Bell.
#C Minimum repeat time: 60 generations
x = 91, y = 144, rule = S23/B3
67bo$66bobo$65bo3bo$63b2o2bo2b2o$59b2obo9bob2o$58bo3bobo5bobo
3bo$58bobobobo5bobobobo$59b2obobo2bo2bobob2o$61bo3bo3bo3bo$61b
ob3o3b3obo$64b2o3b2o$64bobobobo$64bobobobo$63b2obobob2o$62bob
obobobobo$61b2obobobobob2o$60bo3bobobobo3bo$61b2obobobobob2o$
65bo3bo2$64bo5bo$60bob2obo3bob2obo$59bobobo2bobo2bobobo$64bob
obobo$59bo3b2obobob2o3bo$60bo2bob2ob2obo2bo$61bo2bobobobo2bo$
60bo5bobo5bo2$61bo3bo3bo3bo$62bo2bo3bo2bo$63b9o$63bobobobobo$
64b2o3b2o$64b2o3b2o2$61b3o7b3o$63bo7bo$60bo3bo5bo3bo$60bo4bo3b
o4bo$60bo13bo$60b5o5b5o4$64b3o$64bo$65bo2$16bo5b2o5b2o5bo$14b
o2b2ob2o2bo3bo2b2ob2o2bo$12b3o4bobo3bobo3bobo4b3o$12b2o2bo2b3o
b2o3b2ob3o2bo2b2o$12b3o2b3o4bo3bo4b3o2b3o$13bobo2bo15bo2bobo33b
o7bo$14bo23bo28b2obobob2o3b2obobob2o$64b3obob3o9b3obob3o$64bo
3bobo5bobo5bobo3bo$68b2o6bobo6b2o$65b2o9bobo9b2o$65b2ob2o15b2o
b2o$8b2o5b2o5b2o5b2o38bo15bo$6bo3bo3bo2bo3bo2bo3bo3bo$6bo3bob
ob3o5b3obobo3bo$6bo5b2o2b3ob3o2b2o5bo28bo5b2o5b2o5bo$6b2ob3o15b
3ob2o26bo2b2ob2o2bo3bo2b2ob2o2bo$6bo25bo24b3o4bobo3bobo3bobo4b
3o$7bo3bo15bo3bo25b2o2bo2b3ob2o3b2ob3o2bo2b2o$8bo2bo15bo2bo26b
3o2b3o4bo3bo4b3o2b3o$58bobo2bo15bo2bobo$59bo23bo35$6bo3b3o5b3o
3bo$3b2ob5ob2o3b2ob5ob2o$bob2obo5bobobobo5bob2obo28b2o5b2o$o3b
obo3b5ob5o3bobo3bo19b4obobobo5bobobob4o$4b3o5b2o3b2o5b3o22b3o
bobob2obo3bob2obobob3o$bo2bob3o13b3obo2bo19bo3bobo13bobo3bo$3b
o23bo22bob3o5b2ob2o5b3obo$50b2o21b2o$50b5o15b5o$53b2o15b2o7$55b
2o5b2o$47b4obobobo5bobobob4o$46b3obobob2obo3bob2obobob3o$46bo
3bobo13bobo3bo$47bob3o5b2ob2o5b3obo$47b2o21b2o$47b5o15b5o$50b
2o15b2o8$6b2o5b2o5b2o5b2o$4bo3bo3bo2bo3bo2bo3bo3bo$4bo3bobob3o
5b3obobo3bo$4bo5b2o2b3ob3o2b2o5bo$4b2ob3o15b3ob2o$4bo25bo$5bo
3bo15bo3bo$6bo2bo15bo2bo$!

A forwards -> backwards glider turner isn't of much use right now,
but uses for backwards gliders may be found some day:

#C c/5 Forwards -> backwards glider turner
x = 87, y = 71, rule = S23/B3
63bo$62bobo$61bo3bo$59b2o2bo2b2o$55b2obo9bob2o$54bo3bobo5bobo
3bo$54bobobobo5bobobobo$55b2obobo2bo2bobob2o$57bo3bo3bo3bo$57b
ob3o3b3obo$60b2o3b2o$60bobobobo$60bobobobo$59b2obobob2o$58bob
obobobobo$57b2obobobobob2o$56bo3bobobobo3bo$57b2obobobobob2o$
61bo3bo2$60bo5bo$56bob2obo3bob2obo$55bobobo2bobo2bobobo$60bob
obobo$55bo3b2obobob2o3bo$56bo2bob2ob2obo2bo$57bo2bobobobo2bo$
56bo5bobo5bo2$57bo3bo3bo3bo$58bo2bo3bo2bo$59b9o$59bobobobobo$
60b2o3b2o$60b2o3b2o2$57b3o7b3o$59bo7bo$56bo3bo5bo3bo$56bo4bo3b
o4bo$56bo13bo$56b5o5b5o4$60b3o$60bo$61bo6$4bo5b2o5b2o5bo$2bo2b
2ob2o2bo3bo2b2ob2o2bo42bo7bo$3o4bobo3bobo3bobo4b3o34b2obobob2o
3b2obobob2o$2o2bo2b3ob2o3b2ob3o2bo2b2o31b3obob3o9b3obob3o$3o2b
3o4bo3bo4b3o2b3o31bo3bobo5bobo5bobo3bo$bobo2bo15bo2bobo36b2o6b
obo6b2o$2bo23bo34b2o9bobo9b2o$61b2ob2o15b2ob2o$65bo15bo3$57bo
5b2o5b2o5bo$55bo2b2ob2o2bo3bo2b2ob2o2bo$53b3o4bobo3bobo3bobo4b
3o$53b2o2bo2b3ob2o3b2ob3o2bo2b2o$53b3o2b3o4bo3bo4b3o2b3o$54bo
bo2bo15bo2bobo$55bo23bo$!

In August 1999, David Bell posted a Herschel track built from c/5
ships and suggested that it may be possible to construct a complete
track to obtain rakes or spaceships of any sufficiently high period.
Using one of the reflectors or the duplicator shown above it is now
possible to achieve the same result by using a length of Herschel
track and a single glider reflection or duplication.

The front half of the Herschel-based reflector converts a forward
glider to a Herschel which can be translated downwards using c/5
Herschel track pieces shown below. The Herschel can then converted
into a forward glider which can be reflected or duplicated to
complete the loop. Of course, if the Herschel-based
reflector/duplicator is used then track pieces could also be
inserted within it. The period of the resulting rake or spaceship
can be reduced by placing gliders or Herschels at equal time
intervals around the loop.

What follows is a rough proof that spaceships and rakes of period 190
or higher can be built using this method.

Firstly, here are the track pieces:

Here is what I'll call a "type-A" track piece which translates a
Herschel downstream by 62 cells in 288 generations. It also leaves
a block which must be deleted by a following track piece. This c/5
convoy is essentially the one posted by David Bell. I have simply
added two spiders to delete the output gliders.
Minimum repeat time: 150 generations

x = 133, y = 114, rule = S23/B3
70b2o5b2o$62b4obobobo5bobobob4o$61b3obobob2obo3bob2obobob3o$53b
3o5bo3bobo13bobo3bo$55bo6bob3o5b2ob2o5b3obo$54b3o5b2o21b2o$22b
o5b2o5b2o5bo19b5o15b5o$20bo2b2ob2o2bo3bo2b2ob2o2bo20b2o15b2o$
18b3o4bobo3bobo3bobo4b3o$18b2o2bo2b3ob2o3b2ob3o2bo2b2o$18b3o2b
3o4bo3bo4b3o2b3o$19bobo2bo15bo2bobo$20bo23bo6$33b2o$33bobobob
4o$32bob2obobob3o$6bo3b3o5b3o3bo12bobo3bo$3b2ob5ob2o3b2ob5ob2o
3b2o5b3obo$bob2obo5bobobobo5bob2obo11b2o$o3bobo3b5ob5o3bobo11b
5o$4b3o5b2o3b2o5b3o11b2o$bo2bob3o13b3obo2bo$3bo23bo3$89bo7bo$
83b2obobob2o3b2obobob2o$80b3obob3o9b3obob3o$80bo3bobo5bobo5bo
bo3bo$84b2o6bobo6b2o$81b2o9bobo9b2o$28bo5b2o5b2o5bo32b2ob2o15b
2ob2o$26bo2b2ob2o2bo3bo2b2ob2o2bo34bo15bo$24b3o4bobo3bobo3bob
o4b3o$24b2o2bo2b3ob2o3b2ob3o2bo2b2o$24b3o2b3o4bo3bo4b3o2b3o$25b
obo2bo15bo2bobo$26bo23bo3$47b2o5b2o$39b4obobobo5bobobob4o32bo
7bo$38b3obobob2obo3bob2obobob3o25b2obobob2o3b2obobob2o$38bo3b
obo13bobo3bo22b3obob3o9b3obob3o$39bob3o5b2ob2o5b3obo23bo3bobo
5bobo5bobo3bo$39b2o21b2o27b2o6bobo6b2o$39b5o15b5o24b2o9bobo9b
2o$42b2o15b2o27b2ob2o15b2ob2o$92bo15bo7$49b2o5b2o5b2o5b2o$47b
o3bo3bo2bo3bo2bo3bo3bo$47bo3bobob3o5b3obobo3bo$47bo5b2o2b3ob3o
2b2o5bo$47b2ob3o15b3ob2o$47bo25bo$48bo3bo15bo3bo20bo3b3o5b3o3b
o$49bo2bo15bo2bo18b2ob5ob2o3b2ob5ob2o$88bob2obo5bobobobo5bob2o
bo$87bo3bobo3b5ob5o3bobo3bo$91b3o5b2o3b2o5b3o$88bo2bob3o13b3o
bo2bo$90bo23bo6$93b2o5b2o$91bo3bo3bo2bo$91bo3bobob3o13bo7bo$91b
o5b2o2b3o5b2obobob2o3b2obobob2o$91b2ob3o9b3obob3o9b3obob3o$91b
o14bo3bobo5bobo5bobo3bo$92bo3bo13b2o6bobo6b2o$93bo2bo10b2o9bo
bo9b2o$107b2ob2o15b2ob2o$111bo15bo3$37b2o5b2o$29b4obobobo5bob
obob4o$28b3obobob2obo3bob2obobob3o$28bo3bobo13bobo3bo$29bob3o
5b2ob2o5b3obo$29b2o21b2o$29b5o15b5o33bo3b3o5b3o3bo$32b2o15b2o
33b2ob5ob2o3b2ob5ob2o$82bob2obo5bobobobo5bob2obo$81bo3bobo3b5o
b5o3bobo3bo$85b3o5b2o3b2o5b3o$82bo2bob3o13b3obo2bo$84bo23bo3$
72b2o5b2o5b2o5b2o$30b2o5b2o31bo3bo3bo2bo3bo2bo3bo3bo$22b4obob
obo5bobobob4o23bo3bobob3o5b3obobo3bo$21b3obobob2obo3bob2obobo
b3o22bo5b2o2b3ob3o2b2o5bo$21bo3bobo13bobo3bo22b2ob3o15b3ob2o$
22bob3o5b2ob2o5b3obo23bo25bo$22b2o21b2o24bo3bo15bo3bo$22b5o15b
5o25bo2bo15bo2bo$25b2o15b2o$!


Here is what I'll call a "type-B" track piece which translates a
Herschel downstream by 33 cells and laterally by 13 cells in 177
generations. Minimum repeat time: 50 generations.

x = 86, y = 50, rule = S23/B3
63b2o5b2o$55b4obobobo5bobobob4o$54b3obobob2obo3bob2obobob3o$46b
3o5bo3bobo13bobo3bo$48bo6bob3o5b2ob2o5b3obo$47b3o5b2o21b2o$55b
5o15b5o$58b2o15b2o11$12b2o5b2o5b2o5b2o$10bo3bo3bo2bo3bo2bo3bo
3bo$10bo3bobob3o5b3obobo3bo$10bo5b2o2b3ob3o2b2o5bo$10b2ob3o15b
3ob2o$10bo25bo$11bo3bo15bo3bo$12bo2bo15bo2bo3$12bo3b3o5b3o3bo
$9b2ob5ob2o3b2ob5ob2o$7bob2obo5bobobobo5bob2obo$6bo3bobo3b5ob
5o3bobo3bo$10b3o5b2o3b2o5b3o$7bo2bob3o13b3obo2bo32b2o5b2o$9bo
23bo26b4obobobo5bobobob4o$59b3obobob2obo3bob2obobob3o$59bo3bo
bo13bobo3bo$60bob3o5b2ob2o5b3obo$60b2o21b2o$60b5o15b5o$4bo5b2o
5b2o5bo38b2o15b2o$2bo2b2ob2o2bo3bo2b2ob2o2bo$3o4bobo3bobo3bob
o4b3o$2o2bo2b3ob2o3b2ob3o2bo2b2o28bo3b3o5b3o3bo$3o2b3o4bo3bo4b
3o2b3o25b2ob5ob2o3b2ob5ob2o$bobo2bo15bo2bobo24bob2obo5bobobob
o5bob2obo$2bo23bo24bo3bobo3b5ob5o3bobo3bo$55b3o5b2o3b2o5b3o$52b
o2bob3o13b3obo2bo$54bo23bo$!

Here is another track piece which translates a Herschel downstream
by 32 cells and laterally by 31 cells in 240 generations.
Minimum repeat time: 85 generations.

x = 86, y = 61, rule = S23/B3
34b2o5b2o5b2o5b2o$32bo3bo3bo2bo3bo2bo3bo3bo$32bo3bobob3o5b3ob
obo3bo4b3o$32bo5b2o2b3ob3o2b2o5bo6bo$32b2ob3o15b3ob2o5b3o$32b
o25bo$33bo3bo15bo3bo$34bo2bo15bo2bo7$34bo7bo$28b2obobob2o3b2o
bobob2o$25b3obob3o9b3obob3o$25bo3bobo5bobo5bobo3bo$29b2o6bobo
6b2o$26b2o9bobo9b2o$26b2ob2o15b2ob2o$30bo15bo17$16b2o5b2o$8b4o
bobobo5bobobob4o$7b3obobob2obo3bob2obobob3o$7bo3bobo13bobo3bo
$8bob3o5b2ob2o5b3obo$8b2o21b2o$8b5o15b5o28bo5b2o5b2o5bo$11b2o
15b2o29bo2b2ob2o2bo3bo2b2ob2o2bo$57b3o4bobo3bobo3bobo4b3o$57b
2o2bo2b3ob2o3b2ob3o2bo2b2o$57b3o2b3o4bo3bo4b3o2b3o$58bobo2bo15b
o2bobo$9bo7bo41bo23bo$3b2obobob2o3b2obobob2o$3obob3o9b3obob3o
$o3bobo5bobo5bobo3bo34b2o5b2o$4b2o6bobo6b2o30b4obobobo5bobobo
b4o$b2o9bobo9b2o26b3obobob2obo3bob2obobob3o$b2ob2o15b2ob2o26b
o3bobo13bobo3bo$5bo15bo31bob3o5b2ob2o5b3obo$53b2o21b2o$53b5o15b
5o$56b2o15b2o$!

Here are two track terminating pieces which convert a Herschel into
a forwards glider with variants for deleting the block that may have
been left behind by a type-A track piece. The right-hand convoy
produces a second glider and would be used in a rake where none of
the other components can produce extra gliders. The timings of the
'loop' output glider is the same for these two reactions.
Minimum repeat time: 50 & 60 generations respectively.

x = 162, y = 158, rule = S23/B3
121b3o$123bo$122b3o$41b3o$43bo$42b3o4$10bo5b2o5b2o5bo$8bo2b2o
b2o2bo3bo2b2ob2o2bo$6b3o4bobo3bobo3bobo4b3o$6b2o2bo2b3ob2o3b2o
b3o2bo2b2o52b2o5b2o5b2o5b2o$6b3o2b3o4bo3bo4b3o2b3o50bo3bo3bo2b
o3bo2bo3bo3bo$7bobo2bo15bo2bobo51bo3bobob3o5b3obobo3bo$8bo23b
o52bo5b2o2b3ob3o2b2o5bo24bo3b3o5b3o3bo$85b2ob3o15b3ob2o21b2ob
5ob2o3b2ob5ob2o$85bo25bo19bob2obo5bobobobo5bob2obo$86bo3bo15b
o3bo19bo3bobo3b5ob5o3bobo3bo$87bo2bo15bo2bo24b3o5b2o3b2o5b3o$
131bo2bob3o13b3obo2bo$133bo23bo8$133bo3b3o5b3o3bo$130b2ob5ob2o
3b2ob5ob2o$128bob2obo5bobobobo5bob2obo$127bo3bobo3b5ob5o3bobo
3bo$131b3o5b2o3b2o5b3o$128bo2bob3o13b3obo2bo$130bo23bo8$96bo7b
o$90b2obobob2o3b2obobob2o$87b3obob3o9b3obob3o$87bo3bobo5bobo5b
obo3bo$91b2o6bobo6b2o$88b2o9bobo9b2o$88b2ob2o15b2ob2o$92bo15b
o45$37b2o$37b2o85b2o$124b2o9$35b3o$37bo84b3o$36b3o85bo$123b3o
3$4bo5b2o5b2o5bo$2bo2b2ob2o2bo3bo2b2ob2o2bo$3o4bobo3bobo3bobo
4b3o$2o2bo2b3ob2o3b2ob3o2bo2b2o$3o2b3o4bo3bo4b3o2b3o$bobo2bo15b
o2bobo$2bo23bo$88b2o5b2o5b2o5b2o$86bo3bo3bo2bo3bo2bo3bo3bo$86b
o3bobob3o5b3obobo3bo$11bo3b3o5b3o3bo56bo5b2o2b3ob3o2b2o5bo24b
o3b3o5b3o3bo$8b2ob5ob2o3b2ob5ob2o53b2ob3o15b3ob2o21b2ob5ob2o3b
2ob5ob2o$6bob2obo5bobobobo5bob2obo51bo25bo19bob2obo5bobobobo5b
ob2obo$5bo3bobo3b5ob5o3bobo3bo51bo3bo15bo3bo19bo3bobo3b5ob5o3b
obo3bo$9b3o5b2o3b2o5b3o56bo2bo15bo2bo24b3o5b2o3b2o5b3o$6bo2bo
b3o13b3obo2bo97bo2bob3o13b3obo2bo$8bo23bo101bo23bo8$134bo3b3o
5b3o3bo$131b2ob5ob2o3b2ob5ob2o$129bob2obo5bobobobo5bob2obo$128b
o3bobo3b5ob5o3bobo3bo$132b3o5b2o3b2o5b3o$129bo2bob3o13b3obo2b
o$131bo23bo4$133bo3b3o5b3o3bo$130b2ob5ob2o3b2ob5ob2o$128bob2o
bo5bobobobo5bob2obo$127bo3bobo3b5ob5o3bobo3bo$97bo7bo25b3o5b2o
3b2o5b3o$91b2obobob2o3b2obobob2o16bo2bob3o13b3obo2bo$88b3obob
3o9b3obob3o15bo23bo$88bo3bobo5bobo5bobo3bo$92b2o6bobo6b2o$89b
2o9bobo9b2o$89b2ob2o15b2ob2o$93bo15bo$!

The constraints on the possible periods are: the achievable loop
lengths, the minimum repeat times of the components and the need to
avoid collisions between the glider streams. I'll deal with each in
turn.

Achievable loop lengths
~~~~~~~~~~~~~~~~~~~~~~~
By 'loop length' I mean the total number of generations it takes
for a single glider to traverse the entire loop. This must be
equal to the product of the desired rake/spaceship period and the
number of gliders/Herschels in the loop.

It is possible to achieve any desired period even if we just use
the type-A and type-B track pieces and the 'fast' glider reflector.
In this case, colour square constraints force the use of an odd
number of type-B pieces and if we denote the number of type-A pieces
by A, and that of type-B pieces by 2B+1, then the total
time taken to complete the loop is 3280 + 2680A + 3090B. If we
want a rake or spaceship of period 5P using G gliders/herschels in
the loop then the loop length must be 5PG and we must find
non-negative integers A,B & G such that PG = 2(328 + 268A + 309B).
This is possible for any P since (268,309) = 1. In fact if we
change variables by A = aP+8 and B = bP-8, the equation above
reduces to G = 536a + 618b and we can always chose a & b to make
A, B & G non-negative. In practice, it will normally be possible to
find smaller numbers that work.

Repeat time constraints
~~~~~~~~~~~~~~~~~~~~~~~
I have labelled each of the components above with a 'minimum repeat
time', by which I mean: the component can operate at this or any
higher period. The highest of these values is 150 generations for
the type-A track piece. It transpires that this is less than the
minimum period that can be achieved with this design anyway (see
below), and so presents no additional constraint on the possible
periods.

Glider stream collision constraints
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The biggest constraint on possible rake/spaceship periods in this
design is presented by the potential for the two forward glider
streams to interact at their intersection.

The glider streams into and out of the 'fast' glider reflector
intersect at period 540 +/- 90, i.e a glider leaving the reflector
will collide with any glider following between 450 and 630
generations (inclusive) behind it. This rules out these periods and
any which divide into a value in this range, leaving periods 215-220,
320-445 & 635 or higher. Using a Herschel track reflector changes
the point at which they intersect, allowing the missing periods
from 190 to 630 to be constructed. The +/-90 generation collision
range is a feature of intersecting forward glider streams within c/5
convoys. No rake or spaceship of period 185 or lower can contain such
an intersection, since forward glider streams of these periods cannot
cross without interacting.

With robot assistance, I have constructed examples of c/5 rakes of
every period from p190 to p1000. I don't expect many of these to be
optimal, particularly those periods divisible by 30, where p30-based
technology would help.

--
Paul Tooke

-----------------------------------------------------------------------

From: Paul Tooke
Date: Fri Dec 10, 2004
Subject: c/5 (orthogonal) tech, Part 2
  	
Recently, I restarted a symmetrical width 20 c/5 search with gfind
in an attempt to find a spaceship with a domino spark at the rear.
David Bell pointed out in December 2000 that such a spaceship could
turn a forward glider into a block and a reflected forward glider,
enabling a simple forward glider reflector to be built. This would
be useful in producing simple engineless rakes or spaceships.

Here are the new spaceships that the search has found so far:

...

One of these ships has the domino spark and can turn forward gliders
at period 165 or higher, reducing the minimum possible period for
engineless c/5 rakes or spaceships. An unexpected bonus is that it
also has additional sparks nearby which can turn a forward LWSS or
MWSS into a forward glider. These reactions can repeat as fast as
the xWSS can arrive (25 and 30 generations repectively.)

x = 41, y = 154, rule = S23/B3
25b3o6b3o$22b4obo6bob4o$21bo18bo$21bo2bob2o6b2obo2bo$28bob2ob
o$21b3o5bo2bo5b3o$23bo2bo3b2o3bo2bo$22bo6bo2bo6bo$23bo3bo6bo3b
o$26b3o4b3o$27bo6bo$22b3o2bobo2bobo2b3o$25b2o8b2o$26b2o6b2o$25b
obobo2bobobo$22b2o14b2o$24bo12bo$24b2o10b2o$24b2o10b2o$23b2o12b
2o$22b2o2bo8bo2b2o$25b2o8b2o$25bo4b2o4bo$24b2o4b2o4b2o$24bobo
2bo2bo2bobo$24bob2ob4ob2obo$26bob6obo$24bob3o4b3obo$24b3o8b3o
$22b2o14b2o$22b2o14b2o$26bo8bo$25b3o6b3o$24bo12bo$23b2obo8bob
2o$24bobob2o2b2obobo$26bo2bo2bo2bo$25b2ob2o2b2ob2o$26bob2o2b2o
bo$25bo2bo4bo2bo$24b2o10b2o$24bo12bo$25b2o8b2o$24b2o10b2o$23b
o2bo8bo2bo$22b5o8b5o$23bo2bo8bo2bo$25bobo6bobo$22bo2bo2bo4bo2b
o2bo$25b3obo2bob3o$29b4o$28b6o$27bob4obo$27b3o2b3o$25b3ob4ob3o
2$25b2o8b2o$23b2o12b2o$24bo12bo2$23b2ob2o6b2ob2o$22bo3bobo4bo
bo3bo$23b5o6b5o2$23b3obo6bob3o$26b2o6b2o$27bo6bo$28b2o2b2o$28b
2o2b2o$29b4o$25b2ob6ob2o$25bo2b2o2b2o2bo$23b2o3bo4bo3b2o$22bo
5bo4bo5bo$22bo16bo$23bo14bo$24bo2bo6bo2bo$25b2o3b2o3b2o$25b2o
3b2o3b2o$25bo4b2o4bo$26bobob2obobo$25b2o2b4o2b2o$25bo10bo$26b
o2bo2bo2bo$26bobo4bobo$27bobo2bobo$28bo4bo$27bobo2bobo$27bob4o
bo$27bo2b2o2bo$27bob4obo$26bo8bo2$27bo6bo$28bo4bo$30b2o2$31b3o
$31bo$32bo$9b2o5b2o$b4obobobo5bobobob4o$3obobob2obo3bob2obobo
b3o$o3bobo13bobo3bo$bob3o5b2ob2o5b3obo$b2o21b2o$b5o15b5o$4b2o
15b2o8$34b3o$34bo2bo$34bo$34bo$35bobo3$35bo$34b3o$34bob2o$35b
3o$35b2o13$34b3o$34bo2bo$34bo$34bo3bo$34bo$35bobo4$34b3o$33bo
2bo$36bo$32bo3bo$36bo$33bobo$!

Forward LWSS streams can be created from 3 gliders within a c/5
convoy at period 40 and higher, and a forward glider stream can
cross a forward LWSS stream at period 60 or higher. Given suitable
glider duplicators and turners it is therefore possible to build
engineless c/5 rakes and spaceships of quite low period. Below
period 85, only one of the Herschel/r-Pentomino-based reflectors
that I know of works, but it is possible to build rakes of period 60
or higher using just this. I've added examples of rakes from period
60 to period 80 to my archive of c5 rakes

--
Paul Tooke
