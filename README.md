
#include<bits/stdc++.h>
using namespace std;

class Solution
{
    public:
   
    int findMissing(int arr[], int n) 
    {
        int barr[1000003] = {0};
        for(int i=0;i<n;i++)
        {
              if(arr[i]>0)
              {
                  barr[arr[i]] = 1;
              }
        }
        for(int i=1;i<1000003;i++)
        {if(barr[i]==0)
        {
            return i;
        }
    }
    }
};


int main() { 
    int t;
    cin>>t;
    while(t--){
        int n;
        cin>>n;
        int arr[n];
        
        for(int i=0; i<n; i++)cin>>arr[i];
        
        Solution ob;
        cout<<ob.findMissing(arr, n)<<endl;
    }
    return 0; 
}   
