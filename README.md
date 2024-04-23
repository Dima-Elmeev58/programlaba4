# programlaba4
package com.company;

public class Main {
    public static void main(String[] args) {
        int[][] array = {
                {9, 8, 3},
                {2, 5, 4},
                {1, 7, 6}
        };
        sortDiagonal(array);
        for (int i = 0; i < array.length; i++) {
            for (int j = 0; j < array[i].length; j++) {
                System.out.print(array[i][j] + " ");
            }
            System.out.println();
        }
    }
    public static void sortDiagonal(int[][] array) {
        int n = array.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                if (array[i][i] > array[j][j]) {
                    int temp = array[i][i];
                    array[i][i] = array[j][j];
                    array[j][j] = temp;
                }
            }
        }
    }
}

