class Solution {
    public int numberOfBeams(String[] bank) {
        int res = 0;
        int prevcnt = 0;

        for(String row : bank){
            int currcnt = 0;
            for(char ch : row.toCharArray()){
                if(ch == '1'){
                    currcnt++;
                }
            }
            if(currcnt > 0){
            res += prevcnt * currcnt;
            prevcnt = currcnt;
            }
        }
        return res;
    }
}
