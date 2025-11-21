# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## DATE: 10.10.2025
## NAME: Guru Raghav Ponjeevith V
## REG NO: 212223220027

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:
```c
#include <math.h> 
#include <stdio.h>
long long int power(long long int a, long long int b, long long int P)
{
if (b == 1) 
return a;
else
return (((long long int)pow(a, b)) % P);
}
int main()
{
long long int P, G, x, a, y, b, ka, kb;
printf("\n**Diffie-Hellman Key Exchange algorithm\n\n"); 
printf("\n\nEnter the value of P: ");
scanf("%lld",&P); 
printf("The value of P: %lld\n", P);
printf("Enter the value of G (Primitive root of P): "); 
scanf("%lld",&G);
printf("The value of G: %lld\n\n", G);
printf("The private key a for Alice : %lld\n", a); 
x = power(G, a, P); 
b = 3; 
printf("The private key b for Bob : %lld\n\n", b); 
y = power(G, b, P);
ka = power(y, a, P); 
kb = power(x, b, P); 
printf("Secret key for the Alice is : %lld\n", ka); 
printf("Secret Key for the Bob is : %lld\n", kb);
return 0;
}
```


## Output:

<img width="1697" height="988" alt="Screenshot 2025-10-10 091450" src="https://github.com/user-attachments/assets/29a88db9-0441-4c39-be1d-9b3bc0090087" />



## Result:
  The program is executed successfully

