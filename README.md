# Angela_Anticaps_Problem.c
//This is My First Github Program

#include<stdio.h>
#include<string.h>
int main(){
    char A[10000];    //A+Angela's input
    int i,c=0;    //c=checker value
    scanf("%[^\t]",&A);

    for(i=0;i<strlen(A);i++){
        if(c==0){
            if(A[i]>='A' && A[i]<='Z'){
                printf("%c",A[i]);
                c=1;
            continue;
            }
            else{
                printf("%c",A[i]);
            }
        }

        if(c==1){
            if(A[i]>='A' && A[i]<='Z'){
                A[i]=A[i]+32;
                printf("%c",A[i]);
            }
            else if(A[i]=='.' || A[i]=='!' || A[i]=='?'){
                printf("%c",A[i]);
                c=0;
            }
            else{
                printf("%c",A[i]);
            }
        }
    }

return 0;
}
