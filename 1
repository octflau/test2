#include <iostream>
#include <mpi.h>
#include <stdio.h>
#include <stdlib.h>
#include <cmath>
#include <cstdlib>
#include <ctime>
#include <random>
#include <fstream>
using namespace std;
 
#define MAX_N 10
#define MAX_RAND_VALUE 10
 
int world_rank;
int world_size;
 
long long int A[MAX_N][MAX_N], A1[MAX_N][MAX_N], A2[MAX_N][MAX_N], B2[MAX_N][MAX_N], C2[MAX_N][MAX_N], Y3[MAX_N][MAX_N], Y3SQ[MAX_N][MAX_N], y1y2t[MAX_N][MAX_N], y1tY3SQy1PLy2PLy1y2t[MAX_N][MAX_N];
long long int b[MAX_N], b1[MAX_N], c1[MAX_N];
long long int vec_y1[MAX_N], vec_2b1PL3c1[MAX_N], vec_y2[MAX_N], vec_Y3SQy1[MAX_N], vec_Y3SQy1PLy2[MAX_N];
long long int y1tY3SQy1PLy2;
 
void Init_Matrix_Random(long long int matrix[MAX_N][MAX_N], int n)
{
	//srand((unsigned int)time(0));					// встановлюємо seed для генератора випадкових чисел
	long long int lower_bound = 1;					// нижня межа діапазону
	long long int upper_bound = MAX_RAND_VALUE;		// верхня межа діапазону
 
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			matrix[i][j] = (rand() % (upper_bound - lower_bound + 1) + lower_bound);
		}
	}
}
 
void Init_Vect_Random(long long int vect[MAX_N], int n)
{
	//srand((unsigned int)time(0));					// встановлюємо seed для генератора випадкових чисел
	long long int lower_bound = 1;					// нижня межа діапазону
	long long int upper_bound = MAX_RAND_VALUE;		// верхня межа діапазону
 
	for (int i = 0; i < n; i++) 
	{
		vect[i] = (rand() % (upper_bound - lower_bound + 1) + lower_bound);
	}
}
 
void Init_Matrix_Keyboard(long long int matrix[MAX_N][MAX_N], int n, const char title[])
{
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			cout << title << "[" << i << "][" << j << "]: ";
			cin >> matrix[i][j];
		}
	}
}
 
void Init_Vect_Keyboard(long long int vect[MAX_N], int n, const char title[])
{
	for (int i = 0; i < n; i++)
	{
		cout << title << "[" << i << "]: ";
		cin >> vect[i];
	}
}
 
void Init_Matrix_Ones(long long int matrix[MAX_N][MAX_N], int n)
{
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			matrix[i][j] = 1;
		}
	}
}
 
void Init_Vect_Ones(long long int vect[MAX_N], int n)
{
	for (int i = 0; i < n; i++)
	{
		vect[i] = 1;
	}
}
 
 
void Calculate_b(long long int vect[MAX_N], int n)
{
	for (int i = 0; i < n; i++) 
	{
		vect[i] = 8/i;
	}
}
 
void Calculate_C2(long long int matrix[MAX_N][MAX_N], int n)
{
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			matrix[i][j] = 1 / (i+j+2);
		}
	}
}
 
void Mul_Matrix_By_Vector(long long int matrix[MAX_N][MAX_N], long long int vect[MAX_N], long long int result[MAX_N], int n)
{
	for (int i = 0; i < n; i++) 
	{
		result[i] = 0;
		for (int j = 0; j < n; j++) 
		{
			result[i] += matrix[i][j] * vect[j];
		}
	}
}
 
void Mul_Vector_By_Number(long long int vect[MAX_N], long long int mulnumber, int n)
{
	for (int i = 0; i < n; i++)
	{
		vect[i] = vect[i] * mulnumber;
	}
}
 
void Substract_Vectors(long long int vect1[MAX_N], long long int vect2[MAX_N], long long int result[MAX_N], int n)
{
	for (int i = 0; i < n; i++) 
	{
		result[i] = vect1[i] - vect2[i];
	}
}
 
void Substract_Matrix(long long int matrix1[MAX_N][MAX_N], long long int matrix2[MAX_N][MAX_N], long long int result[MAX_N][MAX_N], int  n)
{
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			result[i][j] = matrix1[i][j] - matrix2[i][j];
		}
	}
}
 
void Mul_Matrix_By_Matrix(long long int matrix1[MAX_N][MAX_N], long long int matrix2[MAX_N][MAX_N], long long int result[MAX_N][MAX_N], int  n)
{
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			result[i][j] = 0;
			for (int k = 0; k < n; k++) 
			{
				result[i][j] += matrix1[i][k] * matrix2[k][j];
			}
		}
	}
}
 
