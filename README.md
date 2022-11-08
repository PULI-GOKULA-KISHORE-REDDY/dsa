# dsa


class Solution {
  public static int divide(int A, int B) {
      /* write your solution here */
      boolean sign=(A>=0 == B>=0)? true:false;
      A=Math.abs(A);
      B=Math.abs(B);
      int result=0;
      while(A-B >=0)
      {
          int count=0;
          while(A-(B<<1<<count) >=0)
          {
              count++;
          }
          result+=1<<count;
          A-=B<<count;
          //System.out.println(A+"-"+B+" result-"+result);
      }
      return sign? result:-result;
  }
}
