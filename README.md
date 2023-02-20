# linked_list_cpp
#include<bits/stdc++.h>
using namespace std;


void Takeinput(){
    #ifndef ONLINE_JUDGE
    freopen("input.txt","r",stdin);
    freopen("output.txt","w",stdout);
    #endif
}
class LinkedList{
public:
    struct Node{
        int data;
        Node *next;
        Node(int val){
            data=val;
            next=NULL;
        }
    };
    Node *head;
    Node *tail;
    LinkedList(){
        head=NULL;
        tail=NULL;
    }
    void Insert(int x){
        //creating new node 10,NULL---30,NULL
        Node *newNode=new Node(x);//new keyword is used for space
        if(head==NULL){
            head=newNode;
            tail=newNode;
            return;
        }
        tail->next=newNode;
        tail=tail->next;
       

    }
    void Printdata(){
        Node *temp=head;
        while(temp){
            cout<<temp->data<<" ";
            temp=temp->next;
        }
    }
 
};
int main(){
    Takeinput();
    LinkedList list;
    list.Insert(10);
    list.Insert(20);
    list.Insert(30);
    //insert at begin
    //insert at end
    //insert in middle
    list.Printdata();

}
