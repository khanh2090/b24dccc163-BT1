class Book {
    public String title;
    public String author;
    public int year;
    static int count = 0;

    public Book(String title, String author, int year) {
        this.title = title;
        this.author = author;
        this.year = year;
        count++;
    }

    public void display() {
        System.out.println("Title: " + title + ", Author: " + author + ", Year: " + year);
    }
}

class Library {
    java.util.ArrayList<Book> books = new java.util.ArrayList<>();

    public void addBook(Book book) {
        books.add(book);
    }

    public void showBooks() {
        for (Book book : books) {
            book.display();
        }
        System.out.println(Book.count);
    }
}
public class Main {
    public static void main(String[] args) {
        Library library = new Library();
        Book b1 = new Book("De Men", "Tô Hoài", 1941);
        Book b2 = new Book("Sach Kinh Te", "Rosie Nguyễn", 2016);
        Book b3 = new Book("Harry Potter", "J.K. Rowling", 1997);
        library.addBook(b1);
        library.addBook(b2);
        library.addBook(b3);
        library.showBooks();
    }
}
