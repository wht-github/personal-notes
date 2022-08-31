# Rectangle Packing

## Optimal Rectangle Packing: An Absolute Placement Approach

## Methodology

### Overall Search Strategy

> 1. The minimum bounding box algorithm generates an initial candidate set of bounding boxes of various widths and heights.
> 2. The containment solver is called for each bounding box in order of increasing area, and for each infeasible bounding box, we insert another back into the candidate set of bounding boxes with a height one unit greater. If a packing was found, we continue testing boxes of equal area to find all optimal solutions before terminating.
> 3. The containment solver first works on the x-coordinates in a model where variables are rectangles and values are x-coordinate locations, using dynamic variable ordering and a constraint that detects infeasible subtrees.
> 4. For each x-coordinate solution found, the problem is transformed into a perfect packing instance.
> 5. It then searches for a set of y-coordinates in a model where variables are empty corners and values are rectangles.

### Minumum Bounding Box Problem

generate box with all size of

- *lower bound*: on the area is the sum of the rectangles' area
- *upper bound*: set height to the tallest rectangle's height, greedy put rectangle from left to right, and check from bottom to top. and get the correspond width $width_g$

#### Pruning the set of bounding boxes

1. generate a set of width for bounding box [the widthest rectangle's width, the greedy solution result $width_g$]
2. then for each width, generate a feasible height.(specific method is followed)
3. the result boxes, building a min-heap by area, use a `containment solver` to test the bounding box, if not success, increasing the height by 1, insert new box back to min-heap, loop until the mininum succeed box.

##### Generate a feasible height

1. height must be at least the height of the tallest rectangle
2. $height * width$ must larger than the total area of the sum of rectangles
3. if for every pair of rectangles, the sum of 2 rectangles' width larger than box width, than height must be at least sum of all height.(a vertical line)
4. rectangles whose width larger than half of box width, must be put vertically

##### Anytime Algorithm

