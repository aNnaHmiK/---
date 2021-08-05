// 알고리즘 주식가격 - 자바 풀이


class Solution {
    public int[] solution(int[] prices) {
        int[] answer = new int[prices.length];          //배열

        for(int i =0; i<prices.length;i++){
     
            int tempVal = prices[i];                   // 내가 보기 편하기 위한 초기화값 지정, 굳이 선언하지 않아도된다.     
            int intResult = 0;
            
            for(int j=i+1; j<prices.length;j++){
                if(tempVal <= prices[j]){             //true false로만 작동
                    intResult++;
                }
                else{
                    intResult++;
                    break;
                }
            }
            answer[i] = intResult ;
        }
        return answer;
    }
}
