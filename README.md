Srend   2022nov07 (v 20221107)   Ted Wetherbee   
Contact: ted@fdltcc.edu  .OR.  ted@tedwetherbee.org
Available:  https://srend.nongnu.org  .OR.  https://tedwetherbee.org/srend

**********************************************************************
MANUALS
srend_man.pdf
vrd_man.pdf

**********************************************************************
SOURCE in src/
Srend files:   srend.F90   Fortran Srend code
               srendc.c    C code for sleep routines, and LodePNG
                           written by Lode Vandevenne.  LodePNG  
                           source and other code is available:
                             https://lodev.org/lodepng/
                             https://github.com/lvandeve/lodepng
               srend.H     header file for C++
               
Test script:   t.sh        preps and runs test codes for Srend
                           and Vrd
                           
Test codes:    t_*         Test codes in Fortran, C, C++, and Python
                           to exercise Srend features
                          
Vrd:           vrd.F90     Source code for Vrd
Vrd scripts    vrd.script* Vrd scripts exercises Vrd features
Vrd data       vrd*bob*    Fortran programs to generate BOB data
                           for Vrd scripts
                           
                           
**********************************************************************
QUICKSTART to test Srend and Vrd with test t_* programs

1. cd src
2. edit t.sh to select/add compilers with MPI library
3. chmod 755 t.sh
4. ./t.sh   # run the test programs

Images and movies are created in the current directory, then moved
to the t_result_imagery/ directory when done.  If all went well, 
Errors = 0.  63MB of images and movies should be created.  If ffmpeg
was not in the path, movies won't exist.

It is helpful to have several CPU cores for MPI tests, but not required.

**********************************************************************
LICENSE regarding srend.F90 within srend.F90 and applying also to 
vrd.F90, and t_* test code files
 --------------------------------------------------------------------
 Copyright Notice
 --------------------------------------------------------------------
 Copyright (c) 2016-22 Ted Wetherbee
 
 Permission is hereby granted, free of charge, to any person 
 obtaining a copy of this software and associated documentation files 
 (the "Software"), to deal in the Software without restriction, 
 including without limitation the rights to use, copy, modify, merge,
 publish, distribute, sublicense, and/or sell copies of the Software,
 and to permit persons to whom the Software is furnished to do so, 
 subject to the following conditions:

 The above copyright notice and this permission notice shall be
 included in all copies or substantial portions of the Software.

 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, 
 EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
 MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND 
 NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS
 BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN
 ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN 
 CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE 
 SOFTWARE.


LICENSE regarding LodePNG code (lodepng.c and lodpng.H) within srendc.c
/*
LodePNG version 20220717

Copyright (c) 2005-2022 Lode Vandevenne

This software is provided 'as-is', without any express or implied
warranty. In no event will the authors be held liable for any damages
arising from the use of this software.

Permission is granted to anyone to use this software for any purpose,
including commercial applications, and to alter it and redistribute it
freely, subject to the following restrictions:

    1. The origin of this software must not be misrepresented; you must not
    claim that you wrote the original software. If you use this software
    in a product, an acknowledgment in the product documentation would be
    appreciated but is not required.

    2. Altered source versions must be plainly marked as such, and must not be
    misrepresented as being the original software.

    3. This notice may not be removed or altered from any source
    distribution.
*/

