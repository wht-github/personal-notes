# Picking Object via Ray Casting

## Mouse Picking with Ray Casting for 3D Spatial Information Open-platform

### About the Paper

Korea's gov department need to do some visualize work, need to picking object in large 
amount of data

### Method

碰撞算法是trivial的，提高效率的方法是分层计算，把场景分x份，再在把每份细分，就是X分法

## My Method(also the trivial one)

- projection to the triangle plan
- use cross product to test point is within range of each angle

## Möller–Trumbore intersection algorithm
*Cant useing when triangle useing different winding order*
$$R(t) = O + tD$$

$$O + tD = V_0 + u\overrightharpoon{V_{01}} +v\overrightharpoon{V_{02}}$$

Ax=b
 
solve with carmer's rule


