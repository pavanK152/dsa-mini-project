#include <stdio.h>

#define Max 5000

void Toadd(char a[], char b[], char p[])

{

  int k = 0;

  for (int i = Max - 1; i >= 0; i--)

  {

    int digit = (a[i] - '0') + (b[i] - '0') + k;

    p[i] = (digit % 10) + '0';

    k = digit / 10;

  }

}

void copybona(char a[], char b[])

{

  for (int i = Max - 1; i >= 0; i--)

    a[i] = b[i];

}

char fibonacci1[Max];

char fibonacci2[Max];

char p[Max];

int main()

{

  for (int i = 0; i < Max; i++)

  {

    fibonacci1[i] = fibonacci2[i] = p[i] = '0';

  }

  fibonacci2[Max - 1] = '1';

  int n;

  scanf("%d", &n);

  if (n == 0 || n == 1)

  {

    printf("%c", n + '0');

  }

  else

  {

    for (int i = 2; i <= n; i++)

    {

      Toadd(fibonacci1, fibonacci2, p);

      copybona(fibonacci1, fibonacci2);

      copybona(fibonacci2, p);

    }

    int t = 0;

    for (int i = 0; i < Max; i++)

    {

      if (t == 0 && p[i] == '0')

        continue;

      if (t == 0 && p[i] != '0')

        t = 1;

      printf("%c", p[i]);

    }

    printf("\n");

  }

  return 0;

}
