#!/usr/bin/python3

import sys
import math

def factorize_number(number):
    factors = []
    sqrt_n = int(math.sqrt(number))
    for i in range(2, sqrt_n + 1):
        if number % i == 0:
            factors.append((i, number // i))
    return factors

def main():
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        return

    open_file = sys.argv[1]

    try:
        with open(open_file, 'r') as file:
            for line in file:
                number = int(line.strip())
                n = factorize(number)
                for p, q in n:
                    print(f"{number}={p}*{q}")
    except FileNotFoundError:
        print(f"File '{open_file}' not found.")

if __name__ == "__main__":
    main()
