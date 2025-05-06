#include<bits/stdc++.h>
#include<stdlib.h>
#define MAX 10
int stack1 [MAX];
int top=-1;
void push(int value){
if(top == MAX -1){
    printf("Error:Stack overflow!\n");
}
else{
    top++;
    stack1[top]=value;
}

}
int pop(){
if(top ==-1){
        printf("Error:Stack underflow!\n");
return -1;

}
top --;
return stack1[top+1];
}
int main(){
int choice,value;
while(1){
    printf("1.Push\n2.pop\n3.Exit\n");
    printf("enter your choice: ");
    scanf("%d",&choice);
    switch (choice){
case 1:
    printf("Enter value to push:");
    scanf("%d",&value);
    push(value);
    break;
case 2:
    value = pop();
    if(value!=-1){
        printf("Popped value:%d\n",value);
    }
    break;
case 3:

exit(0);
    default :
    printf("Invalid choice!\n");
    }
}
return 0;
}
