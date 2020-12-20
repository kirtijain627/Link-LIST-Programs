
#include<stdio.h>
#include<stdlib.h>
 struct node
    {
        int info;
        struct  node *plink, *flink;
    };
    struct node *head, *temp, *newnode;
    int choice = 1;
    int count;

void counts()
    {
        count = 0;
        temp = head;
    do{
        printf("%d ",temp->info);
        temp = temp->flink;
        count++;
    }while(temp!=head);
     printf("\nno. of nodes are %d",count);
     printf("\n");
    }

    void del_at_beg()

    {
        temp = head;
        if(temp->flink == head)
        {
            head == 0;

        }
        else{
                temp->plink->flink = temp->flink;
                temp->flink->plink = temp->plink;
                head = temp->flink;
        }
        free(temp);
    }

    void del_at_position()
    {
        int pos, i=1;
        printf("enter the position of element you want to delete: ");
        scanf("%d",&pos);
        if(pos<1||pos>count){
            printf("\ninvalid position");
        }
        else if(pos == 1){
            del_at_beg();
        }
        else if(pos==count){
            del_at_end();
        }
        else{
            temp = head;
            while(i<pos){
                temp = temp->flink;
                i++;
            }
            temp->plink->flink = temp->flink;
                temp->flink->plink = temp->plink;
                free(temp);
        }
    }

void del_at_end()
{
    if(temp->flink == head){
        head = 0;
    }

    else{
    temp = head;
    temp->plink->plink->flink = temp->plink->flink;
    temp->plink = temp->plink->plink->flink;}



}

void main()
{
   head = 0;
    printf("if you want to enter in list type 1 else 0: ","\n");
    scanf("%d",&choice);
    while(choice){
       newnode = (struct node *)malloc(sizeof(struct node));
       printf("enter the info :");
       scanf("%d",&newnode->info);
       if(head==0){
        head = temp = newnode;
       }
       else{
        temp->flink = newnode;
        newnode->plink = temp;
        temp = newnode;
       }
       newnode->flink = head;
       head->plink = newnode;
       printf("if you want to enter more type 1 else 0: ");
       scanf("%d",&choice);
    }
    counts();
   printf("\nenter 1 if you want to delete at beg 2 for any position and 3 for end: ");
    scanf("%d",&choice);
    if(choice == 1){
        del_at_beg();
    }
    else if(choice == 2){
        del_at_position();
    }
    else{
        del_at_end();
    }
    counts();
    printf("\nprogram finished");
}
