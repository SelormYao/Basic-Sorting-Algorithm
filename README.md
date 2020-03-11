# Basic-Sorting-Algorithm
Sorting Techniques


#include<iostream>

using namespace std;

int main()
{
	//SELECTION SORT
    // declaring variables
    int i,j,n,loc,tem,minim;
    cout<<"Input the number of elements:";
    cin>>n;
    cout<<"\nEnter the elements of the array\n";

    int A[n];
    for(i=0;i<n;i++)
    {
        cin>>A[i];
    }

    for(i=0;i<n-1;i++)
    {
        minim=A[i];
        loc=i;
        for(j=i+1;j<n;j++)
        {
            if(minim>A[j])
            {
                minim=A[j];
                loc=j;
            }
        }

        tem=A[i];
        A[i]=A[loc];
        A[loc]=tem;
    }

    cout<<"\nSorted list is as follows\n";
    for(i=0;i<n;i++)
    {
        cout<<A[i]<<" ";
    }

    return 0;
}





#include<iostream>
using namespace std;

int main(){
	//BUBBLE SORT
  //declaring array
  int A[9];
  cout<<"kindly input 9 elements "<<endl;
  for(int i=0; i<9; i++)
  {
    cin>>A[i];
  }
  cout<<endl;


  // Bubble Sort
  int temp;
  for(int i=0; i<=8; i++)
  {
    for(int j=0; j<8; j++)
    {

      if(A[j]>A[j+1])
      {
        temp=A[j];
        A[j]=A[j+1];
        A[j+1]=temp;
      }
    }
  }

  cout<<"Array after sorting is "<<endl;
  for(int i=0; i<9; i++)
  {
    cout<<A[i]<<" ";
  }
  return 0;
}
