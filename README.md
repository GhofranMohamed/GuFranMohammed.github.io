//************* & operator ***********
//When & is placed in front of a name during a variable declaration, that
// means that a "reference to" is being declared.

          int x;
          int& y = x ;
          x = 10 ;
          cout<< y << endl;
//the output will be the value of x "10" .

          int var ;
          int *ptr;
          ptr = &var ;
          var = "Gufran" ;
 //the output will be the value of var "Gufran" .

// putting & in front of a variable name denotes "address of" in C++.

            int a ;
            cout<< &a << endl ;

//the result of the above expression is an r-value address of a.

//The & (bitwise AND) in C or C++ takes two numbers as operands
//and does AND on every bit of two numbers.
//The result of AND is 1 only if both bits are 1. 


            // a = 5(00000101), b = 9(00001001)
            int a = 5, b = 9;
            cout << (a & b) << endl;

//the result is (00000001) = 1 .


//**********const key word ************ 

//when declaring a const variable this means it can't be modified.

                int const x = 5;
                     or
                const int x = 4;
//pointers can be declared as const in two ways
//1 can't modify what is pointed to.

                const int *p_int;
//2 can't modify the data pointed to .

                int x;
                int * const p_int = &x;
//we can use const functions to let the compiler that it's safe to call it from a const object
//it won't make any changes

                int val = x ; 
                int getValue() const {
                    return val; }
//Const iterators are the as regular one, but you can't modify the underlying date .

                std::vector<int> vec;
                vec.push_back( 3 );
                vec.push_back( 4 );
                vec.push_back( 8 );

                for ( std::vector<int>::const_iterator itr = vec.begin(), end = vec.end();
                itr != end;
                     ++itr )
                    {
                       // just print out the values...
                std::cout<< *itr <<std::endl;
                     }
//const cast to pass a const variable to a non const function .

                int fun(int* ptr)
               {
                return (*ptr + 10);
               }

               int main(void)
               {
               const int val = 10;
               const int *ptr = &val;
               int *ptr1 = const_cast <int *>(ptr);
               cout << fun(ptr1);
               return 0;
               }

