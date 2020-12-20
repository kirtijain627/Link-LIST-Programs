#include<stdio.h>
#include<stdlib.h>
struct node

    int info;
    struct node *flink, *plink;
};
struct node *head=0, *temp, *newnode;
int counts;
void count()
{
    counts = 0;
    temp = head;
     while(temp!=0){
        printf("%d ",temp->info);
        counts++;
        temp = temp->flink;
     }
     printf("\ntotal no. of nodes are %d",counts);
     printf("\n");
}


void deletion_at_beg()
{
    if(head==0){
        printf("list is empty\n");
    }
    else{
            temp = head;
          head = head->flink;
    head->plink = 0;
    free(temp);
    }
}


void deletion_at_any_pos()
{
    int i=1,pos;
    printf("\neneter the position of element you want to delete: ");
    scanf("%d",&pos);
    if(pos<1||pos>counts){
        printf("\ninvalid position");
    }
    else if(pos==1){
        deletion_at_beg();
    }
    else if(pos==counts){
        deletion_at_end();
    }

    else{
            temp = head;
    while(i<pos){
        temp = temp->flink;
        i++;
    }
    if(temp == head){
        head = 0;
    }
    else{
    temp->plink->flink = temp->flink;
    temp->flink->plink = temp->plink;
    free(temp);
    }
    }
}



void deletion_at_end()
{
    if(head==0){
        printf("list is empty\n");
    }
    else{
        temp = head;
        while(temp->flink!=0){
            temp = temp->flink;
        }
        if(temp == head){
            head = 0;
        }
        else{
        temp->plink->flink = 0;
        free(temp);
        }
    }

}

void main()
{

    int ch;
    int choice =1;
    printf("do you want to enter type 0 or 1: ");
    scanf("%d",&choice);
    if(choice==0){
        printf("list is empty\n");
        exit(0);
    }
    else{
    while(choice){
        newnode = (struct node *)malloc(sizeof(struct node));
        printf("enter the data: ","\n");
        scanf("%d",&newnode->info);
        newnode->plink=0;
        newnode->flink = 0;
        if(head==0){
            head = temp = newnode;
        }
        else{
            temp->flink = newnode;
            newnode->plink = temp;
            temp = newnode;
        }
        printf("do you want to enter type 0 or 1: ");
        scanf("%d",&choice);
     }
     count();
    }
    printf("if you want to delete from beg enetr 1 any position enter 2 or for end enter 3: ");
    scanf("%d",&ch);
     if(ch==1){
        deletion_at_beg();
        count();
}
else if(ch==2){
    deletion_at_any_pos();
    count();
}
else {
    deletion_at_end();
    count();
}
printf("\nprogram finished");
}
