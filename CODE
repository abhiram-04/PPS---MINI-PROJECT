#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include<math.h>
int find_the_loan(int p,int t,float r){
    float a;
    a=(p*t*r/100)+p;
return a;
};
int CI(int p,int t,float r){
    float ci;
ci = p* (pow((1 + r / 100), t));
return ci;
};

int main()
{   char fname[100],lname[100];
    int  i, num,dd,mm,yy;
    char s[10],phonenumber[100],accno[100];
    float w=0;
    char yesorno[10];
    int bankno,principle,t;
    float r;

    FILE *fptr;

    printf("::: WELCOME TO OUR BANK :::\nEnter date in dd mm yy format :");
            scanf("%d %d %d",&dd,&mm,&yy);
   printf("Enter number of people: ");
   scanf("%d", &num);

   fptr = (fopen("student.txt", "a+"));
   fprintf(fptr,"\ndate : %d/%d/%d",dd, mm, yy);

   for(i = 0; i < num; ++i)
   {
      printf("\nFor person%d\nEnter first name : ", i+1);
      scanf("%s", fname);
      printf("Enter last name : ", i+1);
      scanf("%s", lname);
      printf("Enter 6 digit accno: ");goto sub;
      sub:scanf("%s", &accno);
      if (strlen(accno)!=6)
        {
          printf("plzz enter proper acc number :");goto sub;
        }
     else{
      printf("Enter your phone no. : ");goto money;
      money:scanf("%s", &phonenumber);
        if (strlen(phonenumber)!=10)
        {
          printf("plzz enter the correct number");goto money;
        }
        else{
          
       
      

      
      printf("Do you want any loan :(y/n)");
      scanf("%s",yesorno);
        if (yesorno[0]=='y')
      {
     
        printf("what kind of loan do u want choose the particular number\n1.House Loan\n2.Car Loan\n3.property Loan\n4.Student Loan\n5.Small Business Loan\n6.Home innovation loans\n7.Agriculture loans\n8.Gold Loan\n9.Personal loan\n10.credit card loan\n11.Payday loan\nPlease enter your requirement :");
        goto banks;
        banks: scanf("%d",&bankno);
        

        switch(bankno){
            case 1: r=8.65;
                break;  
            case 2: r=10.75;
                break;        
            case 3: r=9.35;
                break;  
            case 4: r=15.5;
                break;        
            case 5: r=13.0;
                break;  
            case 6: r=8.0;
                break;        
            case 7: r=7.5;
                break;  
            case 8: r=8.4;
                break;        
            case 9: r=9.0;
                break;  
            case 10: r=11.30;
                break;        
            case 11: r=7.5;
                break;  
           
            default: printf("please choose apropriate number  :");goto banks;
                break;  
        }

        printf("\nNote: if your required amount is more than 10lakh \nthen the intrest will be shifted to compound intrest.\nEnter the amount :");scanf("%d",&principle);
        printf("Enter the time in year :");scanf("%d",&t);
    //printf("%.2f",r);
    if(principle<1000000){
        w=find_the_loan(principle,t,r);
        printf("\n The amount you need to pay in total by the end of your term : %.2f",w);}
       
    else{
       w=CI(principle,t,r);
        printf("\n The amount you need to pay in total by the end of your term : %.2f",w);}
        
    }
    else{
        printf("No problem ur loan amount will be zero");
        w=0;
    }
    fprintf(fptr,"\naccountno. :%d\nName: %s %s \nYour Phone number=%d \nloan :%.2f\n",accno, fname,lname, phonenumber, w);
   } }}






   fclose(fptr);
   
    return 0;



}
