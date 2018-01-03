I have created a Jupyter Notebook and used the updated function by @Irene-GM
More here: https://github.com/Irene-GM/sammon


Sammon mapping in Python
========================
Date: 18 April 2014

sammontest.py
-------------
Run sammontest.py() with no arguments to test sammon.py
on Fisher's iris dataset

sammon.py
---------
Simple python implementation of Sammon's non-linear mapping 
algorithm [1]. Perform Sammon mapping on dataset x

y = sammon(x) applies the Sammon nonlinear mapping procedure on
multivariate data x, where each row represents a pattern and each column
represents a feature.  On completion, y contains the corresponding
co-ordinates of each point on the map.  By default, a two-dimensional
map is created.  Note if x contains any duplicated rows, SAMMON will
fail (ungracefully). 

[y,E] = sammon(x) also returns the value of the cost function in E (i.e.
the stress of the mapping).

An N-dimensional output map is generated by y = sammon(x,n) .

A set of optimisation options can be specified using optional
arguments, y = sammon(x,n,[OPTS]):

* maxiter        - maximum number of iterations
* tolfun         - relative tolerance on objective function
* maxhalves      - maximum number of step halvings
* input          - {'raw','distance'} if set to 'distance', X is interpreted as a matrix of pairwise distances.
* display        - 0 to 2. 0 least verbose, 2 max verbose.
* init           - {'pca', 'random'}

The default options are retrieved by calling sammon(x) with no
parameters.

Authors
-------
Tom J. Pollard (https://twitter.com/tompollard)

Ported from MATLAB implementation by 
  Gavin C. Cawley and Nicola L. C. Talbot

References
----------
[1] Sammon, John W. Jr., "A Nonlinear Mapping for Data
    Structure Analysis", IEEE Transactions on Computers,
    vol. C-18, no. 5, pp 401-409, May 1969.

Copyright
---------
Copyright   : (c) Dr Gavin C. Cawley, November 2007.

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307 USA
