# longest-prefi
class Solution{
  public:
    string longestCommonPrefix (string arr[], int N)
    {
        // your code here
    sort(arr,arr+N);
    string str=arr[0];
    string str2=arr[N-1];
    string ans;
    int size1=str.size();
    int size2=str2.size();
    int p1=0;
    int p2=0;
   while(p1<size1 && p2<size2){
       if(str[p1]==str2[p2])
       {
           ans.push_back(str[p1]);
           
       }
       else{
           break;
           p1++;
           p2++;
       }
   }
   if(ans.size()==0)
       return "-1";
   else
    return ans;
    }
};
