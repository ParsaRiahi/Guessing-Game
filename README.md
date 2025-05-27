# Guessing-Game
Originally called Game.c


#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main (void)
{
    int guess;
    int secret;

    printf("UNIX seconds %d\n", time(0));
    srand(time(0));
    secret = rand () % 100;
    printf("Guess a number\n");

    while (1)
    { 
        scanf("%d", &guess);
        if (guess < secret)
        {
            printf("Go higher!\n");
        }
        if (guess > secret)
        {
            printf("Go lower!\n");
        }
        if (guess == secret)
        {
            printf("Nice!\n");
            break;
        }
    }
    return 0;
}
