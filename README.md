=============== CSS Grid Course ================
=========

<b>Wes Bos CSS Grid Course #GRIDDY Notes</b>

20th Feb 2018 - 

## Lesson 2: Starter Files and Tooling Setup
- CSS Variables help you to repeat CSS values conveniently
- using Border-box for box-sizing and everything else

## Lesson 3: CSS Grid Fundamentals
- Take an element, dice it into rows and columns (tracks) and put them into the grid layout
- need to set display:grid for the parent grid container
- gtr and gtc to decide on the rows and column sizes of the grid
- gtr and gtc can take in different formats of sizes
  > 100px 200px 100px
  > 100px 200px auto 100px
  > fr as percentages
- grid-gap is like margin between each 'track'

## Lesson 4: CSS Grid Dev Tools
- Tracks are numbered not by their columns/row number but by their start and end
- Explicit: dark-dashed line (we made those, explicit values)
- Implicit: dotted-lines (values determined by grid, we did not specify values)

## Lesson 5: CSS Grid Implicit Explicit
- Implicit Rows are created when there are not enough css values (2 value) for extra elements (3 rows of elements)
- grid-auto-rows > how big rows are if they are extra added (value for leftovers)

## Lesson 6: Grid auto-flow
- grid auto flow determines direction of extra tracks
- grid-auto-columns, grid-auto-rows control the sizing for ^

## Lesson 7: Sizing tracks in CSS Grid
- percentages not a good idea for gtr and gtc
- fr(fractional unit) is preferred
- not all the space is used because CSS Grid will slice the grid following the px sizings
- fr allows for flexible values, and making full use of the full grid
- fr can be used as a fraction compared to other tracks (1fr 3fr 1fr 1fr)
- auto will asjust to make size of content, whole column/row will follow

## Lesson 8: CSS Grid repeat function
- repeat functon(num of times, value to repeat)
- mix with other values, gtc: 100px repeat(2, 1fr auto)
- helps you to cut typing and keep code concise

## Lesson 9: Sizing Grid Items
- before free space(fr) comes into calculation, css grid will first do tracks that have explicit (determined values)
- span > works like table colspan or rowspan, ignores grid-gap and takes the size of 2 tracks. If no space, bumps to next line
- good way to create big blocks in between a grid shape
- span exceeding grid size forces the grid to be large and fit extra rows/columns in for the track.

## Lesson 10: Placing Grid Items
- start and end values may also offset grid positions
- alternative syntax grid-column: (start) / (end), grid-column: 1 / -1(last)
- -1 may only extend till end of explicit grid, other values in implicit grid may still exist outside your (-1) position
- some -1 values may not work properly if we did not define actual rows
- column and row 1 / -1 take sup entire grid, and shfits all other grid items to implicit rows and columns
