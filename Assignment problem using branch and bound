#include <stdio.h>
#include <stdbool.h>

#define N 4

// Function to find the minimum element in a matrix
int findMin(int matrix[N][N], bool rowCovered[N], bool colCovered[N]) {
    int minVal = 999999;  // Initialize with a large value
    for (int i = 0; i < N; i++) {
        if (!rowCovered[i]) {
            for (int j = 0; j < N; j++) {
                if (!colCovered[j] && matrix[i][j] < minVal) {
                    minVal = matrix[i][j];
                }
            }
        }
    }
    return minVal;
}

// Function to recursively solve the assignment problem
void solveAssignment(int matrix[N][N], bool rowCovered[N], bool colCovered[N], int cost, int level, int *minCost) {
    if (level == N) {
        if (cost < *minCost) {
            *minCost = cost;
        }
        return;
    }

    for (int i = 0; i < N; i++) {
        if (!rowCovered[i]) {
            rowCovered[i] = true;
            for (int j = 0; j < N; j++) {
                if (!colCovered[j]) {
                    colCovered[j] = true;
                    int minVal = findMin(matrix, rowCovered, colCovered);
                    int newCost = cost + matrix[i][j] - minVal;
                    if (newCost + (N - level - 1) * minVal < *minCost) {
                        solveAssignment(matrix, rowCovered, colCovered, newCost, level + 1, minCost);
                    }
                    colCovered[j] = false;
                }
            }
            rowCovered[i] = false;
        }
    }
}

int main() {
    int matrix[N][N] = {{10, 2, 8, 11},
                        {15, 6, 12, 7},
                        {8, 10, 6, 9},
                        {12, 9, 14, 6}};

    bool rowCovered[N] = {false};
    bool colCovered[N] = {false};
    int minCost = 999999;

    solveAssignment(matrix, rowCovered, colCovered, 0, 0, &minCost);

    printf("Minimum cost: %d\n", minCost);

    return 0;
}
