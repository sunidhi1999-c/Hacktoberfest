#include <stdio.h>
#include <stdlib.h>
struct node
{
    int info;
    struct node*link;
};
typedef struct node* NODE;
NODE getnode()
{
    NODE x;
    x=(NODE)malloc(sizeof(struct node))
    ;
    if(x==NULL)
    {
        printf("Memory is not available");
    }
    return(x);
}
void freenode(NODE x)
{
    free(x);
}
NODE insert_front(int item,NODE first)
{
    NODE temp;
    temp=getnode()
    ;
    temp->info=item;
    temp->link=first;
    return(temp);
}
NODE delete_front(NODE first)
{
    NODE temp;
    if(first==NULL)
    {
        printf("List is empty\n");
        return;
    }
    temp=first;
    temp=temp->link;
    printf("deleted=%d",first->info);
    freenode(first);
    return(temp);

}
void display(NODE first)
{
    NODE temp;
    if(first==NULL)
    {
        printf("contents are empty");
        return;
    }
    printf("Contents of list are\n");
    temp=first;
    while(temp!=NULL)
    {
        printf("%d",temp->info);
        temp=temp->link;
    }
    printf("\n");
}
int main()
{
    int choice,item;
    NODE first=NULL;
    for(;;)
    {
        printf("Enter ur choice 1.insert_front 2.delete_front 3.display 4.exit");
        scanf("%d",&choice);
        switch(choice)
        {
            case 1:printf("Enter item");
            scanf("%d",&item);
            first=insert_front(item,first);
            break;
            case 2:delete_front(first);
            break;
            case 3 :display(first);
            break;
            case 4:exit(0);

        }
    }
    printf("Hello world!\n");
    return 0;
}
