# Book-
My first repository on github

package Java_101;
public class Book {
    // This is the Auther name related to te book
    public String auther;
    // This is the name of the book 
    public String name;
    //This is publish date of the book
    public int pubdate;
    //this is  the current state of the boook
    public boolean is_open;
    //This current opened page 
    public int current_page;
    //This is sthe number of the book pages
    public int last_page_number;
    //This is the Instructor method
    public Book(String a, String n, int pdate,int lpage)
    {
        this.auther=a;
        this.name=n;
        this.pubdate=pdate;
        this.is_open= false;
        this.last_page_number=lpage;
    }
    //This method is used for openning the book
    void OpenBook()
    {
        if(is_open)
            System.out.println("itis opened");
        else 
            is_open=true;
    }
    /*
    This method is used to close the book
    */
    void CloseBook()
    {
        if(is_open)
            this.is_open=true;
        else
            System.out.println("Itis Cllosed");
    }
    /*
    This method is used to move to specific page 
    */
    void MoveToBage(int page )
    {
        if(!is_open)
            System.out.println("Open The Book First");
        if(page<1 || page>last_page_number)
            System.out.println("Erorr : Choose a page inside the book");
        if(is_open)
            System.out.println("Here we are ");
    }
    //This is the book information
    void BookInformation()
    {
        if(is_open){
        System.out.println("Book Auther is : "+this.auther);
        System.out.println("Book name is : "+this.name);
        System.out.println("Book pubdate is : "+this.pubdate);
        System.out.println("Book end page is : "+this.last_page_number +" page");
        }
        else
            System.out.println("Open the book first");
    }    
}
    public static void main(String[] args) {
        Book The_way_to_Success=new Book("Moaaz","The way to Success",2023,500);
        Book C_plus_plus=new Book("Moaaz Ahmed","C++",2018,870);
        StrOp  Str=new StrOp(The_way_to_Success.auther);
        
        The_way_to_Success.OpenBook();
        The_way_to_Success.BookInformation();
        The_way_to_Success.CloseBook();
        System.out.println("------------------------");
        C_plus_plus.OpenBook();
        C_plus_plus.BookInformation();
        C_plus_plus.CloseBook();
    }        

}
