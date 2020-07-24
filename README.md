# Maximum-value-pair

package maxpairsum;
import java.util.*;
 
 public class Maxpairsum
 {
   
     int arr[], N;
    Maxpairsum()//Default Constructor
    {
        arr=new int[0];
         N=0;
    } 
     
     
     
    void LargestSumPair() 
    { 
         
   Scanner sc=new Scanner(System.in);
        System.out.println("Enter size of matrix.");
        N=sc.nextInt();
   
     arr=new int[N]; 
      
        for(int i=0;i<N;i++)
        {
            arr[i]=sc.nextInt();
             
        }
        
        // Initialize first and second largest element 
        int first, second; 
        if (arr[0] > arr[1]) 
        { 
            first = arr[0]; 
            second = arr[1]; 
        } 
        else
        { 
            first = arr[1]; 
            second = arr[0]; 
        } 
       
        // Traverse remaining array and find first and second largest 
        // elements in overall array 
      
        for (int i = 2; i<arr.length; i ++) 
        { 
            /* If current element is greater than first then update both 
              first and second */
            if (arr[i] > first) 
            { 
                second = first; 
                first = arr[i]; 
            } 
       
            /* If arr[i] is in between first and second then update second  */
            else if (arr[i] > second && arr[i] != first) 
                second = arr[i]; 
        } 
        System.out.println("Max pair sum is: "+(first + second)); 
      
    } 
     
    public static void main(String[] args)  
    { 
         Maxpairsum obj=new Maxpairsum(); 
      obj.LargestSumPair(); 
          
    } 

 }

    
    

