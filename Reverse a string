#include <stdio.h>
#include <string.h>

int main() {
    char input[100];
    printf("Enter a string: ");
    scanf("%s", input);

    int length = strlen(input);
    char reversed[length + 1];

    for (int i = 0; i < length; i++) {
        reversed[i] = input[length - i - 1];
    }
    reversed[length] = '\0';

    printf("Reversed string: %s\n", reversed);

    return 0;
}
