#include <omp.h>
#include <cmath>
#include <vector>
#include <iostream>

bool is_prime(int number){
    for(int i = 2; i < sqrt(number); ++i){
        if(number % i == 0){
            return 0;
        }
    }
    return 1;
}

int main(int argc, char** argv){
    int n_start = 2;
    int n_end = 50000000;
    double start, end;

    std::vector<int> primes;

    start = omp_get_wtime();
    
    for (int i = n_start; i < n_end; i++)
    {
        if(is_prime(i))
        {
            primes.push_back(i);
        }
    }

    end = omp_get_wtime();

    std::cout << end - start << "\n";
    return 0;
}
