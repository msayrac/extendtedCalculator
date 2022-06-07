# extendtedCalculator
import java.util.Scanner;

public class Main {
    static int sum(int a, int b) {
        int result = a + b;
        System.out.println("Toplam : " + result);
        return result;
    }

    static int minus(int a, int b) {
        int result = a - b;

        System.out.println("Cikarma :" + result);
        return result;
    }

    static int times(int a, int b) {
        int result = a * b;
        System.out.println("Carpma : " + result);
        return result;
    }

    static double divide(double a, double b) {
        if (b == 0) {
            System.out.println("ikinci sayi 0'dan farklı olmalidir");
            return 0;
        }
        double result = a / b;
        System.out.println("Bolme : " + result);
        return result;
    }


    static int power(int a, int b) {
        int result = 1;
        for (int i = 1; i <= b; i++) {
            result = result * a;
        }
        System.out.println("Us alma : " + result);
        return result;
    }

    static int mod(int a, int b) {
        int result = a % b;
        System.out.println("mod : " + result);
        return result;
    }

    static void calc(int a, int b) {
        System.out.println("Ceversi : " + (2 * (a + b)));
        System.out.println("Alani : " + a * b);
    }

    public static void main(String[] args) {

        Scanner scan = new Scanner(System.in);

        int select;

        String menu = "1-Toplama\n"
                + "2-Cikarma\n"
                + "3-Carpma\n"
                + "4-Bolme\n"
                + "5-Uslu Sayi Hesaplama\n"
                + "6-Mod Alma\n"
                + "7-Dikdortgen Alan ve Cevre Hesabi"
                + "0-Cikis yap";
        while (true) {
            System.out.println(menu);
            System.out.println("Bir islem seciniz : ");
            select = scan.nextInt();

            if (select == 0) {
                break;
            }
            System.out.println("İlk sayiyi giriniz : ");
            int a = scan.nextInt();
            System.out.println("İkinci sayiyi giriniz : ");
            int b = scan.nextInt();


            switch (select) {
                case 1:
                    sum(a, b);
                    break;
                case 2:
                    minus(a, b);
                    break;
                case 3:
                    times(a, b);
                    break;
                case 4:
                    divide(a, b);
                    break;
                case 5:
                    power(a, b);
                    break;
                case 6:
                    mod(a, b);
                    break;
                case 7:
                    calc(a, b);
                    break;

                default:
                    System.out.println("1-7 arasi secim yapiniz");
            }

        }
        System.out.println("Gule GUle");

    }
}
