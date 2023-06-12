# DAA
QUESTION FOR PRACTISE
#include <stdio.h>
FIND MIN AND MAX ELEMENT IN AN ARRAY
int main()
{
    int n , i , min , max;
    int a[10];
    printf("enter the size of an element\n");
    scanf("%d",&n);
    printf("enter an element in array: \n");
    for(i=0; i<n; i++)
    {
        scanf("%d",&a[i]);
    }
    max=a[0];
    for(i=0; i<n; i++)
    {
        if(a[i]>max)
        {
            max=a[i];
        }
        
    }
    min=a[0];
    for(i=0; i<n; i++)
    {
        if(a[i]<min)
        {
            min=a[i];
        }
    }
    printf("%d max number\n",max);
    printf("%d min number\n",min);
}
FIND SEARCH ELEMENT IN AN ARRAY
#include <stdio.h>
int main()
{
    int size , i ,flag , search;
    int a[10];
    printf("enter the size of an element\n");
    scanf("%d",&size);
    printf("enter an element in array: \n");
    for(i=0; i<size; i++)
    {
        scanf("%d",&a[i]);
    }
    printf("enter the search element\n");
    scanf("%d",&search);
    flag = 0;
    for(i=0; i<size; i++)
    {
        if(a[i]==search)
        {
            flag = 1 ; 
            break;
        }
        
    }
    if(flag == 1)
    
    {
       printf("we found the search element %d and the position is %d ", search ,i+1);
    }
    else
    printf("we dont found the search element %d",search);
    
}

const str1 = "xyab";
const str2 = "xzca";
const findUncommon = (str1 = '', str2 = '') => {
   const res = [];
   for (let i = 0; i < str1.length; i++){
      if (!(str2.includes(str1[i]))){
         res.push(str1[i])
      }
   }
   for (let i = 0; i < str2.length; i++){
      if (!(str1.includes(str2[i]))){
         res.push(str2[i])
      }
    }
    return res.join("");
};
console.log(findUncommon(str1, str2));

function differenceInMonths(date1, date2) {
    const monthDiff = date1.getMonth() - date2.getMonth();
    const yearDiff = date1.getYear() - date2.getYear();
  
    return monthDiff + yearDiff * 12;
  }
function res()
{
const str1 = prompt("enter the date1");
const str2 = prompt("enter the  date2");
  
  const date1 = new Date(str1);
  
  const date2 = new Date(str2);
  
  const difference = differenceInMonths(date1, date2);
  
  console.log(difference);
}
<?php
$target_dir = "C:/xampp/htdocs/cwharry/";
$target_file = $target_dir . basename($_FILES["file"]["name"]);

// if everything is ok, try to upload file
{
  if (move_uploaded_file($_FILES["file"]["tmp_name"], $target_file)) {
    echo "The file "." has been uploaded.";
  } else {
    echo "Sorry, there was an error uploading your file.";
  }
}

?>
