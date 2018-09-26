# StructExc4
Informatics Coursebook, Structure, p143

// Да се напише програма, която създава структура Book с полета title, author, price и ISBN_num, указващи заглавието на книгата,автора, цена и уникален номер на книгата. Да се въведе цяло число n и след него n на брой данни от тип Book. Да се изведат на монитора данните за книгите с цена, по-висока от предварително зададената

#include<iostream>
using namespace std;
struct Book
{
  char title[20];
  char author[20];
  double price;
  char ISBN_num[10];
};
int main()
{
	Book books[100];
	int n;
	cout<<"Br knigi=";
	cin>>n;
	for(int i=0;i<n;i++)
	{
		cout<<"Title=";
		cin>>books[i].title;
	    cin.get();
     cin.getline(books[i].title,40);
		cout<<"Author=";
    cin.get();
     cin.getline(books[i].author,40);

		cout<<"Price=";
		cin>>books[i].price;
		cout<<"ISBN=";
		cin>>books[i].ISBN_num;
	}
	double min_price;
	cout<<"min price=";
	cin>>min_price;
	for(int i=0;i<n;i++)
	{
		if(books[i].price>min_price) 
		{
		cout<<"Title="<<books[i].title<<endl;
		cout<<"Author="<<books[i].author<<endl;
		cout<<"Price="<<books[i].price<<endl;
		cout<<"ISBN="<<books[i].ISBN_num<<endl;
		}
	}
	system("pause");
	return 0;
}


