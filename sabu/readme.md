//
// main.c
// checkPrime
//
// Created by Murat Durgut on 15.10.18.
// Copyright © 2018 FHV IT. All rights reserved.
//


#include <stdio.h>
#include <math.h>


int checkPrime(int n)
{
    int t = 0;
    int i = 2;
    int out;
    if((n==1)||(n==2)){
    return 1;
    }
    else {
    return 0;
    }

    while (i<=n/2)
    {
        if( n % i == 0)
            t++;
            i++;
    }

    if (t==1) {
        out = 1;
    } else {
        out = 0;
    }
    return out;
}

int main()
{
    printf("checkPrime\n");
    int n;
    printf("Enter number to check: ");
    scanf("%d", &n);

    printf("%d checkPrime = %d", n, checkPrime(n));
    printf("\n");
    return 0;
}
