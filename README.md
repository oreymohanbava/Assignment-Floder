# Assignment-Floder
# waveLab Coding round Exam

include <iostream>
using namespace std;
int main()
{
    int n,p;
    cin>>n;
    cin>>p;
    int a[p][2];
    for(int i=0;i<p;i++){
        cin>>a[i][0];
        cin>>a[i][1];
    }
    int b[n];
    for(int i=0;i<n;i++){
        b[i]=0;
    }
    for(int i=0;i<p;i++){
        b[a[i][0]]++;
        b[a[i][1]]++;
    }
    int s=0;
    for(int i=0;i<n;i++){
        s=s+b[i];
    }
    int z=0;
    for(int i=0;i<n;i++){
        if(b[i]==0){
            z++;
        }
    }
    int t=2*(n-2)+2;
    if(s>=t){
        cout<<z;
    }
    else{
        cout<<-1;
    }
    return 0;
}
