! "main" (cells 1462 length 118 width 370 generation 0)
! Sawtooth with expansion factor 25
! Population is unbounded but does not tend to infinity.  Its graph
! is a sawtooth function with ever-increasing teeth.  More
! specifically, the population in generations  t  near  30 * 25^n  is
! about  59t/225  if  t  is odd, about  7t/10  if  t  is even but not
! == 46 (mod 60),  and about  211t/900  if  t == 46 (mod 60);  the
! population in generation  6 * 25^n - 1125  (n>=2)  is only 1846.
! (Even more specifically, the population in generation
! t = 30 * 25^n - 525  (n>=1), is  59t/225 + 1951.)
!
! A shotgun produces a salvo of 4 eastward lightweight spaceships
! every 120 generations.  Some are deleted; the others eventually
! catch up to a pair of c/3 spaceships and reflect off the backs of
! them, forming westward middleweight spaceships.  When a MWSS
! returns to the shotgun, it causes the deletion of 5 salvos.  So the
! region between the shotgun and the c/3s alternately becomes full
! and empty of spaceships.
!
! Specifically, for  N>=3,  salvo N is created in gen  120N-305.
! (Salvos 1 and 2 are already fully formed in the initial pattern.
! Salvo 0 doesn't exist, but its effect is simulated by the
! nonexistence of 2 gliders.)  If not deleted, salvo N hits the c/3s
! in gen  360N-71,  creating a MWSS 111 gens later.  This MWSS
! returns to the shotgun and deletes 2 gliders, in gens  600N+85
! and  600N+155,  causing the deletion of salvos  5N+5  through
! 5N+9.  Thus, 5 salvos (numbered 0 to 4) delete 5^2 salvos (5 to
! 29), allowing 5^3 salvos (30 to 154) to escape, deleting 5^4
! salvos (155 to 779), ...
!
! The c/3 spaceships were found by David Bell, who suggested this
! way of making a sawtooth.
!
! Dean Hickerson, drhickerson@ucdavis.edu  8/26/92
59k184h@!
117.................OO
117.................O
117..............OO...............O
117.O...........OOO...............O.O
115.O.O12.OO18.OO50.OO
106.O7.O.O16.O16.OO5.O45.O
105.OO6.O..O16.OO15.OO4.OO31.O15.OO60.O40.O
94.O9.OO4.O3.O.O30.O.O37.O.O15.3O11.O46.O.O38.O.O
49.O44.OO7.3O4.OO3.O.O29.O37.OO18.OO12.O.O34.OO7.O.OO36.OO3.O14.OO
49.O.O52.OO11.O15.OO44.O5.OO16.O16.O.O7.O24.O.O5.O.O.OO10.OO19.OO3.OO3.O13.O.O
52.OO6.OO43.OO27.O44.OO4.OO15.OO16.O..O6.OO22.O10.O.OO11.O19.O4.OO3.O12.3O
4.O31.O15.OO8.O43.O80.O.O30.O.O3.O4.OO9.O..O8.O..O8.O.O38.O.O12.3O10.O
3.O.O29.OO15.OO..O6.O125.O29.O.O3.OO4.3O7.OO..OO7.O12.O40.O14.3O8.OO
..OO15.OO13.OO13.O.O4.OO5.O8.OO145.O11.OO22.O.O66.O.O
4.O14.3O11.3O13.O7.O5.O9.O156.OO24.OO67.OO
..OO17.OO.O9.OO26.O71.OO94.O
..3O5.O10.O..O10.OO23.OO73.O
10.OO.........OO.O...........O
..O..O13.3O139.O
..O.O14.OO113.3O23.3O
..O132.OO127.O72.OO
3.O128.OO130.OO71.O
3.O.O126.3O117.O.O73.O6.O.O
4.O45.OO81.O.O116.O3.O71.O.O4.OO
3.OO46.O82.OO3.OO5.OO12.3O47.O31.OO12.O10.OO45.OO15.OO
139.O7.O13.O48.O.O29.O14.O7.O..O45.O16.OO
..O..O204.OO44.O7.O46.OO18.OO10.OO23.OO
.O47.O.OO161.OO36.O3.O7.O45.3O15.O.O13.O23.O
OO..O44.O.O161.3O36.O.O9.O46.OO15.O17.OO10.O7.O.O
..4O44.O161.O.O..O3.O43.O..O5.OO29.OO7.O19.OO10.3O7.O.O7.OO
..O.OO44.OO160.OO..OO..OO45.OO5.O.O27.O.O7.OO18.O11.OO6.OO
..O.O45.OO164.OO58.O27.O39.O9.OO
..3O45.OO224.OO25.OO38.OO9.OO
..OO352.O.O10.O
3.O.OO351.O8.3O
6.O58.O59.O59.O59.O59.O60.O
6.O57.O59.O59.O59.O59.O61.OO
4.3O57.O3.O44.O10.O3.O44.O10.O3.O44.O10.O3.O44.O10.O3.O
..OO60.4O44.O11.4O44.O11.4O44.O11.4O44.O11.4O
..OO..O105.O3.O55.O3.O55.O3.O55.O3.O
5.O106.4O56.4O56.4O56.4O
3.OO311.OO
3.3O310.3O6.OO7.OO25.OO3.OO
310.O...O..O.O.....O.........O.........................O.....O
276.OO................................OO..OO..OO......OOOOOOOOO
272.OO..OO..OO32.OO7.3O..5O..3O20.OO..O3.O
272.O.O..O3.O41.O..O..3O..O..O19.OO4.3O
273.3O48.OO9.OO22.O
62.O89.O6.O114.OO
60.O.O88.OO.O..O.OO178.OO
61.OO89.O.O..O.O167.O.O10.OO
153.O4.O168.O..O8.O
307............OO..........OO...........OO
307.O..........O.........O...OO........O.O.................O
131.OO47.O75.OO49.OO21.OO9.O11.O6.OO.OO
131.O48.O.O74.O38.O11.OO17.O..O10.O..O7.OO
129.O.O48.OO55.O.O17.O.O6.O29.O.O3.OO4.3O16.O.O11.O17.O5.O
84.O44.OO75.OO9.OO17.O..O18.OO4.O.O30.O.O3.O4.OO32.O.O
84.OO109.O9.O..O.O3.O.O..O7.OO6.OO17.O7.OO15.OO16.O..O6.OO7.OO25.OO14.OO3.OO
83.O.O110.O8.3O9.3O7.O5.OO3.O14.O.O6.OO16.O16.O.O7.O8.O.O
192.O4.O..O7.OO5.OO18.OO16.OO.O5.OO18.OO12.O.O19.O
192.OO.O..O.OO5.O..5O..O18.O..O13.OO.OO6.O.O15.3O11.O21.OO
196.OO9.OO7.OO19.O.O13.OO.O9.O15.OO
19.3O231.O.O3.OO19.O
19.OO233.O4.O.O17.OO
21.O63.OO58.OO58.OO54.O
18.OO..O61.4O56.4O56.4O53.OO
18.OO54.4O5.OO.OO46.4O5.OO.OO55.OO.OO153.O
20.3O51.O3.O5.OO48.O3.O5.OO58.OO155.OO
22.O51.O59.O
22.O52.O59.O
19.O.OO
18.OO164.OO
18.3O40.OO122.O
18.O.O40.O90.O4.O27.O.O5.OO23.OO
18.O.OO30.OO5.O.O88.OO.O..O.OO26.OO5.O.O22.O
18.4O28.O..O5.OO89.OO6.OO36.O11.O.O5.O.O
16.OO..O16.O.O9.O100.3O4.3O33.O..O10.O..O5.OO
17.O19.O3.O7.O146.O9.OO46.OO9.OO
18.O..O5.O13.O7.O135.O7.O.O8.OO3.O44.O.O7.O.O
27.OO13.O7.O..O91.O38.OO7.OO11.OO12.O.O25.O5.O8.O10.OO
19.OO20.O10.OO91.O.O32.O3.O.O20.O..O7.O3.O24.O.O13.O..O8.O
20.O16.O3.O86.O17.O.O30.OO27.O.O7.O10.OO3.OO10.O.OO13.O
19.O.O15.O.O88.OO16.O..O3.OO4.O57.O10.O.O3.O..O7.OO.OO14.O.O
19.O30.OO77.OO15.O.O5.O4.OO19.O37.O11.O7.O7.O.OO15.OO
18.O31.O12.O55.O9.3O13.O.O10.O.O18.O.O31.OO3.O3.O15.O8.O.O
18.O.O42.OO54.OO8.OO7.O.O4.O32.O..O30.O.O5.O.O15.O9.O
18.O..O106.OO9.OO36.O..O31.O21.O..O5.OO
63.O64.O10.O21.OO48.OO21.OO7.O.O
18.3O41.O.O97.O17.O64.O
18.OO42.O..O22.4O87.OO22.OO40.OO
20.O20.OO20.O..O20.O7.OO62.O..O42.O
18.OO20.O.O44.O3.OO3.O63.O..O28.O6.O6.O8.OO
19.O.O8.OO7.O12.O10.O24.O..O15.OO52.O.O28.O.O4.OO5.O9.O
20.O9.O8.O..O8.O.O9.OO41.O..O52.O18.O13.OO3.O5.O
39.O10.O.OO52.O74.OO12.OO8.O
40.O.O5.O.O.OO52.O54.OO32.OO6.OO
41.OO7.O.OO52.O.OO52.O29.O.O
51.O.O8.OO44.O24.O58.O
52.O9.O.O68.OO
64.O59.OO8.OO14.O
64.OO41.O16.O9.3O13.O.O
107.OO.........................OO...............O.O.....O
107...........................OO................O..O...OO
107...........................O.................O.O
107............................................O.O
72.....O.........................................................................O
72...O.O.............................O
72.OO...............OO..............OO
66.OO....OO................O............................OO
66.O.....OO..................OO.......................O..O
66.........O.O...............OOO.......O.............O...........OO
66...........O...............OO......OOOO............O............O
66.........................O........O.O.OO...........O
66........................OO.......O..O.OOO...........O..O
66..................................O.O.OO..............OO
66...................................OOOO
66.....................................O
