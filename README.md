package Biblioteca;

import java.util.ArrayList;
import java.util.Scanner;

public class principal {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        ArrayList<Livro> livros = new ArrayList<>();

        int opcao;

        do {

            System.out.println("\n=== SISTEMA BIBLIOTECA ===");
            System.out.println("1 - Cadastrar livro");
            System.out.println("2 - Listar livros");
            System.out.println("3 - Sair");

            System.out.print("Escolha: ");
            opcao = scanner.nextInt();
            scanner.nextLine();

            if (opcao == 1) {

                Livro livro = new Livro();

                System.out.print("Título: ");
                livro.titulo = scanner.nextLine();

                System.out.print("Autor: ");
                livro.autor = scanner.nextLine();

                livros.add(livro);

                System.out.println("Livro cadastrado!");

            }

            else if (opcao == 2) {

                for (Livro l : livros) {

                    System.out.println("Título: " + l.titulo);
                    System.out.println("Autor: " + l.autor);
                    System.out.println("----------------");

                }

            }

        } while (opcao != 3);

        scanner.close();

    }

}
