#include <stdio.h>
struct Item {
    int weight;
    int value;
};
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            double ratio1 = (double)items[i].value / items[i].weight;
            double ratio2 = (double)items[j].value / items[j].weight;
            if (ratio1 < ratio2) {
                struct Item temp = items[i];
                items[i] = items[j];
                items[j] = temp;
            }
        }
    }

 
    int currentWeight = 0;
    int totalValue = 0;

    for (int i = 0; i < n; i++) {
        if (currentWeight + items[i].weight <= containerCapacity) {
            currentWeight += items[i].weight;
            totalValue += items[i].value;
            printf("Item %d added.\n", i + 1);
        }
    }

    printf("Total value packed: %d\n", totalValue);
}

int main() {
    int containerCapacity = 50;
    struct Item items[] = {
        {10, 60},
        {20, 100},
        {30, 120}
    };
    int n = sizeof(items) / sizeof(items[0]);

    containerLoading(items, n, containerCapacity);

    return 0;
}
