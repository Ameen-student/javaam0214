import java.util.ArrayList;
import java.util.Scanner;

class Book {
    int id;
    String title;
    String author;
    boolean isIssued;

    Book(int id, String title, String author) {
        this.id = id;
        this.title = title;
        this.author = author;
        this.isIssued = false;
    }

    @Override
    public String toString() {
        return "Book ID: " + id + ", Title: " + title + ", Author: " + author + ", Issued: " + isIssued;
    }
}

public class LibraryManagementSystem {
    private ArrayList<Book> books = new ArrayList<>();
    private Scanner scanner = new Scanner(System.in);

    public void addBook() {
        System.out.print("Enter Book ID: ");
        int id = scanner.nextInt();
        scanner.nextLine();
        System.out.print("Enter Book Title: ");
        String title = scanner.nextLine();
        System.out.print("Enter Book Author: ");
        String author = scanner.nextLine();
        books.add(new Book(id, title, author));
        System.out.println("Book added successfully!");
    }

    public void issueBook() {
        System.out.print("Enter Book ID to issue: ");
        int id = scanner.nextInt();
        for (Book book : books) {
            if (book.id == id) {
                if (!book.isIssued) {
                    book.isIssued = true;
                    System.out.println("Book issued successfully!");
                } else {
                    System.out.println("Book is already issued!");
                }
                return;
            }
        }
        System.out.println("Book not found!");
    }

    public void viewBooks() {
        System.out.println("Library Books:");
        for (Book book : books) {
            System.out.println(book);
        }
    }

    public void menu() {
        while (true) {
            System.out.println("\n1. Add Book");
            System.out.println("2. Issue Book");
            System.out.println("3. View Books");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");
            int choice = scanner.nextInt();
            switch (choice) {
                case 1 -> addBook();
                case 2 -> issueBook();
                case 3 -> viewBooks();
                case 4 -> {
                    System.out.println("Exiting...");
                    return;
                }
                default -> System.out.println("Invalid choice! Try again.");
            }
        }
    }

    public static void main(String[] args) {
        LibraryManagementSystem library = new LibraryManagementSystem();
        library.menu();
    }
}
