# havkerrank-percursion-problem-in-c


#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
//Complete the following function.
int sum_last_three_terms(int x,int y,int z){
    return x+y+z;
}

int nth_term(int n, int a, int b, int c) {
  //Write your code here.
  int the[n+1];
  the[1]=a;
  the[2]=b;
  the[3]=c;
  
  the[n]=sum_last_three_terms(the[n-1],the[n-2],the[n-3]);
  return the[n];
}

int main() {
    int n, a, b, c;
  
    scanf("%d %d %d %d", &n, &a, &b, &c);
    int ans =nth_term(n, a, b, c);
 
    printf("%d", ans); 
    return 0;
}
