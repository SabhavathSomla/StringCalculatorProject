class NegativeException extends Exception{
	public NegativeException(String str){
    	super(str);
    }
}

public class StringCalculator {

  public static int add(String numbers)  {
    int sum = 0;
    try{
      if(numbers==""){
        return 0;
      }
      if(numbers.charAt(0)=='/' && numbers.charAt(1)=='/' && numbers.charAt(3)== '\n'){
        char newDelimiter = numbers.charAt(2);
        numbers = numbers.substring(4);
        numbers = numbers.replace(newDelimiter, ',');
      }
      numbers = numbers.replace('\n', ',');
      String[] arr =numbers.split(",");
      for(int i=0;i<arr.length;i++){
        int val=Integer.parseInt(arr[i]);
        if(val<0){
          throw new NegativeException("Negatives not allowed: "+arr[i]);
        }
        sum = sum+val;
      }
     } catch(NegativeException ne){
     	  System.out.print(ne+" => ");
     }
    return sum;
  }
  
  public static void main(String[] args) {
    System.out.println(add(""));
    System.out.println(add("2\n3,4,5,6"));
    System.out.println(add("//;\n1;2"));
    System.out.println(add("//;\n1;-2"));
  }
}
