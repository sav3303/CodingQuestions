# CodingQuestions
In this repository list of coding questions will be there.


<code> class Solution {
    // Function to return the position of the first repeating element.
    public static int firstRepeated(int[] arr, int n) {
        
        HashMap<Integer, Integer> hm = new HashMap<>();
        
        for(int i=0; i<n; i++){
            
            // hm.put(arr[i] , hm.getOrDefault(arr[i], 0) + 1);
            // you can write above line also instead of below if else condition. (Please UpVote if it is helpful)
            
            if(hm.containsKey(arr[i])){
                hm.put(arr[i] , hm.get(arr[i]) + 1);
            }
            else{
                hm.put(arr[i] , 1);
            }
        }
        
        for(int i=0; i<n; i++){
            if(hm.get(arr[i]) > 1){
                return i+1;
            }
        }
        return -1;
    }
    
} </code>
