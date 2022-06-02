# even-fibonacci-numbers
#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int main(){
    int t; 
    scanf("%d",&t);
    unsigned long long arr[1000];
    arr[0]=1;
    arr[1]=2;
    for(int i=2;i<120;i++) {
        arr[i]=arr[i-1]+arr[i-2];
    }
    while(t--){
      unsigned long long n;
      scanf("%lld",&n);
      unsigned long long sum = 0;
      for(int i=0;i<120;i++){
        if(arr[i]<=n){
            if(arr[i]%2==0)
            sum+=arr[i];
        }else{
            break;
        }
      }
        printf("%lld\n",sum);
    }
    return 0;
}
   
