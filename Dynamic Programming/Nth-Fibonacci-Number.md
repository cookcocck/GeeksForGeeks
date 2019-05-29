# Nth Fibonacci Number

#include <stdio.h>
    #include <vector>
    
    std::vector<long long int> fibonacci(1001);
    
    void getFibo(int n) {
        fibonacci[0] = 0, fibonacci[1] = 1;
        for (int i = 2; i < n; ++i) {
            fibonacci[i] = (fibonacci[i - 2] + fibonacci[i - 1]) % 1000000007;
        }
    }
    
    
    int main() {
    		// 提前计算好
        getFibo(1001);
        int t = 0, n = 0;
        scanf("%d", &t);
        while (t--) {
            scanf("%d", &n);
            printf("%ld\n", fibonacci[n]);
        }
        return 0;
    }