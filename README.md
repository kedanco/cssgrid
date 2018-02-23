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

## Lesson 11: Spanning and Placing Cardio
- Keeping code examples is a good way of recapping, maybe I should do this for every note file that I write.
- .item20{ grid-row: 4 / span 3; } didn't notice that I could provide a span as a start/end value, makes it so much more flexible that I don't need to specify a fixed value :)
- grid-template-columns: repeat(5,1fr 2fr); And of course, thank God for repeat values :)

## Lesson 12: auto-fit and auto-fill
- when there's items to fill up a grid, auto-fit and auto-fill kinda do the same thing
- when there's not enough items, auto-fill extends the grid (as if there's extra tracks) and auto-fit ends the grid at the last item.
- using auto-fill and placing the last track to the end simulates a responsive navbar behavior. auto-fit feels like a 'fixed' positioning instead.

## Lesson 13: Using minmax() for Responsive Grids
- Sometimes text get too big for their track sizes.
- Having minmax(150px,1fr) as the value for track size makes the track size flexible.
- auto-fill minmax will see the tracks resize for a lil-bit everytime the grid size changes
- auto-fit minmax displays truly responsive behavior -  with the tracks spreading out over the full-width.
- 'auto' for a specific track size may make it full-width when other tracks are not, no more consistency
- fit-content limits a track size.

## Lesson 14: Grid Template Areas
- name your areas by using grid-template-areas: "sidebar-1 content sidebar-2" "sidebar-1 content sidebar-2";
- assign the tracks to these areas using
grid-area: footer;
- Line names are given automatically from the area names
- chaining a whole block of area names is possible grid-template-areas:
        "A A A A B C D E"
        "A A A A B C D E"
        "A A A A B C D E"
        "A A A A B C D E"
- grid-column: A-start / E will then make the track full-width
- grid-area: A will make the element span across the whole A block.

## Lesson 15: Naming lines in CSS Grid
- naming of lines is done using [name-here] syntax
- naming should be in-between track values to denote start and end line names like [content-start] 500px [content-end] 1fr [site-right]
- name multiple line names by spaced values inside an [] sign, [sidebar-start site-left] 1fr

