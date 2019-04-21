#include <iostream>
#include <cmath>

using namespace std;
struct Matrix{

    int*data;
    int row,col;

};

void createMatrix(int row,int col,int num[],Matrix& mat){
    mat.row=row;
    mat.col=col;
    mat.data=new int[row*col];
    for(int i=0;i<row*col;i++){
            mat.data[i]=num[i];

    }
    cout<<"creation done"<<endl;

}
Matrix operator+ (Matrix mat1, Matrix mat2){ // Add if same dimensions
    Matrix mat3;
int arr[mat1.col*mat1.row];//create a new matrix to save the result
if (mat1.col==mat2.col && mat1.row==mat2.row){ //check that they are the same dimensions
for (int i = 0 ; i <= mat1.col*mat1.row ; i++){ //loop for the whole array
arr[i]=mat1.data[i]+mat2.data[i]; //make the calculation and save the result in the new matrix
}
}
else
{
    cout<<"rows and columns must be equal to add them"<<endl;

}

createMatrix( mat1.row,mat1.col,arr,mat3);
return mat3;
}
bool  operator== (Matrix mat1, Matrix mat2){

    for(int i=0;i<(mat1.row*mat1.col);i++){
        return(mat1.data[i]==mat2.data[i]);


}
}
bool  operator!= (Matrix mat1, Matrix mat2){

    for(int i=0;i<(mat1.row*mat1.col);i++){
        return(mat1.data[i]!=mat2.data[i]);


}
}
bool   isSquare   (Matrix mat){
    return(mat.col==mat.row);


}
bool   isSymetric (Matrix mat){
    int sum1=0,sum2=0,x=0,y=0;
    int summ1[mat.row],summ2[mat.row];
    if(mat.col==mat.row){
            for(int i=0;i<mat.row;i++){
                for(int j=0;j<mat.col;j++){
                sum1+=mat.data[i*mat.col+j];


                }
                summ1[x]=sum1;
                sum1=0;
                x++;

            }
              for(int i=0;i<mat.col;i++){

                for(int j=0;j<mat.row;j++){
                        sum2+=mat.data[j*mat.row+i];

                }
                 summ2[y]=sum2;
                sum2=0;
                y++;
              }
              for(int k=0;k<mat.row;k++){
                return(summ1[k]==summ2[k]);
              }


    }


}
ostream& operator<<(ostream& out,Matrix mat){
     for(int i=0;i<mat.row;i++){
        for(int j=0;j<mat.col;j++){
            out<<mat.data[(i*mat.col)+j]<<" ";
        }
        out<<endl;
    }
    return out;


}

Matrix transpose(Matrix mat)
{
    Matrix mat1;
    int arr[mat.row*mat.col];

     for(int i=0;i<mat.col;i++){
        for(int j=0;j<mat.row;j++){
            arr[i*mat.row+j]=mat.data[j*mat.col+i];




        }
    }
    createMatrix(mat.col,mat.row,arr,mat1);

    return mat1;
}

bool   isIdentity (Matrix mat){
    bool check=true;
    if(mat.col!=mat.row){
            check=false;


    }
    else if(mat.col==mat.row){
        for(int i=0;i<mat.row;i++){
            for(int j=0;j<mat.col;j++){
                if(i==j&&mat.data[i*mat.col+j]!=1)
                    check=false;
                else if(i!=j&&mat.data[i*mat.col+j]!=0)
                    check=false;
            }
        }
    }
    return check;


}
istream& operator>> (istream& in, Matrix mat) /// Input matrix like this (dim 2 x 3) cin >> 2 3 4 6 8 9 12 123 { /// and return istream to allow cascading input

{
    cin>>mat.row>>mat.col;
    int matrix[mat.row*mat.col];


for(int i=0 ; i<mat.row*mat.col ; i++)
{

    cin>>matrix[i];

}
return in ;

}






int main()
{
    int arr1[]={1,2,3,4,5,6,7,8,9};
    int arr2[]={1,2,3,4,5,6,7,8,9};
    int arr3[]={9,10,11,4,5,6,7,8};

    Matrix mat1,mat2,mat3,mat4;

createMatrix(3,3,arr1,mat1);

createMatrix(3,3,arr2,mat2);


if(mat1==mat2){
    cout<<"true"<<endl;
}
else
    cout<<"false"<<endl;
if(mat1!=mat2){
    cout<<"true"<<endl;
}

    cout<<"false"<<endl;

if(isSquare (mat1))
    cout<<"true"<<endl;
else
    cout<<"false"<<endl;



cout<<mat1<<mat2;


cout<<transpose(mat1);



if(isSymetric (mat1)){
    cout<<"true symetric"<<endl;

}
else
    cout<<"false not symetric"<<endl;

if(isIdentity(mat1)){
    cout<<" the matrix is identity"<<endl;
}
else
     cout<<" the matrix is not identity"<<endl;
     cout<<"-----------------------"<<endl;
     mat3=mat1+mat2;
     cout<<mat3;
    cin>>mat4;
    cout<<mat4;



delete [] mat1.data;
delete [] mat2.data;
return 0;
}
