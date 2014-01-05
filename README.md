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

Results
=============================




| Light use (10 concurrent users) | Average (ms) | Min (ms) | Max (ms) | Error |
| ------------- | ------------- | ----- | ----- |----- |
| Apache_Simple HTML Request	| 17 | 5 | 433 |	0% |
|Apache_PHP (Various processing & Calculations)|	2676|	838|	3211|	0%|
|Apache_Images (20 jpg images)|	804|	179|	1270|	0%|
|Apache_Large text (1mb)|	1203|	190|	1914|	0%|
|Apache_PHP MySQL (Read one record)|	121|	13|	611|	0%|
|JDBC MySQL (Read one record)|	28|	2|	86|	0%|
|Lighttpd_Simple HTML Request|	15|	0| 178|	0.01%|
|Lighttpd_PHP (Various processing & Calculations)|	2571|	263|	5678|	0%|
|Lighttpd_Images (20 jpg images)|	554|	0|	1234|	0.01%|
|Lighttpd_Large text (1mb)|	1173|	196|	2624|	0%|
|Lighttpd_PHP MySQL (Read one record)|	115|	10|	3149|	0%|
				
				
|Heavy use (100 concurrent users)|	Average (ms)	|Min (ms) |	Max (ms) |	Error|
| ------------- |-------------| -----|-----|----- |
|Apache_Simple HTML Request|	234|	5|	11829|	0%|
|Apache_PHP (Various processing & Calculations)|	26830|	3203|	50734|	0%|
|Apache_Images (20 jpg images)|	8536|	532|	27262|	0.04%|
|Apache_Large text (1mb)|	12902|	193|	37127|	0%|
|Apache_PHP MySQL (Read one record)|	1110|	16|	34548|	0%|
|JDBC MySQL (Read one record)|	240|	2|	768|	0%|
|Lighttpd_Simple HTML Request|	169|	0|	391|	0.03%|
|Lighttpd_PHP (Various processing & Calculations)|	25668|	1189|	26595|	0%|
|Lighttpd_Images (20 jpg images)|	5698|	0|	7882|	17.40%|
|Lighttpd_Large text (1mb)|	12493|	237|	25506|	0%|
|Lighttpd_PHP MySQL (Read one record)|	1125|	21|	1680|	0%|




