# code-when-i-am-a-newbie
Viết chương trình kiểm tra số đối xứng (palindrome). Định nghĩa: Số đối xứng là một số tự nhiên mà khi đảo ngược các chữ số vẫn không thay đổi, ví dụ: số 16461 là số đối xứng.
#include <iostream>
using namespace std;
bool lasodoixung(int n){
if (n<0) return false;

int sogoc = n;
int sodaonguoc = 0;
while (n > 0){
    int chusocuoi = n % 10;
    sodaonguoc = sodaonguoc * 10 + chusocuoi;
    n /= 10;
}
return sogoc == sodaonguoc;
}
int main(){
int n;
cin >> n;
cout << (lasodoixung(n)? "true" : "false")<<endl;
    return 0;
}
