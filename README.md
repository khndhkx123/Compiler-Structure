### Project 1 : Create of C- Scanner

- 1) Modify Tiny Compiler code to scan C- Language
- 2) Using Lex(Flex) by Tiny. modificatioin

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
![Alt text](/Compiler-Structure/cp1/cp1.PNG)
