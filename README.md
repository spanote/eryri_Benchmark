eryri_Benchmark
===============

various test benchmark results for the raspberry pi using a number of web servers

Environment
==================
Tools: apache-jmeter2.10

Network : Raspberry pi and Test computer connected to a Cisco EPC2325 router through a Lan interface (RJ-45 cable)

Type of tests: Light use (10 concurrent users, 1000 iterations), Heavy use (100 concurrent users, 100 iterations)

Types of tests
===================
Simple HTML Test: Simple short HTML page with text stating "Welcome to Raspberry Pi Test page" (80 bytes) 

PHP test : A series of processes consisting of 

1. randomly generating an array of 1000 numbers 

2. sorting the numbers in the array

3. performing plus, minus, multiply and division operations on a random data element in the array and looping 1000 times

4. Generating 1000 key and value elements for a hash and then going through each key and value and then  printing them out

5. File operations, listing the files in a prearranged directory (10 empty text files)

6. Outputing the current system data and time.

Image Test: Loading 20 images. Images randomly drawn from the caltech 101 image set one each from twenty categories

Large Text file test: 1 MB text file. Text drawn from the loren ipsum generator.

SQL test: Read one record from a sample database from oracle. Data consists of 490,000 records.



