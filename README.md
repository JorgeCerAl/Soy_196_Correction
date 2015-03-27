# Soy_196_Correction

#include <string>
#include <iostream>
#include <cstdlib>
#include <sstream>
#include "BigIntegerLibrary.hh"

using namespace std;

bool is_palindrome(BigInteger n){
  return true; 

BigInteger apply196(BigInteger n){
  return n; 
}

BigInteger cagadero1(int x,int y){
	BigInteger z, u, a, i;

	i = x;
	
	for(int f = x; f <= y; f++){

		u = i;

		string ii = bigIntegerToString(i);
		reverse(ii.begin(),ii.end());
		a = stringToBigInteger(ii);
		if(a == u){

			z = z + 1;

		}
		i = i + 1;

	}
	return z;
}

	BigInteger cagadero2(int x,int y){
		BigInteger a, trys, z, i;
		BigInteger u, sum, sum2, k;
		i = x;

		for(int f = x; f <= y; f++){

			u = i;
			string ii = bigIntegerToString(i);
			reverse(ii.begin(), ii.end());
			a = stringToBigInteger(ii);

			if(a != u){
				do{

					sum = a + u;
					sum2 = sum;
					string sumsum = bigIntegerToString(sum);
					reverse(sumsum.begin(), sumsum.end());
					k = stringToBigInteger(sumsum);

					if(sum2 == k){
						z = z + 1;
						trys = 50;
					}

					else{
					trys = trys + 1;
					a = k;
					u = sum2;
					}

				}while(trys < 50);

				trys = 0;

			}
			i = i + 1;

		}
		return z;
	}

		BigInteger cagadero3(int x, int y){
			BigInteger a, trys, z, i;
			BigInteger u, sum, sum2, k;
			i = x;

			for(int f = x; f <= y; f++){

				u = i;
				string ii = bigIntegerToString(i);
				reverse(ii.begin(), ii.end());
				a = stringToBigInteger(ii);

				if(a != u){
				do{

					sum = a + u;
					sum2 = sum;
					string sumsum = bigIntegerToString(sum);
					reverse(sumsum.begin(), sumsum.end());
					k = stringToBigInteger(sumsum);

					if(sum2 == k){
						trys = 50;
					}

					else{
					trys = trys + 1;
					a = k;
					u = sum2;
					}

				}while(trys < 50);

				trys = 0;

				if (sum2 != k){
						z = z + 1;
						cout << "Lyncherel found " << f << endl;
					}
			}
			i = i + 1;


			}

			return z;
		}
 

int main() {
	int x, y;

	cout << "The lower bound of the sequence please \n";
	cin >> x;

	cout << "The upper bound of the sequence please \n";
	cin >> y;


	cout << endl;
	cout << "Between " << x << " and " << y << " you got\n";
	cout << "The number of natural palindromes is " << 	cagadero1(x,y) << endl;
	cout << "The number of non-Lycherels encountered is " << cagadero2(x,y) << endl;
	cout << cagadero3(x,y) << " number of Lycherel found" << endl;

  return 0;
}
