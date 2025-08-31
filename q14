#include <stdio.h>
void readMatrix(int p, int q, int r, int a[p][q][r]) {
    int i, j, k;
    printf("enter elements of %dx%dx%d matrix:\n", p, q, r);
    for (i = 0; i < p; i++) {
        for (j = 0; j < q; j++) {
            for (k = 0; k < r; k++) {
                scanf("%d", &a[i][j][k]);
            }
        }
    }
}
void displayMatrix(int p, int q, int r, int a[p][q][r]) {
    int i, j, k;
    printf("matrix is:\n");
    for (i = 0; i < p; i++) {
        printf("slice %d:\n", i+1);
        for (j = 0; j < q; j++) {
            for (k = 0; k < r; k++) {
                printf("%d ", a[i][j][k]);
            }
            printf("\n");
        }
        printf("\n");
    }
}
void sumMatrix(int p, int q, int r, int a[p][q][r], int b[p][q][r], int c[p][q][r]) {
    int i, j, k;
    for (i = 0; i < p; i++) {
        for (j = 0; j < q; j++) {
            for (k = 0; k < r; k++) {
                c[i][j][k] = a[i][j][k] + b[i][j][k];
            }
        }
    }
}
void transposeMatrix(int p, int q, int r, int a[p][q][r], int t[p][r][q]) {
    int i, j, k;
    for (i = 0; i < p; i++) {
        for (j = 0; j < q; j++) {
            for (k = 0; k < r; k++) {
                t[i][k][j] = a[i][j][k];   // transpose each slice
            }
        }
    }
}
void productMatrix(int p, int q, int r, int a[p][q][r], int b[p][q][r], int c[p][q][r]) {
    int i, j, k;
    for (i = 0; i < p; i++) {
        for (j = 0; j < q; j++) {
            for (k = 0; k < r; k++) {
                c[i][j][k] = a[i][j][k] * b[i][j][k]; // element-wise product
            }
        }
    }
}
int main() {
    int p, q, r, choice;
    printf("enter dimensions p q r: ");
    scanf("%d %d %d", &p, &q, &r);
    int a[p][q][r], b[p][q][r], c[p][q][r];
    printf("\nenter first matrix:\n");
    readMatrix(p, q, r, a);
    printf("enter second matrix:\n");
    readMatrix(p, q, r, b);

    do {
        printf("\nmenu:\n");
        printf("1. display matrices\n");
        printf("2. sum of matrices\n");
        printf("3. transpose first matrix\n");
        printf("4. product of matrices\n");
        printf("5. exit\n");
        printf("enter your choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                printf("\nfirst matrix:\n");
                displayMatrix(p, q, r, a);
                printf("second matrix:\n");
                displayMatrix(p, q, r, b);
                break;
            case 2:
                sumMatrix(p, q, r, a, b, c);
                printf("\nsum of matrices:\n");
                displayMatrix(p, q, r, c);
                break;
            case 3: {
                int t[p][r][q];
                transposeMatrix(p, q, r, a, t);
                printf("\ntranspose of first matrix:\n");
                int i,j,k;
                for (i = 0; i < p; i++) {
                    printf("slice %d:\n", i+1);
                    for (j = 0; j < r; j++) {
                        for (k = 0; k < q; k++) {
                            printf("%d ", t[i][j][k]);
                        }
                        printf("\n");
                    }
                    printf("\n");
                }
                break;
            }
            case 4:
                productMatrix(p, q, r, a, b, c);
                printf("\nproduct of matrices (element-wise):\n");
                displayMatrix(p, q, r, c);
                break;
            case 5:
                printf("exiting...\n");
                break;

            default:
                printf("invalid choice\n");
        }
    } while(choice != 5);
    return 0;
}
