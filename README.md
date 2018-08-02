### Project 1 : Create of C- Scanner

- Modify Tiny Compiler code to scan C- Language
- Using Lex(Flex) by Tiny. modificatioin

#### Implement of C-Scanner

     /*program to perform Euclid's
	 Algorithm to computer gcd*/
	 
	int gcd (int u, int v)
	{
		if (v == 0) return u;
		else return gcd(v,u-u/v*v);
		/* u-u/v*v == u mod v */
	}

	void main(void)
	{
    	int x; int y;
    	x = input(); y = input();
    	output(gcd(x,y));
	}

#### Final Result of Project1
![Final Result](https://github.com/khndhkx123/Compiler-Structure/blob/master/cp1/cp1.PNG)


### Project 2 : Create of C- Parser

- Implement the parser using Yacc(bison)
- Create Syntax Tree

#### Implement of C-Scanner

     /*program to perform Euclid's
	 Algorithm to computer gcd*/
	 
	int gcd (int u, int v)
	{
		if (v == 0) return u;
		else return gcd(v,u-u/v*v);
		/* u-u/v*v == u mod v */
	}

	void main(void)
	{
    	int x; int y;
    	x = input(); y = input();
    	output(gcd(x,y));
	}

#### Final Result of Project2
