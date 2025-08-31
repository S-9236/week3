#include <stdio.h>
int main() {
    int arr[100];
    int i,j,found=0;
    printf("enter 100 integers:\n");
    for (i=0;i<100;i++) {
        scanf("%d",&arr[i]);
    }
    printf("pairs whose sum is 50:\n");
    for (i=0;i<100;i++) {
        for (j=i+1;j<100;j++) {
            if (arr[i]+arr[j]==50) {
                printf("(%d,%d)\n",arr[i],arr[j]);
                found=1;
            }
        }
    }
    if (!found) {
        printf("no such pairs found\n");
    }
    return 0;
}
