# dsa10
# bineary search
#  Minimum Difference Element in a Sorted Array


public class Main
{
    static int bs ( int arr[], int key)
    {
        int l=0;
	    int h=arr.length-1;
	    int min=-1;
	    while(l<=h)
	    {
	        int mid=(l+h)/2;
	        if(arr[mid]==key)
	        {
	            return arr[mid];
	        }
	        else if(arr[mid]<key)
	        {
	            l=mid+1;
	        }
	        else
	        h=mid-1;
	    } 
	   int a=Math.abs(arr[h]-key);
	   int b=Math.abs(arr[l]-key);
	   if(a>b)
	   return b;
	   return a;
    }
	public static void main(String[] args) 
	{
	    int arr[]={1,2,5,7,11,15,17};
	    int key=12;
	    int ans = bs (arr,key);
	    System.out.println(ans);
	}
}
