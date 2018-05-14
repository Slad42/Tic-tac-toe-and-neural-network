package tictactoe;
 
import java.util.Scanner;
 
public class tictactoe {
 
    private static int[][] gameField = new int[3][3]; // -1 is o, 0 is void, 1 is x
    private static boolean[][] probabilityField = new boolean[3][3]; // false is there is probability to put something
                                                                        // in
                                                                        // this cell; true is conversely
 
    static Scanner sc = new Scanner(System.in);
 
    private static void clrscr() {
        for (int clear = 0; clear < 100; clear++) {
            System.out.println();
        }
    }
 
    private static void printField() {
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                if (gameField[i][j] == -1)
                    System.out.print("O");
                if (gameField[i][j] == 0)
                    System.out.print("*");
                if (gameField[i][j] == 1)
                    System.out.print("X");
            }
            System.out.println();
        }
    }
 
    private static boolean checkInput(int x, int y) {
        return ((x < 3 && x > -1 && y < 3 && y > -1) && !probabilityField[x][y]);
    }
 
    private static void playing() { // player is X //It doesnt work
        int x, y;
        int i = 0;
        while (i < 5) {
            printField();
            x = sc.nextInt();
            y = sc.nextInt();
            if (checkInput(x, y)) {
                gameField[x][y] = 1;
                probabilityField[x][y] = true;
                clrscr();
                i++;
                // now it is AI's step
                boolean flag = true;
                while (flag) {
                    x = (int) Math.round(Math.random() * 2);
                    y = (int) Math.round(Math.random() * 2);
                    if (checkInput(x, y)) {
                        flag = false;
                    }
                    gameField[x][y] = -1;
                    probabilityField[x][y] = true;
                }
                clrscr();
            } else {
                clrscr();
                System.out.println("try again, pls");
            }
 
        }
 
    }
 
    public static void main(String[] args) {
        playing();
    }
}
