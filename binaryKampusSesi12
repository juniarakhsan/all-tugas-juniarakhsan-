public class binarykampus {
    public static void main(String[] args) {
        int[] arr = {24,54,87,56,84,98,67,75,43,49,64,67,93,43}; 
        bubbleSort(arr);
        System.out.print("data yang telah di sorting = ");
        for (int i : arr) {
            System.out.print(i +" " );
        }
        int key = 56;
        long startTimeBinary = System.nanoTime();
        int hasilCariBinary = binarySearch(arr,key);
        long endTimeBinary = System.nanoTime();
        long subTimeBinary = endTimeBinary - startTimeBinary;

        if (hasilCariBinary == -1) {
            System.out.println("array tidak ditemukan");
        }else{
            System.out.println("\nhasil array binary search di temukan di index = "+ hasilCariBinary);   
        }
        
        System.out.println("Hasil waktu dari binary search = "+subTimeBinary + " nano second" );

        long startTimeLinear = System.nanoTime();
        int hasilCariLinear = linearSearch(arr,key);
        long endTimeLinear = System.nanoTime();
        long subTimeLinear = endTimeLinear - startTimeLinear;


        if (hasilCariLinear == -1) {
            System.out.println("array tidak ditemukan");
        }else{
            System.out.println("hasil cari linear search di temukan di index = "+ hasilCariLinear);   
        }
        
        System.out.println("Hasil waktu dari linear search = "+subTimeLinear + " nano second" );

    }

    static void bubbleSort(int array[]) {
        int size = array.length;
        
        // loop to access each array element
        for (int i = 0; i < (size-1); i++) {
          // check if swapping occurs
          boolean swapped = false;
          // loop to compare adjacent elements
          for (int j = 0; j < (size-i-1); j++) {
    
            // compare two array elements
            // change > to < to sort in descending order
            if (array[j] > array[j + 1]) {
    
              // swapping occurs if elements
              // are not in the intended order
              int temp = array[j];
              array[j] = array[j + 1];
              array[j + 1] = temp;
              
              swapped = true;
            }
          }
          // no swapping means the array is already sorted
          // so no need for further comparison
          if (!swapped)
            break;
    
        }
      }


    static int binarySearch(int[] arr,int key){
        int low = 0;
        int high = arr.length - 1;

        while(low <= high){
            int mid = (low + high) / 2 ;

            if(arr[mid] == key){
                return mid;
            }

            if(arr[mid] < key){
                low = mid + 1;
            }else{
                high = mid - 1;
            }
        }
    
        return -1;
    }

    static int linearSearch(int[] arr,int key) {
        for (int i = 0; i < arr.length; i++) {
            if(arr[i] == key){
                return i;
            }
        }
        return -1;
    }

}
