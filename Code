#include <stdio.h>
#include <string.h>
void main() {
    char s[100],w[25];
    int i, id, max, count, len, k = 1;
    gets_s(s);
    len = strlen(s);
    max = 0;
    id = 0;
    count = 0;
    for (i = 0; i < len; i++)
        if (s[i] != ' ') count += 1;
        else {
            if (count > max) {
                max = count;
                id = i - count;  //Индекс начала этого слова(определяется вычитанием длины слова из текущего индекса)
            }
            count = 0;
        }

    if (count > max) {
        max = count;
        id = i - count;
    }
    max += id; 
    for (i = id; i < max; i++) //Часть строки от первой буквы на длину слова
        w[i] = s[i];
    for (i = 1; i < max; i++) {
        k++;
        if ((k % 2) == 0) w[i] = w[i] - w[i];
    }
    for (i = id; i < max; i++) 
        putchar(w[i]);
}
