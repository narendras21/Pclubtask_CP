# Pclubtask_CP
Problem Statement:

https://docs.google.com/document/d/1_dXRepgaFlUnYXqDP5ZWDaMLArEjA2IH_blIm2YmUiQ/edit

Answer Code:



#include<bits/stdc++.h>
using namespace std;

int main(){

    int q;
    cin>>q;

    while(q--){
        int n,m,r,l;
        cin>>n>>m>>r>>l;

        if(n%2)   // n and m are of the same parity
           cout<<"NO"<<endl;
        
        else {
            if((r == 1 && l == 2) || (r == 2 && l == 1))
                cout<<"NO"<<endl;
            else cout<<"YES"<<endl;
            
        }
   
    }
    return 0;
}

Code for test cases:


#include<bits/stdc++.h>
using namespace std;

int main(){

    int q,n,m;
    cin>>q>>n>>m;
    
    int cnt = 0;

    cout<<q<<endl;

    for(int i = 2; i<n; i++){
        for(int j = 2; j<m; j++){
            for(int k = 1; k<3; k++){
                for(int l =2; l<3; l++){

                    if(i%2){
                       if(!j%2){
                       j++;
                        cout<<i<<" "<<j<<" "<<k<<" "<<l<<endl;
                        cnt++;
                        if(cnt == q)
                           break;
                       }
                    }
                     else{
                          cout<<i<<" "<<j<<" "<<k<<" "<<l<<endl;
                         cnt++;
                         if(cnt == q)
                           break;
                    }

                }
                 if(cnt == q)
                     break;
                
            }
             if(cnt == q)
                break;

        }
         if(cnt == q)
            break;
    }

return 0;
}


