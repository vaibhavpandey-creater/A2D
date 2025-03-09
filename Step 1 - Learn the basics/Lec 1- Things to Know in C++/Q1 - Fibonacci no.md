# Question 1- Nth Fibonacci NO
## Link - https://www.naukri.com/code360/problems/nth-fibonacci-number_74156?leftPanelTabValue=PROBLEM

### Solution - 
```
#include<bits/stdc++.h>
using namespace std;
int main(){
    int n;
    cout<<"enter no"<<"/n";
        cin>>n;
        
        if (n<=2) {cout<<"1"; 
        } else {
            
            int a=1, b=1,curr= 0;
            for (int i =3; i<=n; i++){
                curr = a+b;
                a=b;
                b=curr;
            }
            cout<<curr;
        }
    return 0;
}
```