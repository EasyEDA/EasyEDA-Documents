# Functions

The sections on expressions and parameters shows how component and source values can be defined using arithmetic equations. The examples used to illustrate this used only simple linear expressions. This section introduces the concept of functions.

Functions hugely expand the power of parameters and expressions by allowing the creation of expressions including non-linear functions of other parameters

## Predefined functions

EasyEDA has a number of pre-defined functions. Many of them are immediately available to be used in expressions because they are built-in to ngspice or they are automatically added in to the spice netlist by EasyEDA at the time of first saving a schematic.

Some are not yet automatically added in to the netlist so their definitions must be pasted in manually before they can be used. These function definitions are clearly indicated in the examples illustrating each function.

These functions will be appended to the list of those automatically added to the netlist soon.

All the currently available pre-defined functions are listed, together with illustrative examples, in the table below.

Note that all the functions in this list can be used in any context in EasyEDA: in the value fields and in expressions for component values, Independent Sources and for B Sources.

### Table of functions
<table border="1" cellspacing="0">

  <colgroup width="139"></colgroup> <colgroup span="3" width="85"></colgroup>
  <tbody>
    <tr>
      <td align="left">Function</td>
      <td align="left">Description</td>
      <td align="left">ngspice native or EasyEDA special</td>
      <td align="left">Where useable</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=xMic6oGYg" target="blank">abs(x)</a></td>
      <td align="left">Absolute value of x </td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=HEWQ8qI0U" target="blank">acos(x)</a></td>
      <td align="left">Arc cosine of x. Fails to converge for x &lt; -1
and x &gt; +1. Use invcos(x) instead.</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=IGztLFXfV" target="blank">acosh(x)</a></td>
      <td align="left">Real part of the arc hyperbolic cosine of x,
e.g., acosh(.5) returns 0, not 1.0472i</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=oOICUcunF" target="blank">arctan(x)</a></td>
      <td align="left">Alternate syntax to atan(x)</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=hDxP71jAS" target="blank">asin(x)</a></td>
      <td align="left">Arc sine of x. Fails to converge for x &lt; -1
and x &gt; +1. Use invsin(x) instead.</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=dNHZhbRL3" target="blank">asinh(x)</a></td>
      <td align="left">Arc hyperbolic sine</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=oOICUcunF" target="blank">atan(x)</a></td>
      <td align="left">Arc tangent of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=r1VdvpHZT" target="blank">atan2(y,x)</a></td>
      <td align="left">4 quadrant arc tangent of x/y (tan^-1(x/y))</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=OZTN5ZhzR" target="blank">atanh(x)</a></td>
      <td align="left">Arc hyperbolic tangent. (Limited output swing to
avoid numerical under/overflow failure.)</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=YxrJDVdvN" target="blank">buf(x)</a></td>
      <td align="left">Returns 1 if x &gt; 0.5, else 0</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=dQmEWe8qI" target="blank">ceil(x)</a></td>
      <td align="left">Integer equal or greater than x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=Xx3lfxOI0" target="blank">cos(x)</a></td>
      <td align="left">Cosine of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=y82kewO5n" target="blank">cosh(x)</a></td>
      <td align="left">Hyperbolic cosine of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=co4YgaQJ1" target="blank">exp(x)</a></td>
      <td align="left">e to the x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=E82ke86oF" target="blank">floor(x)</a></td>
      <td align="left">Integer equal to or less than x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=aAICTN5nh" target="blank">if(x,y,z)</a></td>
      <td align="left">IF x &gt; 0.5, THEN y ELSE z</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=9lR8qICUc" target="blank">ifx(x,y,z)</a></td>
      <td align="left">IF x, THEN y ELSE z</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=M82kCwO6o" target="blank">int(x)</a></td>
      <td align="left">Convert x to integer</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=JHBTb5nFX" target="blank">inv(x)</a></td>
      <td align="left">Returns 0 if x &gt; 0.5, else 1</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=WUN5nFXf9" target="blank">invcos(x)</a></td>
      <td align="left">Real part of the arc cosine of x, e.g., acos(-5)
returns 3.14159, not 3.14159+2.29243i</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=6GASM4KEV" target="blank">invsin(x)</a></td>
      <td align="left">Real part of the arc sine of x, asin(-5) returns
-1.57080, not -1.57080+2.29243i</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=x71jBTasm" target="blank">invtan(x)</a></td>
      <td align="left">Alternate syntax to atan(x)</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=tX9JjgeOC" target="blank">limit(x, L, U)</a></td>
      <td align="left">Value of x, bounded by L and U</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=tJDVd7pGY" target="blank">ln(x)</a></td>
      <td align="left">Natural logarithm of x. Fails with errors for
negative x. Use log(x) instead.</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=CzRL3lDVd" target="blank">log(x)</a></td>
      <td align="left">Natural logarithm of x. Generates a real valued
