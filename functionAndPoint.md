## 函数指针和指针函数 ##

1. 函数是函数,指针是指针. 函数根据==返回值的不同==,可以分为==不同函数==, 指针根据==指向类型的不同==,也可以分为==很多种指针==.
2. 有的函数返回值是一个 int, 有的返回值是一个  char , 同样,有的函数==返回值是一个指针==.这就是==指针函数==.
3. 有的指针指向 int:(int* p), 有的指针指向char:(char *p), 同样,有的指针指向 *函数* : void (*f)(int), ==指向函数的指针==就叫==函数指针==.
4. 指针函数: int \*f(int);    //函数名字叫f
    函数指针: int (\*f)(int);    //指针名字叫f
5. 函数指针中, 前 () 改变了*的优选级,所以两个()可以说是函数指针的标志.
6. void fun(int a){ return a;}
     void (\*f)(int) = fun;    ||    void (\*f)(int) = &fun;  //两种函数指针的赋值方法
7. int x = (\*f)(30);    || int x = fun(30);    //两种函数指针的使用方法 