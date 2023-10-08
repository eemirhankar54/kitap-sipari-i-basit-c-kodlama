# kitap-sipari-i-basit-c-kodlama
Kitap adedine göre indirim veren basit bir öğrenme amaçlı "c" dili ile kodlanmış bir kodlamadır.




#include <stdio.h>
#include <stdlib.h>

int main()
{
 int bookprice,orderquantity;

 float discountrate,nodiscountprice,discountprice,sum;
 bookprice=20;
 orderquantity=0;

 printf("lutfen sıparıs adedını gırınız:");
 scanf("%d",&orderquantity);

 if (orderquantity>=60){
     discountrate=0.30;
}else{
    if(orderquantity>=30 && orderquantity<60){
        discountrate=0.20;
}else if (orderquantity>=10&&orderquantity<30){
        discountrate=0.12;
}else{
discountrate=0.01;
   }
}
nodiscountprice=bookprice*orderquantity;
printf("kıtabın indirimsiz tutarı: %f TL \n",nodiscountprice);
discountprice=discountrate*bookprice*orderquantity;
printf("indirim tutarı: %f TL \n",discountprice);
sum=nodiscountprice-discountprice;
printf("toplam tutar: %f TL \n",sum);

return 0;
}
