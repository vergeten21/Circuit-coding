#include <reg51.h>
#define SEG P0
char code TAB[10]={0xC0, 0xF9, 0xA4, 0xB0,0x99,0x92, 0x83, 0xF8, 0x80, 0x98
};
void delay1ms(int x);
void main()
{
    char i;
    while (1)
    {
        for (i = 0; i < 10; i++)
        {
            SEG = TAB[i];
            delay1ms(500);
        }
    }
}
void delay1ms(int x)
{
    int i, j;
    for (i = 0; i < x; i++)
    {
        for (j = 0; j < 120; j++);
    }
}
