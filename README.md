#include<stdio.h>

int main(void)

{

    unsigned long long int m,n,rem_m,rem_n,carry_op=0, sum,count;
    while((scanf("%llu %llu",&m,&n))==2)
    {
        if (m==0 && n==0)
        {
            break;
        }
        count =0;

        while(m!=0 || n!=0)
        {
                rem_m=m%10;
                rem_n=n%10;
                if(carry_op==1)
                {
                    rem_m++;
                }
                sum = rem_m+rem_n;
                if(sum>=10)
                {
                    count++;
                    carry_op++;
                }
                m=m/10;
                n=n/10;
            }
            carry_op = 0;

            if(count==0)
            {
                printf("No carry operation.\n");
            }
            else
            {
                printf("%llu carry operations.\n",count);
            }





    return 0;
    }
}

