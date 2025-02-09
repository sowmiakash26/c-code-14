#include<stdio.h>
void rev(int *arr, int size){
   int *start = arr, *end = arr+size-1;
   while(start<end){
      int temp = *start;
      *start = *end;
      *end = temp;
      start++;
      temp--;
   }
   return 0;
}
int main(){
   int arr[]={1,2,3,4,5,6};
   int size=sizeof(arr)/sizeof(arr[0]);
   printf("Original array : \n");
   for(int i=0;i<size;i++){
      printf("%d",arr[i]);
   }
   rev(arr,size);
   printf("\nReversed array : \n");
   for(int i=0;i<size;i++){
      printf("%d",arr[i]);
   }
   return 0;
}
