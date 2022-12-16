package ru.mirea.task15;

import java.io.*;
import java.nio.file.Files;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.Scanner;

public class FileWork {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        File newFile = new File("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt", "Task15.txt");
        if (newFile.exists())
            System.out.println("Файл успешно создан");

        System.out.println("Введите что-либо в файл: ");
        String sometext = sc.nextLine();
        try(FileWriter writer = new FileWriter("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt", true)) {
            writer.write(sometext);
            writer.close();
        }
        catch(IOException ex)
        {
            System.out.println(ex.getMessage());
        }

        System.out.println("Ваш файл: ");
        try(FileReader reader1 = new FileReader("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt")) {
            int c;
            while((c=reader1.read())!=-1)
                System.out.print((char)c);
            reader1.close();
        }
        catch(IOException ex)
        {
            System.out.println(ex.getMessage());
        }
        System.out.println();

        String s, newS;
        String buf= "";
        try(FileReader reader2 = new FileReader("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt"))
        {
            List<String> fl;
            System.out.println("На что нужно заменить файл: ");
            newS = sc.nextLine();
            fl = Arrays.asList(newS);
            Files.write(newFile.toPath(), fl);
            reader2.close();
        }
        catch(IOException ex)
        {
            System.out.println(ex.getMessage());
        }

        System.out.println();
        System.out.println("Ваш файл: ");
        try(FileReader reader3 = new FileReader("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt")) {
            int c;
            while((c=reader3.read())!=-1)
                System.out.print((char)c);
            reader3.close();
        }
        catch(IOException ex)
        {
            System.out.println(ex.getMessage());
        }
        System.out.println();

        try(FileWriter writer = new FileWriter("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt", true)) {
            System.out.println("Введите данные в конец файла");
            s = sc.nextLine();
            writer.write(s);
            writer.close();
        }
        catch(IOException ex)
        {
            System.out.println(ex.getMessage());
        }

        System.out.println();
        System.out.println("Ваш файл: ");
        try(FileReader reader4 = new FileReader("C:\\Users\\maryi\\Desktop\\JAVA\\JavaMirea\\src\\ru\\mirea\\task15\\file.txt")) {
            int c;
            while((c=reader4.read())!=-1)
                System.out.print((char)c);
            reader4.close();
        }
        catch(IOException ex)
        {
            System.out.println(ex.getMessage());
        }
    }


}