void Mul_Vector_By_Transposed_Vector(long long int vect1[MAX_N], long long int vect2[MAX_N], long long int result[MAX_N][MAX_N], int n)
{
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			result[i][j] = vect1[i] * vect2[j];
		}
	}
}
 
void Add_Vectors(long long int vect1[MAX_N], long long int vect2[MAX_N], long long int result[MAX_N], int n)
{
	for (int i = 0; i < n; i++) 
	{
		result[i] = vect1[i] + vect2[i];
	}
}
 
long long int Mul_Transposed_Vector_By_Vector(long long int vect1[MAX_N], long long int vect2[MAX_N], long long int result, int n)
{
	result = 0;
	for (int i = 0; i < n; i++)
	{
		//cout << vect1[i] << " " << vect2[i];
		result += vect1[i] * vect2[i];
		//cout << endl << result << endl;
	}
	return result;
}
 
void Mul_Matrix_By_Number(long long int matrix[MAX_N][MAX_N], long long int mulnum, long long int result[MAX_N][MAX_N], int  n)
{
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			result[i][j] = matrix[i][j] * mulnum;
		}
	}
}
 
void Add_Matrix(long long int matrix1[MAX_N][MAX_N], long long int matrix2[MAX_N][MAX_N], long long int result[MAX_N][MAX_N], int  n)
{
	for (int i = 0; i < n; i++) 
	{
		for (int j = 0; j < n; j++) 
		{
			result[i][j] = matrix1[i][j] + matrix2[i][j];
		}
	}
}
 
 
 
