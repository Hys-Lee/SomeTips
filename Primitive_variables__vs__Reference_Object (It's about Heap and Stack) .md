If confusing, think about relation about "Pointer" in C (or C++);

First of all, "substitute" means kind of a variable and related object are the same.

Primitive variables are like integers or characters in C.
They can be "substituted" in variables.
And they cannot be changed and remain in memory if something like garbage collector doesn't delete them.
In case where we operating them like below,
'''
int a=0;
a++;
'''
there are 0.
And 'a++' means a=a+1 And a+1 = 2 so, there 2 appear in memory and, a = 2 .

However, Reference Objects are like object pointed by a variable in C
The variable has(is substituted) the address to the related object which is in memory(more precisely, in stack)
For example, Array or Class are such type.


But if you know precisely, should also about Heap and Stack

Local variables are stored in Stack with their data
And each data related each local variables are different each other as I said above
It's important that the Stack store data types with fixed size like int, char, float etc...
Those types have fixed size in complie time

In contrast, the Heap store data types with non-fixed size like class etc
And their size are set in run time.
So for using these types, we need pointing variable like in C.
these variable has the addresses for those data types.

Now let's think about difference between C++(C),Java and Python,Javascript

In Javascript or Python, we use variable with no datatype.
That means every variables are determined their data size in run time.(I think)
But the data themselves like integer(number) might be in the Stack because they have fixed size when they are called unlike their variables.
In Javascript, so, the Object type is mutable. we can edit their properties. It's the same situation about class in Python(or C++ or Java)

the String type is different on language about how to treat.
In Javascript, the String is immutable type. The data appear in the Stack space whenever they are called.
But in other language (maybe Python? I don't remember in other language srr) the String is mutable type.
You can check whether they are immutable or not by changing one letter from the String data like doing str[0]='a'

If knowing more precisely I'm gonna edit this.
hope this might help.

/*
스택에 데이터랑 같이 들어가는데 이때 데이터는 서로 다른 것들이지 예를들어서
int a=2;
int b=2;
면 이 때 두개의 2는 서로 다른 메모리위치에 존재하지.
아무튼 중요한 것인 이렇게 변수와 그 값이 같이 stack에 존재한다는 것.
그리고 가장 중요한 것이 이런 원시변수들이 stack에 존재한다
int char같은 데이터 타입은 크기가 고정되어 있음
stack은 이런 고정된 데이터타입을 저장한다. (컴파일 타임에 크기가 결정되어서 그런 듯)

반대로 heap은 그렇지 않은 타입을 저장한다. (런타임에 크기가 결정되어서 그런 듯)
예를 들어 array(동적으로 만들어 진 것 생각하면 될 듯)나 class같은 것처럼.
따라서 이 친구들은 포인터의 개념으로 이들을 가리키는 변수가 필요한 것임. (이 포인팅 하는 친구는 주소를 저장하니 일정한 크기안에서 해결가능->stack에 있을 듯[?])

그럼 이제 String에 대해서 생각해보자
C++,Java에서랑 Javascript나 Python에서 느낌이 다른 것 같은데, 특히 뒤의 둘은 변수 선언시 데이터타입을 지정하지 않자너[?]
*/