output for all x, limited to a minimum of approximately -230.5 for x
&lt;= 1e-100.</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=CzRL3lDVd" target="blank">log(x)</a></td>
      <td align="left">Base 10 logarithm. Generates a real valued
output for all x, limited to a minimum of -100 for x &lt;= 1e-100.</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=dHhsqoYWw" target="blank">max(x,y)</a></td>
      <td align="left">The greater of x or y</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=Hzxusq0mk" target="blank">min(x,y)</a></td>
      <td align="left">The smaller of x or y</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=LNHBvN5nF" target="blank">pow(x,a)</a></td>
      <td align="left">Real part of x raised to the power of a. Zero
for negative x and fractional a</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=LNHBvN5nF" target="blank">pwr(x,a)</a></td>
      <td align="left">The absolute value of x raised to the power of a</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=LNHBvN5nF" target="blank">pwrs(x,a)</a></td>
      <td align="left">pwr(x) multiplied by the sign of x </td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=iEyrJ1jBT" target="blank">sgn(x)</a></td>
      <td align="left">Sign of x. Returns -1 for x &lt; 0, 0 for x == 0
(where == means 'exactly equal to') and 1 for x &gt; 0</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=FnhasmEWQ" target="blank">sin(x)</a></td>
      <td align="left">Sine of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=USa4KEVdv" target="blank">sinh(x)</a></td>
      <td align="left">Hyperbolic sine of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
<tr>
      <td align="left"><a href="https://easyeda.com/editor#id=t3lfxO60i" target="blank">softlim(ip, lo, hi, sharp)</a></td>
      <td align="left">Value of ip, bounded by lo and hi with the sharpness of the transition between linear and limited regions defined by 'sharp'.</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=AyQ82kCUc" target="blank">sqr(x)</a></td>
      <td align="left">Square of x</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=Aa4m2We8O" target="blank">sqrt(x)</a></td>
      <td align="left">Real part of the square root of x. Zero for
negative x</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=dM4mgyQ8q" target="blank">stp(x)</a></td>
      <td align="left">Alternate syntax for u(x)</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=cZJDVPJeY" target="blank">tan(x)</a></td>
      <td align="left">Tangent of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=db4YgyQ8q" target="blank">tanh(x)</a></td>
      <td align="left">Hyperbolic tangent of x</td>
      <td align="left">ngspice</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=dM4mgyQ8q" target="blank">u(x)</a></td>
      <td align="left">Unit step, i.e., 1 if x &gt; 0., else 0</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=ec6ohzR9r" target="blank">u2(x)</a></td>
      <td align="left">Returns 1 for x &gt;= to 1, x for x between 0
and 1, 0 for x &lt;= 0.</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
    <tr>
      <td align="left"><a href="https://easyeda.com/editor#id=B5hRPpYy8" target="blank">uramp(x)</a></td>
      <td align="left">x if x &gt; 0, else 0</td>
      <td align="left">EasyEDA</td>
      <td align="left">E, I, B</td>
    </tr>
  </tbody>
</table>

## User defined functions

There may be occasions where a function is required that maybe has to be used in several places in a schematic or it is useful in several different schematics. To save having to copy and paste a complicated expression as a block of text each time it is needed, the <span style="font-weight:bold">.func</span> statement makes it is possible to create a user defined function.

The syntax of the .func statement is very simple:

	.func myfunctionname(a,b,c, ...n) {expression of functions of a, b, c ... n}

For example:

	.func hypotenuse(x,y) {sqrt(x^2+y^2)}

defines a function that calculates the length of the hypotenuse of a right angle triangle with sides length x and y.

Once a function has been defined in a schematic in a project in this way it can be used anywhere in any schematic in that project, i.e. it does not have to be defined separately in every sheet in which it is used in a project. It does, however, have to be defined in a sheet in every project in which it is to be used but, if it's a really useful function, let us know and maybe we'll add it to the growing list of pre-defined functions!

To use the function all that is then required is to paste <span style="font-weight:bold">hypotenuse(x,y)</span> into wherever it is needed and to substitute the 'x' and 'y' with the required variables. So, for example to use the function in a parametric expression:

	.param a=3 b=4 hypot=hypotenuse(a,b)

or in a current output B Source driven by two voltages, V(oneside) and V(otherside):

	I=hypotenuse(V(oneside), V(otherside))

There are many examples of functions defined by the .func statement in the simulations linked to in the table above and in all EasyEDA spice netlists for the automatically appended predefined functions.

Note that when used in .func statements, expressions can wrap over more than one line by using the '+' continuation character.

There are several examples of this in the simulations linked to in the table above and in all EasyEDA spice netlists for the automatically appended predefined functions. For example:

	.func POW(x,a) 
	+ {(((a-(int(a)))==0)||(sgn(x)>=0))_( max(exp(ln(uramp(x))_a),0) +
	+ (2_(0.5-ABS((int(a))-2_int(a/2))))_max(exp(ln(uramp(-1_x))*a),0) )}

can be found appended to every EasyEDA spice netlist.