int main(int argc, char** argv)
{
	MPI_Init(NULL, NULL);
	MPI_Comm_rank(MPI_COMM_WORLD, &world_rank);
	MPI_Comm_size(MPI_COMM_WORLD, &world_size);
 
	if (world_size != 4)
	{
		cout << "World size must be equal to 4 for " << argv[0] << endl;
		MPI_Finalize();
		return 1;
	}
 
 
	ofstream proc0file;
	ofstream proc1file;
	ofstream proc2file;
	ofstream proc3file;
 
 
	//назва файлу для запису 
	proc0file.open("process0.txt");
	proc1file.open("process1.txt");
	proc2file.open("process2.txt");
	proc3file.open("process3.txt");
 
 
 
	if (world_rank == 0)
	{
		int n, mode;
		cout << "Enter n: ";
		cin >> n;
		if (n < 1 || n > MAX_N)
		{
			cout << "Invalid input, n = MAX_N selected automatically \n";
			n = MAX_N;
		}
 
		cout << "Enter mode: \n";
		cout << "1 - keyboard \n" ;
		cout << "2 - random numbers \n";
		cout << "3 - ones \n";
		cin >> mode;
 
		if (mode < 1 || mode > 3) 
		{ 
			cout << "Invalid input, mode 3 selected automatically \n";
			mode = 3;
		}
 
		if (mode == 1)
		{
			Init_Matrix_Keyboard(A, n, "A");
			Init_Matrix_Keyboard(A1, n, "A1");
			Init_Matrix_Keyboard(A2, n, "A2");
			Init_Matrix_Keyboard(B2, n, "B2");
			Init_Vect_Keyboard(b1, n, "b1");
			Init_Vect_Keyboard(c1, n, "c1");
		}
		else if (mode == 2)
		{
			srand((unsigned int)time(0));
			Init_Matrix_Random(A, n);
			Init_Matrix_Random(A1, n);
			Init_Matrix_Random(A2, n);
			Init_Matrix_Random(B2, n);
			Init_Vect_Random(b1, n);
			Init_Vect_Random(c1, n);
		}
		else
		{
			Init_Matrix_Ones(A, n);
			Init_Matrix_Ones(A1, n);
			Init_Matrix_Ones(A2, n);
			Init_Matrix_Ones(B2, n);
			Init_Vect_Ones(b1, n);
			Init_Vect_Ones(c1, n);
		}
 
 
		Calculate_b(b, n);
		MPI_Send(&n, 1, MPI_INT, 1, 0, MPI_COMM_WORLD);
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Send(&A[i][j], 1, MPI_LONG_LONG_INT, 1, 0, MPI_COMM_WORLD);
			}
		}
		MPI_Send(b, MAX_N, MPI_LONG_LONG_INT, 1, 0, MPI_COMM_WORLD);
 
 
		/*MPI_Send(&n, 1, MPI_INT, 2, 0, MPI_COMM_WORLD);
		for (int i = 0; i < n; i++) 
		{
			for (int j = 0; j < n; j++) 
			{
				MPI_Send(&A1[i][j], 1, MPI_LONG_LONG_INT, 2, 0, MPI_COMM_WORLD);
			}
		}
		MPI_Send(b1, MAX_N, MPI_LONG_LONG_INT, 2, 0, MPI_COMM_WORLD);
		MPI_Send(c1, MAX_N, MPI_LONG_LONG_INT, 2, 0, MPI_COMM_WORLD);*/
 
 
		/*Calculate_C2(C2, n);
		MPI_Send(&n, 1, MPI_INT, 3, 0, MPI_COMM_WORLD);*/
		/*for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Send(&A2[i][j], 1, MPI_LONG_LONG_INT, 3, 0, MPI_COMM_WORLD);
			}
		}
 
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Send(&B2[i][j], 1, MPI_LONG_LONG_INT, 3, 0, MPI_COMM_WORLD);
			}
		}
 
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Send(&C2[i][j], 1, MPI_LONG_LONG_INT, 3, 0, MPI_COMM_WORLD);
			}
		}*/
 
 
 
	}
	else if (world_rank == 1) 
	{
		int n;
 
		MPI_Recv(&n, 1, MPI_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Recv(&A[i][j], 1, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}
		MPI_Recv(b, MAX_N, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
 
		proc1file << "A:" << endl;
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				proc1file << A[i][j] << "\t";
			}
			proc1file << endl;
		}proc1file << endl;
 
 
		proc1file << "b:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc1file << b[i] << " " << endl;
		}
		proc1file << endl << endl;
 
 
 
		Mul_Matrix_By_Vector(A, b, vec_y1, n);
		proc1file << "y1:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc1file << vec_y1[i] << " " << endl;
		}
		proc1file << endl << endl;
		//
		/*MPI_Recv(vec_y2, MAX_N, MPI_LONG_LONG_INT, 2, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
 
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Recv(&Y3[i][j], 1, MPI_LONG_LONG_INT, 3, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}
 
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Recv(&Y3SQ[i][j], 1, MPI_LONG_LONG_INT, 3, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}*/
 
	//	proc1file << "Received:" << endl;
 
	//	proc1file << "y2:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		proc1file << vec_y2[i] << " " << endl;
	//	}
	//	proc1file << endl << endl;
 
	//	proc1file << "Y3:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		for (int j = 0; j < n; j++)
	//		{
	//			proc1file << Y3[i][j] << "\t";
	//		}
	//		proc1file << endl;
	//	}
	//	proc1file << endl;
 
	//	proc1file << "Y3^2:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		for (int j = 0; j < n; j++)
	//		{
	//			proc1file << Y3SQ[i][j] << "\t";
	//		}
	//		proc1file << endl;
	//	}
	//	proc1file << endl;
 
	//	Mul_Vector_By_Transposed_Vector(vec_y1, vec_y2, y1y2t, n);
	//	proc1file << "y1*y2t:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		for (int j = 0; j < n; j++)
	//		{
	//			proc1file << y1y2t[i][j] << "\t";
	//		}
	//		proc1file << endl;
	//	}
	//	proc1file << endl;
	//	
	//	Mul_Matrix_By_Vector(Y3SQ, vec_y1, vec_Y3SQy1, n);
	//	proc1file << "Y3SQ*y1:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		proc1file << vec_Y3SQy1[i] << " " << endl;
	//	}
	//	proc1file << endl << endl;
 
	//	Add_Vectors(vec_Y3SQy1, vec_y2, vec_Y3SQy1PLy2, n);
	//	proc1file << "Y3SQ*y1 + y2:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		proc1file << vec_Y3SQy1PLy2[i] << " " << endl;
	//	}
	//	proc1file << endl << endl;
 
	//	y1tY3SQy1PLy2 = Mul_Transposed_Vector_By_Vector(vec_y1, vec_Y3SQy1PLy2, y1tY3SQy1PLy2, n);
	//	proc1file << "y1t * (Y3SQ*y1 + y2):" << endl;
	//	proc1file << y1tY3SQy1PLy2 << endl;
	//	proc1file << endl << endl;
 
	//	Mul_Matrix_By_Number(Y3, y1tY3SQy1PLy2, Y3, n);
	//	proc1file << "(y1t * (Y3SQ*y1 + y2)) * Y3:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		for (int j = 0; j < n; j++)
	//		{
	//			proc1file << Y3[i][j] << "\t";
	//		}
	//		proc1file << endl;
	//	}
	//	proc1file << endl;
 
	//	Add_Matrix(Y3, y1y2t, y1tY3SQy1PLy2PLy1y2t, n);
	//	proc1file << "((y1t * (Y3SQ*y1 + y2)) * Y3) + y1*y2t:" << endl;
	//	for (int i = 0; i < n; i++)
	//	{
	//		for (int j = 0; j < n; j++)
	//		{
	//			proc1file << y1tY3SQy1PLy2PLy1y2t[i][j] << "\t";
	//		}
	//		proc1file << endl;
	//	}
	//	proc1file << endl;
 
 
 
	}
	else if (world_rank == 2)
	{
		/*int n;
		MPI_Recv(&n, 1, MPI_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
		for (int i = 0; i < n; i++) 
		{
			for (int j = 0; j < n; j++) 
			{
				MPI_Recv(&A1[i][j], 1, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}
		MPI_Recv(b1, MAX_N, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
		MPI_Recv(c1, MAX_N, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
 
		proc2file << "A1:" << endl;
		for (int i = 0; i < n; i++) 
		{
			for (int j = 0; j < n; j++) 
			{
				proc2file << A1[i][j] << "\t";
			}
			proc2file << endl;
		}proc2file << endl;
 
 
		proc2file << "b1:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc2file << b1[i] << " " << endl;
		}
		proc2file << endl << endl;
 
 
		proc2file << "c1:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc2file << c1[i] << " " << endl;
		}
		proc2file << endl << endl;
 
 
		Mul_Vector_By_Number(b1, 2, n);
		proc2file << "2b1:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc2file << b1[i] << " " << endl;
		}
		proc2file << endl << endl;
 
		Mul_Vector_By_Number(c1, 3, n);
		proc2file << "3c1:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc2file << c1[i] << " " << endl;
		}
		proc2file << endl << endl;
 
		Add_Vectors(b1, c1, vec_2b1PL3c1, n);
 
		proc2file << "2b1 + 3c1:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc2file << vec_2b1PL3c1[i] << " " << endl;
		}
		proc2file << endl << endl;
 
		Mul_Matrix_By_Vector(A1, vec_2b1PL3c1, vec_y2, n);
		proc2file << "y2:" << endl;
		for (int i = 0; i < n; i++)
		{
			proc2file << vec_y2[i] << " " << endl;
		}
		proc2file << endl << endl;*/
 
		//MPI_Send(vec_y2, MAX_N, MPI_LONG_LONG_INT, 1, 0, MPI_COMM_WORLD);
 
	}
	else
	{
		/*int n;
		MPI_Recv(&n, 1, MPI_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);*/
		/*for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Recv(&A2[i][j], 1, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Recv(&B2[i][j], 1, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}
		for (int i = 0; i < n; i++)
		{
			for (int j = 0; j < n; j++)
			{
				MPI_Recv(&C2[i][j], 1, MPI_LONG_LONG_INT, 0, 0, MPI_COMM_WORLD, MPI_STATUS_IGNORE);
			}
		}*/
 
		//proc3file << "A2:" << endl;
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		proc3file << A2[i][j] << "\t";
		//	}
		//	proc3file << endl;
		//}
		//proc3file << endl;
 
		//proc3file << "B2:" << endl;
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		proc3file << B2[i][j] << "\t";
		//	}
		//	proc3file << endl;
		//}
		//proc3file << endl;
 
		//proc3file << "C2:" << endl;
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		proc3file << C2[i][j] << "\t";
		//	}
		//	proc3file << endl;
		//}
		//proc3file << endl;
 
		////рахуємо
		//Substract_Matrix(B2, C2, B2, n);
		//proc3file << "B2 - C2:" << endl;
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		proc3file << B2[i][j] << "\t";
		//	}
		//	proc3file << endl;
		//}
		//proc3file << endl;
 
		//Mul_Matrix_By_Matrix(A2, B2, Y3, n);
		//proc3file << "Y3:" << endl;
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		proc3file << Y3[i][j] << "\t";
		//	}
		//	proc3file << endl;
		//}
		//proc3file << endl;
 
		//Mul_Matrix_By_Matrix(Y3, Y3, Y3SQ, n);
		//proc3file << "Y3^2:" << endl;
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		proc3file << Y3SQ[i][j] << "\t";
		//	}
		//	proc3file << endl;
		//}
		//proc3file << endl;
 
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		MPI_Send(&Y3[i][j], 1, MPI_LONG_LONG_INT, 1, 0, MPI_COMM_WORLD);
		//	}
		//}
 
		//for (int i = 0; i < n; i++)
		//{
		//	for (int j = 0; j < n; j++)
		//	{
		//		MPI_Send(&Y3SQ[i][j], 1, MPI_LONG_LONG_INT, 1, 0, MPI_COMM_WORLD);
		//	}
		//}
 
	}
 
 
 
	MPI_Finalize();
	return 0;
 
 
 
 
 
}
