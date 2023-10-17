Pointers in CPP is something I've heard about a lot. Although the views were drastically diverse, something among them was the same: " Pointers are quite sh\*ty to deal with but are f\*cking cool! "; is a quote from a cool friend of mine. Now dealing with pointers might feel like collecting 200 needles from a football-sized playground while FIFA WorldCup is being played, but as soon as good understanding starts to develop, that football playground starts to shrink into a small bowl (players and crowd? let's not talk about them). So, let me try my best to make you understand these "sh\*ty to deal but f\*cking cool" pointers and use em to create miracles!

## Lets Start!

Now, if you are a bit familiar with _programming,_ you should know that we use variables to store data right? Okay, and we also know that this data is stored in memory(RAM) yep? So, these variables and data are stored in memory like people are stored in colonies/societies/cities/states/countries/continents/planets........ You got my point right? NO? okay, just like people living in a city have their own different addresses, variables too have addresses in memory. Yeah. Memory is like a city where every person(variable) living is a loner, living alone at their address.

- Variables store data.
- Data is stored in memory(RAM)
- Every variable stored has a unique address in memory.

## Pointers? The F is that?

Now that we dumbos know how lonely variables are, let's see what pointers are all about. So, Pointers are a type of variable that, like every variable, stores data. Now now, I know you might be screaming "_Sanskaari, the f\*ck bro, why you writin this whole a\*\* paragraph just to tell us another name for variables huh?_" well, Ummm. _calm the f\*ck down_. Pointers are not just any normal variable, they are special. They are different. _I wish I was....._ Pointers don't just store any data. They store **address**. **Address of another variable**! Yeah. Interesting huh?

- Pointers are a type of variable that stores other variable's address.

## Now where all the problem begins. Syntax!

Syntax is one of the things that make Pointers, well, Sh\*ty to deal with. So the infamous syntax is just like the syntax of any normal variable in CPP, but with a "\*". _Yeah, that multiply sign that half of us don't even know what it is called. Star maybe?_ Anyways. So, to declare a pointer, you need to put a "\*" in front of the variable name. It signifies that the variable declared is a pointer. Remember, that "\*" is part of syntax, not the variable name.

- Declaration of pointers includes a "\*" in front of the variable name.
- "\*" is a part of the syntax, not the variable name!

## Digging into the Syntax! Like a golddigger?

```cpp
int a = 10;
int *ptr = &a;
```

Now, for your convenience, I've written this code with a lot of effort and hard work so, thank me okay?

Jokes aside, this small block of code teaches many things. Let's break it down!

**First line**: Just the normal definition and initialization of a normal integer type variable. So nothing new.

**Second line**: Now here come some interesting parts. So, the first thing to notice is that I've given an **integer type to the pointer**. Why? Well, when declaring pointers, we need to specify the **type of the variable whose address we are gonna store** here. This is because different types of data have different storage spaces. For example, the int type takes 2 or 4 bytes of storage and char type takes 1 byte. So, if we go _evil mode_ and give char type to store int address, it'll go looking for a char where, actually, an integer is stored. So, you'll get unexpected results that _will make you rethink your life decisions (please don't do this...)_. Another thing to notice is the "&" sign in front of the variable "a". This symbol is used to get the **address** of a variable. So here "&a" actually gives the address where variable "a" is stored. You can also use "cout" to print any variable's address as shown:

```cpp
cout<<&a;
```

This will give the address of variable "a" in a **hexadecimal form**. Also, we should always assign a value to pointers since declaring a pointer with no initial value is disastrous and thus called a **wild pointer**. Still, if you want to declare a pointer with the initial value being zero, you can initialize it with NULL. Below is an example:

```cpp
int *ptr = NULL;
```

- Pointers have the same variable type as the variable whose address is being stored.
- "&a" gives the address of variable "a".
- Do not define a pointer with no initial value. Assign it NULL instead.

## Playin with pointers!

So, now that we know about pointers to some extent, we can try experimentation with them. So, let's get started!

```cpp
    int a = 10;
    int *ptr = &a;
    cout<<a<<endl;
    cout<<ptr<<endl;
    cout<<&a<<endl;
    cout<<*ptr<<endl;
```

Here, we know about the first five lines right? no? Go above and read this whole a\*\* blog again then. So, the interesting stuff starts in line 6. What would "\*ptr" do? I mean, we have already learned that putting a "\*" in front of a variable name during definition, makes it a pointer. So, what will happen if we put it again anywhere else in the code? Well, what it'll do is it will **access the value** stored at the address it is pointing to. Or, in simpler terms ( _that you obviously need_) is that "\*ptr" == "a" (**considering "ptr" is a pointer pointing to the variable "a"**). So, line 6 will print "10". Similarly, if you put "\*\*" in front of a pointer, it will again access the address of the variable it was pointing to. putting "\*\*\*" again will access the value at the address and so on..... Thus, you can put any number of "\*" in front of the pointer. If number of "\*" is even, it will access the address of the variable it is pointing to, and an odd number of "\*" will access the value at that address.

![GeeksforGeeks Zindabad!](https://media.geeksforgeeks.org/wp-content/cdn-uploads/How-Pointer-Works-In-C.png align="center")

**The image belongs GeeksforGeeks. Read their Pointers stuff as well.**

[**Pointers on GeeksforGeeks**](https://www.geeksforgeeks.org/c-pointers/)

This image shows how a pointer can be defined to access another pointer's address. Since pointers are a type of variable, they too have their own unique address.

This opens many interesting doors in programming which can be very fun but at the same time, Sh\*ty to deal with. For example, you can now change the value of a variable, declared and initialized in main() function, from any other function. Just pass it as a pointer to the function. Fun right? When I first learned it, I quickly went to try swaping two variables through a function and man I was so fascinated by this.

- "\*" in front of a pointer, allows it to access the value stored at that address.
- pointers too have their own unique address.
- pointers can be used to access another pointer's address.
- even number if "\*" is used to access the address and an odd number of "\*" is used to access the value at that address.

## Afterthought

Pointers is quite a big and interesting topic. I wanted to explain some main points here but ended up writing a huge mess. Still, I think for a newbie, it's nice writing everything you remember and learn about. It helps a lot in revising and revisiting things you've done quite some time ago. Still, I wanted to make it more organized and well-written but you know, exams a b\*tch. I hope you had fun reading this and learned something new. There are many topics I've not covered here like array pointers etc. I'll try writing it in another blog. But I think, for now, it's enough. Make sure to explore further on yourself. Theres a huge amount of info available on the internet for free. Read,write and practice. It's the best way to learn!
