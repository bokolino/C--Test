C--Test
=======

#include <iostream>
#include <string>
#include <fstream>
#include <stdlib.h>
#include <ctime> 
#include <vector>
#include <cmath>

using namespace std;

class Calcul{
	public:

		double arie(int x, int y)
		{
			return(x*y);
		}

		double pitagora(int x, int y)
		{
			double pit = pow((double)x, 2) + pow((double)y, 2);
			double res = sqrt((double)pit);
			return(res);
		}
};


void main()
{
	int x = 0;
	int y = 0;
	Calcul calcul;
	
	cin >> x ;
	cout << x << endl;
	cin >>y;
	cout << y <<endl;

	

	double arie  = calcul.arie(x, y);
	double pit = calcul.pitagora(x, y);

	cout << "Arie este: " << arie << endl;
	cout << "Pitagora este: " << pit << endl;

	vector<double> myVector;
	myVector.push_back(arie);
	myVector.push_back(pit);

	for (unsigned i = 0; i < myVector.size(); i++)
	{
		cout << myVector[i] << " ";
	}

	ofstream outFile;
	outFile.open("Rezultate.txt");

	outFile << arie << endl;
	outFile << pit << endl;

	outFile.close();

	system ("pause");
}


