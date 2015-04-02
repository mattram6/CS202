#include <stdlib.h>
#include <stdio.h>
#include <string.h>

using namespace std;




struct student
{
char* name;
float grade;
};


void get_average(student *s, int size)
{
float av = 0, sum = 0;

	for( int i = 0; i < size; i++)
	{
	sum += s[i].grade;
	}

av = sum/size;
FILE *f = fopen("Out.txt", "w");
fprintf( f, "The average grade is: %f", av);
printf("Output file is created!!\n");


}


int main(int argc, char* argv[])
{
char* file_name = argv[1];
int size = atoi (argv[2]); // convert string to integer
student stud[size];
FILE *fl = fopen( file_name, "r");


	for(int i = 0; i < size; i++)
	{
	stud[i].name = new char[30];
	fscanf( fl, "%s%f", stud[i].name, &(stud[i].grade));
	printf( "Name: %s Grade: %f\n",stud[i].name, (stud[i].grade));
	}
get_average(stud, size);




return 0;
}
