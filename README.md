# BANK-MANAGEMENT-SYSTEM
#include <stdio.h>
#include<string.h>
struct bank
{
    char name[100];
    long ph_no,acc_no;
    float balance,amount;
};
int main()
{
    int i,j,w,d,a,ch,c=0;
    struct bank b[10000];
    for(i=1; ;i++)
    {
        printf("Enter 1 to open an account \n");
        printf("Enter 2 to withdraw \n");
        printf("Enter 3 to deposit \n");
        printf("Enter 4 for balance enquiry \n");
        printf("Enter 5 to check details of existing customer \n");
        printf("Enter 6 to exit \n");
        printf("Enter your choice \n");
        scanf("%d",&ch);
        if(ch == 6)
          break;
        else
        {
            switch(ch)
            {
                case 1: printf("Enter the name of the customer \n");
                        gets(b[i].name);
                        printf("Enter the phone number \n");
                        scanf("%d",&(b[i].ph_no));
                        printf("Enter the amount to be deposited \n");
                        scanf("%d",&(b[i].amount));
                        b[i].balance= b[i].amount;
                        b[i].acc_no= b[i].ph_no + 1900;
                        break;
                        
                
                case 2: printf("Enter the account number \n");
                        scanf("%d",&a);
                        c=0;
                        for(j=1;j<=i;j++)
                        {
                            if(b[j].acc_no == a)
                              {
                                  printf("Enter the amount to withdraw \n");
                                  scanf("%d",&w);
                                  b[j].balance= b[j].balance - w;
                                  printf("BALANCE = %f \n",b[j].balance);
                                  c=1;
                              }
                        }      
                            if(c!=1)
                             printf("No details found \n");
                        
                        
                    break;
                case 3: printf("Enter the account number \n");
                        scanf("%d",&a);
                        c=0;
                        for(j=1;j<=i;j++)
                        {
                            if(b[j].acc_no == a)
                              {
                                  printf("Enter the amount to be deposited \n");
                                  scanf("%d",&d);
                                  b[j].balance= b[j].balance + d;
                                  printf("BALANCE = %f \n",b[j].balance);
                                  c=1;
                                  
                              }
                        }      
                            if(c!=1)
                             printf("No details found \n");
                    break;
                
                case 4: printf("Enter the account number \n");
                        scanf("%d",&a);
                        c=0;
                        for(j=1;j<=i;j++)
                        {
                            if(b[j].acc_no == a)
                              {
                                  printf("BALANCE = %f \n",b[j].balance);
                                  c=1;
                              }
                        }      
                            if(c!=1)
                             printf("No details found \n");
                    break; 
                    
                case 5: printf("Enter the account number whose detail you want to check \n");
                        scanf("%d",&a);
                        c=0;
                        for(j=1;j<=i;j++)
                        {
                            if(b[j].acc_no == a)
                              {
                                  printf("NAME : %s \n",b[j].name);
                                  printf("PHONE NUMBER : %d \n",b[j].ph_no);
                                  printf("ACCOUNT NUMBER : %d \n",b[j].acc_no);
                                  printf("BALANCE : %f \n",b[j].balance);
                              }
                        }
                        if(c!=1)
                          printf("No details found \n");
                    break;      
                default: printf("Invalid choice \n");
                
                                  
            }
        }
    }
    

    return 0;
}
