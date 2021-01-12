# Function Definition Statement
```java
func int main(int:a,int:b){
    return 1;
}
```
reg30: args addres register <br>
reg31: frame offset register <br>
reg32: function return value register <br>
以上代码应该将被翻译成:
```asm
main:
mov_m [0],[reg30],8;
add reg30,8;
mov_m [0],[reg30],8;
mov 1,reg10;
```
**调用语句**`main(0,0);`
```asm
mov_m [0],0,8;
mov_m [8],0,8;
add reg31,16;
mov reg30,0;
call main;
```
