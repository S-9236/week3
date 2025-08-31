#include <stdio.h>
int main() {
    int MARKS[20][5];
    int i, j;
    float subAvg[5] = {0};  
    float stuAvg[20] = {0};  
    int below50 = 0;          

    // Input marks
    printf("enter marks of 20 students (5 subjects each): \n");
    for (i = 0; i < 20; i++) {
        printf("Student %d:\n",i+1);
        for (j=0;j<5;j++) {
            scanf("%d",&MARKS[i][j]);
        }
    }

    // (a) Find average marks in each subject
    for (j=0;j<5;j++) {
        int sum = 0;
        for (i=0;i<20;i++) {
            sum+=MARKS[i][j];
        }
        subAvg[j]=(float)sum/20;
    }

    // (b) Find average marks of each student
    for (i=0;i<20;i++) {
        int sum = 0;
        for (j=0;j<5;j++) {
            sum += MARKS[i][j];
        }
        stuAvg[i]=(float)sum/5;
        if(stuAvg[i]<50) {
            below50++;   // (c) count students below 50
        }
    }
    // (d) Display all student scores
    printf("\nMarks of each student:\n");
    for (i=0;i<20;i++) {
        printf("Student %d: ",i+1);
        for (j=0;j<5;j++) {
            printf("%d ",MARKS[i][j]);
        }
        printf("\n");
    }

    // Display averages
    printf("\naverage marks in each subject:\n");
    for (j=0;j<5;j++) {
        printf("subject %d: %.2f\n",j+1,subAvg[j]);
    }
    printf("\naverage marks of each student:\n");
    for (i=0;i<20;i++) {
        printf("student %d: %.2f\n",i+1,stuAvg[i]);
    }
    printf("\nNumber of students scoring below 50 on average = %d\n",below50);
    return 0;
}
