# StructExc4
Informatics Coursebook, Structure, p143

#include<iostream>
#include <iomanip>
using namespace std;
struct Book
{
    char title[40];
    char author[40];
    double price;
    char ISBN_num[25];
};
int main()
{
    int n, minPrice;
    cin>>n;
    Book books[n];
    for(int i=0;i<n;i++)
    {
        cout<<"BOOK "<<i+1<<endl;
        cout<<"Title: ";
        cin>>books[i].title;
        cout<<"Author: "<<endl;
        cin.get();
        cin.getline(books[i].author,40);
        cout<<"Price: ";
        cin>>books[i].price;
        cout<<"ISBN_num: ";
        cin>>books[i].ISBN_num;
    }
    cin>>minPrice;
    for(int i=0;i<26;i++)
    {
        if(books[i].price>minPrice)
        {
            cout << std::setiosflags(std::ios::left);
            cout<<setw(20)<<books[i].title;
            cout<<setw(20)<<books[i].author;
            cout<<setw(20)<<books[i].price;
            cout<<setw(20)<<books[i].ISBN_num<<endl;
        }
    }
}
