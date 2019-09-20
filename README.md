# Sequential
import java.awt.BorderLayout;
import java.util.Scanner;
import javax.swing.JOptionPane;


public class ArrayArrayArrayArrayArrayArray {

   
    public static void main(String[] args) {

        String menu = JOptionPane.showInputDialog("pilihlah :\n1.latihan praktikum\n2.tugas praktikum");
        int Option = Integer.parseInt(menu);

        if (Option == 1) {
            String menu2 = JOptionPane.showInputDialog("pilihlah :\n1.latihan praktikum 1\n2.latihan praktikum 2\n3.latihan praktikum 3\n4.latihan praktikum 4");
            int option = Integer.parseInt(menu2);

            if (option == 4) {
                ArrayArrayArrayArrayArrayArray.prak4();
            }
            if (option == 2) {
                ArrayArrayArrayArrayArrayArray.lat2();
            }
            if (option == 1) {
                ArrayArrayArrayArrayArrayArray.lat1();
            }

            if (option == 3) {
                ArrayArrayArrayArrayArrayArray.lat3();
            }

        } else if (Option == 2) {
            String menu3 = JOptionPane.showInputDialog("pilihlah :\n1.tugas praktikum 1\n2.tugas praktikum 2\n3.tugas praktikum 3\n4.tugas praktikum 4");
            int option3 = Integer.parseInt(menu3);

            if (option3 == 4) {
                ArrayArrayArrayArrayArrayArray.prak4();
            }
            if (option3 == 2) {
                ArrayArrayArrayArrayArrayArray.prak2();
            }
            if (option3 == 1) {
                ArrayArrayArrayArrayArrayArray.prak1();
            }

            if (option3 == 3) {
                ArrayArrayArrayArrayArrayArray.prak3();
            }
        }
    }

    public static void lat1() {
        String carilah;
        boolean mencari_cari = false;
        String[] Kelompok = new String[]{"Aji", "Manggala", "Rakha", "Ilham", "Iwan"};
        Scanner masukkan = new Scanner(System.in);
        System.out.println("Masukkan data yang diinginkan");
        carilah = masukkan.nextLine();
        for (int i = 0; i < Kelompok.length; i++) {
            if (carilah.equalsIgnoreCase(Kelompok[i])) {
                mencari_cari = true;
                break;
            }
        }
        if (mencari_cari == true) {
            System.out.println("Data ada");
        } else {
            System.out.println("Data tidak ada");
        }
    }

    public static void lat2() {
        int find;
        boolean ketemu = false;
        int[] nomor = new int[]{1, 2, 3, 4, 5, 6, 7, 8, 9};
        Scanner masukkan = new Scanner(System.in);
        System.out.println("Masukkan data yang diinginkan");
        find = masukkan.nextInt();
        for (int i = 0; i < nomor.length; i++) {
            if (find == nomor[i]) {
                ketemu = true;
                System.out.println("Data ketemu pas indeksnya " + i);
            }
        }
        if (ketemu == true) {
            System.out.println("Data ada");

        }
    }

    public static void lat3() {
        int besar = 0;
        int[] data = new int[]{-25, 45, 79, 14444, -140, 702};
        System.out.println("Data pada array:");
        for (int i = 0; i < data.length; i++) {
            System.out.println(data[i] + "\t");
            if (data[i] > besar) {
                besar = data[i];
            }
        }
        System.out.println("\n Data terbesar dari array adalah" + besar);

    }

    public static void lat4() {
        Scanner membaca = new Scanner(System.in);
        String mencari;
        System.out.println("Masukkan sebuah kata/kalimat: ");
        mencari = membaca.nextLine();

        int anjay = 0;
        for (int i = 0; i < mencari.length(); i++) {
            if (mencari.charAt(i) == 'a') {
                anjay++;
            }
        }
        System.out.println("Jumlah huruf a pada kalimat di atas adalah " + anjay);

    }

    public static void prak1() {
        int cari = 0;
        int bilangan;
        boolean ketemu = false;
        int data[] = {74, 98, 72, 74, 72, 90, 81, 72};
        Scanner membaca = new Scanner(System.in);
        System.out.println("data pada array:");
        for (int i = 0; i < data.length; i++) {
            System.out.print(data[i] + "\t");
        }
        System.out.println("\nmasukkan nilai yang dicari:");;
        bilangan = membaca.nextInt();
        int anjay = 0;
        for (int i = 0; i < data.length; i++) {
            if (data[i] == bilangan) {
                anjay++;
                ketemu = true;
            }
        }
        if (ketemu == true) {
            System.out.println("Data yang dicari di atas ditemukan sebanyak " + anjay + " kali");

        } else {
            System.out.println("Data tidak ditemukan!");
        }

    }

    public static void prak2() {
        double ratarata = 0.0;
        int data[] = {83, 76, 45, 90, 85, 80, 78, 74};
        System.out.println("data pada array:");
        for (int i = 0; i < data.length; i++) {
            System.out.print(data[i] + "\t");
        }
        System.out.println("");
        for (int i = 0; i < data.length; i++) {

            ratarata += data[i];
        }
        ratarata /= data.length;
        System.out.println("Rata-rata nilai array: " + ratarata);
        System.out.print("Nilai yang diatas rata-rata adalah: ");
        for (int i = 0; i < data.length; i++) {
            if (data[i] > ratarata) {
                System.out.print("\t" + data[i]);
            }
        }
        System.out.println("");

    }

    public static void prak3() {

        int data[] = {92, 96, 76, 72, 84, 101, 39};
        Scanner membaca = new Scanner(System.in);
        System.out.println("data pada array:");
        for (int i = 0; i < data.length; i++) {
            System.out.print(data[i] + "\t");
        }
        System.out.println("\nNilai yang merupakan bilangan kelipatan 3:");
        for (int i = 0; i < data.length; i++) {
            if (data[i] % 3 == 0) {
                System.out.print(data[i] + "\t");
            }
        }
    }

    public static void prak4() {

        Scanner membaca = new Scanner(System.in);
        String mencari;
        System.out.println("Masukkan sebuah kata/kalimat: ");
        mencari = membaca.nextLine();

        int hurufa = 0, hurufi = 0, hurufu = 0, hurufe = 0, hurufo = 0;
        for (int i = 0; i < mencari.length(); i++) {
            if (mencari.charAt(i) == 'a') {
                hurufa++;
            }
        }

        for (int i = 0; i < mencari.length(); i++) {
            if (mencari.charAt(i) == 'i') {
                hurufi++;
            }
        }
        for (int i = 0; i < mencari.length(); i++) {
            if (mencari.charAt(i) == 'u') {
                hurufu++;
            }
        }
        for (int i = 0; i < mencari.length(); i++) {
            if (mencari.charAt(i) == 'e') {
                hurufe++;
            }
        }
        for (int i = 0; i < mencari.length(); i++) {
            if (mencari.charAt(i) == 'o') {
                hurufo++;
            }
        }
        int semua = hurufa + hurufu + hurufe + hurufo + hurufi;
        System.out.println("Jumlah huruf a: " + hurufa);
        System.out.println("Jumlah huruf i: " + hurufi);
        System.out.println("Jumlah huruf u: " + hurufu);
        System.out.println("Jumlah huruf e: " + hurufe);
        System.out.println("Jumlah huruf o: " + hurufo);
        System.out.println("Jumlah semua huruf vokal: " + semua);
    }
}

