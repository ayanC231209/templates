void sprime(int n, vi& a){
 
int prime[3000]={0};
 
for(int i=2;i*i<=n;i++){
    if(prime[i]==0){
        for(int j=i*i;j<=n;j+=i){
            prime[j]=1;
        }
    }
}
for(int i=2;i<=n;i++){
    if(prime[i]==0){
       a.pb(i);
    }
}
}
