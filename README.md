# Search-Value-in-LinkedList
public class SearchValueLL {
    public static class Node{
        int data;
        Node next;
        Node(int data)
        {
            this.data=data;
        }
    }
        public boolean SearchValue(int value,Node root)
        {
            if(root==null)
            {
                return false;
            }
            while(root!=null)
            {
                if(root.data==value)
                {
                    return true;
                }
                root=root.next;
            }
            return false;
        }
    
    public static void main(String[] args)
    {
        SearchValueLL obj=new  SearchValueLL();
        Node root=new Node(11);
        Node root1=new Node(12);
        Node root2=new Node(13);
        root.next=root1;
        root1.next=root2;
        
        System.out.println(obj.SearchValue(111,root));
        System.out.println(obj.SearchValue(11,root));
    }
    
}
