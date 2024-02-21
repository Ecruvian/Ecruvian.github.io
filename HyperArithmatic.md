[ <script
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
  type="text/javascript">
</script> ]: #

[The above javascript script enables browsers to read the \(\LaTeX\) scripts in this page by calling upon mathjax. One dollar sign leads to inline, two leads to block. It isn't necessary here because the default github reader already reads LaTex.]: #

### Some Useful Equations When Drawing Hypercubes
- [Calculating basic features](#making-tables)



[The curly bracket heading ID didn't work for me. The guide does say it's dependent on the processor, so maybe that's just this preview.]: #
## Making Tables 
A hypercube is not a cube. A hypercube is related to a 3-cube in the same way a 3-cube is related to a square.

You may remember learning about the properties of a cube when you were in primary school. Here are a few of them:
- Polygons have corners, also called vertices. A cube has eight of them.
- Polygons have edges. A cube has twelve of them.
- Polygons have flat surfaces, also called faces. A cube has six of them.

There are other properties of a cube that we usually learn when we are a little bit older. For example:
- We can calculate the surface area of a polygon by adding the size of each size. For a cube with an edge length of $x$, the surface area is $6x^2$, because it has six sides and each has an area of $x^2$.
- We can calculate the volume of a cube with an edge length of $x$ using the equation "_x_ cubed," or $x^3$. (You can calculate the size of a square with $x$ squared. Note that naming convention.)

When you are making models of hyperspace, you will eventually need to know about the properties of whatever shape you are working with. For a hypercube, you can calculate the basic properties very easily in a table.

To start with, make your table:

|dimensions in space:|vertices|edges|faces|volumes|hypervolumes|5-volumes|etc...|
|----|----|----|----|----|----|----|----|
|0| | | | | | | |
|2| | | | | | | |
|3| | | | | | | |
|4| | | | | | | |
|5| | | | | | | |
|6| | | | | | | |

It is more concise and easier to read if, instead of calling the elements by the same name, you just refer to them as the dimension they represent:

| |0|1|2|3|4|5|$n$|
|----|----|----|----|----|----|----|----|
|0| | | | | | | |
|2| | | | | | | |
|3| | | | | | | |
|4| | | | | | | |
|5| | | | | | | |
|6| | | | | | | |

## Filling in the table yourself

An entire table of any size can be filled systematically. We will name each cell $C_{x,y}$. 

First, let's fill in the first column (column $y=1$). Every cell in this column should be double the column above it, starting with 1. To do this, use this formula:
$$C_{x,1}=2^x$$

| |0|1|2|3|4|5|$n$|
|----|----|----|----|----|----|----|----|
|0|1| | | | | | |
|2|2| | | | | | |
|3|4| | | | | | |
|4|6| | | | | | |
|5|12| | | | | | |
|6|24| | | | | | |

For all other cells, you will use this formula:
$$C_{x,y}=2C_{x-1,y}+C_{x-1,y-1}$$

| |0|1|2|3|4|5|$n$|
|----|----|----|----|----|----|----|----|
|0|1| | | | | | |
|2|2|1| | | | | |
|3|4|4|1| | | | |
|4|6|12|6|1| | | |
|5|12|30|24|8|1| | |
|6|24|72|78|40|10|1| |

## Filling in the table using a spreadsheet software

If you want to use Microsoft Excel, Google Sheets, LibreCalc, et cetera, you can make this table as big as you need very quickly. Start with a square area:
| |**A**|**B**|**C**|**D**|**E**|**F**|**G**|
|----|----|----|----|----|----|----|----|
|**1**| | | | | | | |
|**2**| | | | | | | |
|**3**| | | | | | | |
|**4**| | | | | | | |
|**5**| | | | | | | |
|**6**| | | | | | | |
|**7**| | | | | | | |

# To make your headers:

1. Add a 0 to cell **B1** and **A2**
2. Type =**B1**+1 in cell **C1**, then copy/paste or drag that formula to the right across row **1**.
3. Type =**A2**+1 in cell **A3**, then copy/paste or drag that formula down column **A**.

Here is what the formulas will look like:

| |**A**|**B**|**C**|**D**|**E**|**F**|**G**|
|----|----|----|----|----|----|----|----|
|**1**| |0|=**B1**+1|=**C1**+1|=**D1**+1|=**E1**+1|=**F1**+1|
|**2**|0| | | | | | |
|**3**|=**A2**+1| | | | | | |
|**4**|=**A3**+1| | | | | | |
|**5**|=**A4**+1| | | | | | |
|**6**|=**A5**+1| | | | | | |
|**7**|=**A6**+1| | | | | | |

I recommend formatting these headers in some way for clarity's sake. 

# To fill in the first column:

Type =2^**B1** in cell **B2**, then copy/paste or drag that formula down column **B**. 

Here is what the formulas will look like:

| |**A**|**B**|**C**|**D**|**E**|**F**|**G**|
|----|----|----|----|----|----|----|----|
|**1**| |0|=**B1**+1|=**C1**+1|=**D1**+1|=**E1**+1|=**F1**+1|
|**2**|0|=2^**B1**| | | | | |
|**3**|=**A2**+1|=2^**B2**| | | | | |
|**4**|=**A3**+1|=2^**B3**| | | | | |
|**5**|=**A4**+1|=2^**B4**| | | | | |
|**6**|=**A5**+1|=2^**B5**| | | | | |
|**7**|=**A6**+1|=2^**B6**| | | | | |

# To fill in the rest of the table:

Type =2\***C2**+**B2** in cell **C3**, then copy/paste or drag that formula in a square down and to the right.

Here is what the formulas will look like:

| |**A**|**B**|**C**|**D**|**E**|**F**|**G**|
|----|----|----|----|----|----|----|----|
|**1**| |0|=**B1**+1|=**C1**+1|=**D1**+1|=**E1**+1|=**F1**+1|
|**2**|0|=2^**B1**| | | | | |
|**3**|=**A2**+1|=2^**B2**|=2\***C2**+**B2**|=2\***D2**+**C2**|=2\***E2**+**D2**|=2\***F2**+**E2**|=2\***G2**+**F2**|
|**4**|=**A3**+1|=2^**B3**|=2\***C3**+**B3**|=2\***D3**+**C3**|=2\***E3**+**D3**|=2\***F3**+**E3**|=2\***G3**+**F3**|
|**5**|=**A4**+1|=2^**B4**|=2\***C4**+**B4**|=2\***D4**+**C4**|=2\***E4**+**D4**|=2\***F4**+**E4**|=2\***G4**+**F4**|
|**6**|=**A5**+1|=2^**B5**|=2\***C5**+**B5**|=2\***D5**+**C5**|=2\***E5**+**D5**|=2\***F5**+**E5**|=2\***G5**+**F5**|
|**7**|=**A6**+1|=2^**B6**|=2\***C6**+**B6**|=2\***D6**+**C6**|=2\***E6**+**D6**|=2\***F6**+**E6**|=2\***G6**+**F6**|

When you're done, the formulas will render this table:
| |**A**|**B**|**C**|**D**|**E**|**F**|**G**|
|----|----|----|----|----|----|----|----|
|**1**| |0|1|2|3|4|5|
|**2**|0|1| | | | | |
|**3**|2|2|1| | | | |
|**4**|3|4|4|1| | | |
|**5**|4|6|12|6|1| | |
|**6**|5|12|30|24|8|1| |
|**7**|6|24|72|78|40|10|1|
