# RSA Factoring Challenge

## Description
The RSA Factoring Challenge is a project that focuses on factoring natural numbers into products of two smaller numbers. This is essential for understanding and breaking RSA encryption, a widely used method for secure data transmission.
The challenge is to do this as efficiently as possible, especially for large numbers, within a 5-second runtime limit.


## Project Structure

| Task                              | Description                                          | Source Code                              |
|-----------------------------------|------------------------------------------------------|------------------------------------------|
| Factorize all the things!         | Factorize numbers into products of two factors.     | [factors](factors)                       |
| RSA Factoring Challenge            | Factorize RSA numbers into two prime factors.       | [rsa](rsa)                               |

## Environment

- **Operating System**: Ubuntu 20.04 LTS
- **Language**: Any programming language of your choice.
- **Dependencies**: None. The scripts must run without any additional dependencies.

## Requirements

- All files should end with a new line.
- The executable must run without any additional dependencies.
- The program should complete execution within 5 seconds.
- Output format should be `n=p*q` where `p` and `q` are factors of `n`.
- The file to be factorized will always end with a new line and contain natural numbers greater than 1.

## Learning Objectives

After completing this project, you should be able to:

- Understand the basics of RSA encryption and prime factorization.
- Implement efficient algorithms for factorizing numbers.
- Develop and test scripts that can perform factorization tasks under time constraints.

## How to use

**Installation**

For Ubuntu/Debian:

```bash
sudo apt-get update
sudo apt-get install gcc
```

**Compiling the Code**

Make sure to compile the code before running it:

```bash
gcc -o factors factors.c
gcc -o rsa rsa.c
```

**Running the Code**

For the general factorization task:

```bash
./factors <file>
```

For the RSA factorization task:

```bash
./rsa <file>
```

**Examples**

```bash
cat tests/test00
4
12
34
128
1024
4958
1718944270642558716715
9
99
999
9999
9797973
49
239809320265259

./factors tests/test00
4=2*2
12=6*2
34=17*2
128=64*2
1024=512*2
4958=2479*2
1718944270642558716715=343788854128511743343*5
9=3*3
99=33*3
999=333*3
9999=3333*3
9797973=3265991*3
49=7*7
239809320265259=15485783*15485773
```

```bash
cat tests/rsa-1
6

./rsa tests/rsa-1
6=3*2
```

## Tasks

## Task 0: General Factorization

### Objective
Factorize each number in a file into a product of two smaller numbers.

### Usage
```bash
./factors <file>
```

- `<file>`: A file containing natural numbers, one per line. Each line contains a valid natural number greater than 1, and the file ends with a newline character.

### Output Format
```
n=p*q
```
Where:
- `n` is the number from the input file.
- `p` and `q` are factors of `n`.

### Example

**Input File (test00):**
```
4
12
34
128
```

**Command:**
```bash
./factors test00
```

**Output:**
```
4=2*2
12=6*2
34=17*2
128=64*2
```

### Instructions
1. Implement a script that reads the file and factorizes each number.
2. Output the results in the format `n=p*q` where `p` and `q` are factors of `n`.
3. Make sure the script executes in 5 seconds for each number.
4. No external dependencies are required; the script should run as a standalone executable.

## Task 1: RSA Factoring

### Objective
Factorize RSA numbers into their prime components.

### Usage
```bash
./rsa <file>
```

- `<file>`: A file containing a single RSA number. The file should contain exactly one RSA number greater than 1.

### Output Format
```
n=p*q
```
Where:
- `n` is the RSA number.
- `p` and `q` are the prime factors of `n`.

### Example

**Input File (rsa-2):**
```
77
```

**Command:**
```bash
./rsa rsa-2
```

**Output:**
```
77=11*7
```

### Instructions
1. Implement a script to read the RSA number from the file and factorize it into two prime numbers.
2. Output the results in the format `n=p*q` where `p` and `q` are prime factors.
3. Ensure the script executes within a 5-second time limit.
4. No external dependencies are required; the script should run as a standalone executable.
5. RSA numbers are guaranteed to be the product of exactly two prime numbers. Use efficient algorithms suited for factorizing large numbers.


## Additional Notes

- Make sure your executable is optimized for speed.
- Avoid using external libraries or dependencies.
- If you need to factor large RSA numbers, use Pollard's rho algorithm or elliptic curve factorization. 
- Ensure proper handling of large numbers and edge cases, including very large primes or near-primes.


## Background Context
RSA (Rivest-Shamir-Adleman) is a public key cryptosystem based on the difficulty of factorizing large composite numbers into their prime factors. Your task is to factorize RSA numbers as quickly as possible to demonstrate the efficiency of your algorithm and to understand the practical implications of number theory in cryptography.
