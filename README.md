#error?generator function to yield the first n prime numbers
def is_prime(num):
    if num < 2:
       return False
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            return False
    return True
    
def prime_generator(n):
    count, num = 0, 2
    while count < n:
       if is_prime(num):
          yield num
          count += 1
    num += 1
    
#gen = prime_generator(10)
# ... = in gen:
for prime in prime_generator(10):
    print(prime)
