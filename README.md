# Riemann-zeta function

The Riemann Zeta function is defined as the summation of 1/n^s for n=1 to infinity. It is a function of s which is a complex variable, i.e. s = x + iy, for some real numbers x and y. This is one of the most important functions in modern number theory, particulary due to it's intimate connection to the prime numbers. These connections are related to the instances of the variable s where the Riemann Zeta function is equal to zero, these instances are called zeros. The trivial zeros occur when s = -2, -4, -6, -8, ... The non-trivial zeros are what mathematicians are most interested in, because they have mysterious and far reaching consequences related to the prime numbers. It has been proven that these non-trivial zeros occur between x = 0 and x = 1 in the variable s = x +iy. The Riemann Hypothesis is one of the 7 remaining unsolved millennium problems, there were originally 23. It conjectures that all of the non-trivial zeros occur at x = 1/2, called the critical line.

The Riemann-Siegel approximation for the Riemann Zeta function can be used to estimate the function near the critical line, namely x = 1/2, making it a good method for approximating the non-trivial zeros. It turns out that it is not a good approximation away from the critical line. This project investigates the previous claim that it is not a good approximation away from the critical line. The investigation employs code written in Python.

The code Plot_Riemann_Zeta_Critical_Line.py generates a plot, namely Z(t)_plot.png, comparing the modulus of the
Riemann zeta function evaluated on the critical line (for complex numbers
s=1/2+it) to the Riemann-Siegel Z-function, which is one of the most powerful numerical methods for computing
the Riemann zeta function near and on the critical line. It was used to compute the first 1.5 billion zeros and verify that they lie on the critical line.

In Python, mpmath has built in functions pertaining to the Riemann zeta function, including zeta(), zetazeros(), and siegelz().

The plot Z(t)_plot.png exposes the Riemann-Siegel formula as a convenient way of exploring the Riemann zeta
function near the critical line, notice how the blue and orange paths overlap in the first quadrant meeting at the zeros.

The code Siegel_Graph_Loop.py generates a list of plots starting at a given input, it plots the modulus of the Riemann zeta function along an array of input values for its real part (by default the input values are from -0.5 to 1.5 but that can easily be changed in the code) converging to the Riemann zeta function evaluated at 0.5 (which is the same as the plot Z(t)_plot.png). The plots were then used to make a stillframe video, namely output.mp4. It further demonstrates that the Riemann-Siegel formula is a good approximation near the critical line but not away from it. This can clearly be seen in the video called output.mp4.

The video was created using ffmpeg which you can install on ubuntu using the command "sudo apt-get install ffmpeg". The command line which was used to create the video is in the text file called "Make_mp4_from_png_files_ubuntu.txt". Notice it takes any .png file starting with "zeta_plot1_" and uses them to create an .mp4 file.

For more information on the Riemann-Siegel Approximation, read "Computational methods for evaluating
the Riemann zeta function" which can be found in this repository.

For neat visualizations of the Riemann Zeta function using python, check out Christian S. Perone's article "Riemann Zeta function visualizations with Python". Here is a link...

http://blog.christianperone.com/2010/02/riemann-zeta-function-visualizations-with-python/#comments
