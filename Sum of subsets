#include <stdio.h>

#define MAX 100

int subset[MAX];
int n;

void findSubsets(int currentIndex, int currentSum, int targetSum) {
    if (currentSum == targetSum) {
        printf("{ ");
        for (int i = 0; i < currentIndex; i++) {
            printf("%d ", subset[i]);
        }
        printf("}\n");
        return;
    }

    if (currentIndex >= n || currentSum > targetSum) {
        return;
    }

    subset[currentIndex] = currentIndex + 1; // Assuming elements start from 1
    findSubsets(currentIndex + 1, currentSum + subset[currentIndex], targetSum);

    subset[currentIndex] = 0; // Exclude current element
    findSubsets(currentIndex + 1, currentSum, targetSum);
}

int main() {
    int targetSum;
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    printf("Enter the elements: ");
    for (int i = 0; i < n; i++) {
        scanf("%d", &subset[i]);
    }

    printf("Enter the target sum: ");
    scanf("%d", &targetSum);

    printf("Subsets with sum %d are:\n", targetSum);
    findSubsets(0, 0, targetSum);

    return 0;
}
