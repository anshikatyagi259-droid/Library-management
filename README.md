import java.util.ArrayList;
import java.util.Scanner;

// Class to represent a Book
class Book {
    int id;
    String title;
    String author;
    boolean isIssued;

    public Book(int id, String title, String author) {
        this.id = id;
        this.title = title;
        this.author = author;
        this.isIssued = false;
    }
}

// Main Library Management System Class
public class LibraryManagementSystem {

    static ArrayList<Book> books = new ArrayList<>();
    static Scanner sc = new Scanner(System.in);

    public static void main(String[] args) {
        // Sample books
        books.add(new Book(1, "Java Programming", "Author A"));
        books.add(new Book(2, "Python Programming", "Author B"));
        books.add(new Book(3, "C Programming", "Author C"));

        int choice;
        do {
            System.out.println("\n--- Library Management System ---");
            System.out.println("1. View all books");
            System.out.println("2. Issue a book");
            System.out.println("3. Return a book");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            switch(choice) {
