#include<stdio.h>
#include<stdlib.h>


    struct node
    {
        int info;
        struct node *plink, *flink;
    };
    struct node *head=0, *newnode, *temp=0, *loc;
    int count, choice = 1;
    void counts(){
    temp = head;
    count = 0;
    while(temp!=0){
        printf("%d ",temp->info);
        count++;
        temp = temp->flink;
    }
    printf("no. of nodes are %d",count);
    }
    void main(){
    printf("enter a sorted list:");
    while(choice){
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("enter the info: ");
        scanf("%d",&newnode->info);
        if(head==0){
            head = temp = newnode;
            newnode->plink = 0;
        }
        else{
            temp->flink = newnode;
            newnode->plink = temp;
            temp = newnode;
        }
        printf("\ndo you want to cintinue type 0 or 1: ","\n");
        scanf("%d",&choice);
    }
    temp->flink = 0;
    counts();

 printf("\nenter value for insertion: ");
       newnode = (struct node *)malloc(sizeof(struct node));
       printf("enter the value: ");
       scanf("%d",&newnode->info);
       newnode->flink = 0;
       newnode->plink = 0;
       temp = head;
       if(newnode->info<head->info){
        newnode->flink = head;
        head = newnode;
       }
       else{


        while(temp!=0&&newnode->info>temp->info){

           loc = temp;
            temp = temp->flink;

        }
        if(temp==0){
            loc->flink = newnode;
            newnode->plink = loc;
        }
        else{
       newnode->flink = temp;
       temp->plink->flink = newnode;
       newnode->plink = temp->plink;
       temp->plink = newnode;
       }

    }
    counts();
       printf("\nprogram finished");
    }

