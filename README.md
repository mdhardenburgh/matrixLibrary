# matrixLibrary
C++ matrix library for fast computation

## Introduction
The purpose of this project is to provide an easy to use standalone matrix library. It is designed to be in the style of a C standard library.

## Usage
This library can be slotted into any project or added as a git submodule. If added as a git submodule, the unit tests will not be built unless explicitly build them. A cmake file is provided and may be modified to fit your project.

To instantiate a matrix object, simply declare something like `matrix<uint32_t> resultMatrix;`, where uint32_t is a numerical data type. Other data types or even object can be used, but may not make sense

The library is separated into two parts, operations on matrices and operations with matrices. Operations on matrices are getters, setters, fillers (fill the matrix with a number) or printers (print the contents of the matrix). Operations between matrices include add, subtract, matrix multiply, transpose, hadamard product, and scalar multiply.

## Testing
This library includes unit tests based on the gtest testing framework. Running these unit tests require that you have at least cmake version 3.23.1 installed on your system. If you would like to build these tests follow these steps:

Starting in the root directory:
1. `$ cmake -S unitTest -B unitTest`
2. `$ cmake --build unitTest`
3. `$ cd unitTest/`
4. `$ ctest`

## Roadmap
Here is a list that includes functionality that I would like to add to this matrix library, but it is not a complete list, and priories may change:
* Matrix Inverse
* Matrix Determinant
* multithreaded matrix add/subtract
* multithreaded scalar multiply
* multithreaded hadamard product
* Strassen improvement to matrix multiply
* Multithreaded Strassen matrix multiply
* Cuda ...

## License
Copyright &copy; Matthew Hardenburgh 2024

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.