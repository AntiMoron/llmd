# Using markdown as a programming language
�����markdown����һ�ű�����Կ�������Щ��Ȥ�����飿�����Ŀ����Ϊ�˽���������:)

# ʾ��:ʹ��markdown����쳲���������
+ Դ��:[fibonacci.md](example/fibonacci.md)
+ llvm ir:
```llvm
; ModuleID = 'llmd'
source_filename = "llmd"

define void @main() {
entry:
  %times = alloca i32
  %result = alloca i32
  %b = alloca i32
  %a = alloca i32
  store i32 1, i32* %a
  store i32 1, i32* %b
  store i32 0, i32* %result
  store i32 50, i32* %times

label:                                            ; preds = %label
  %a1 = load i32, i32* %a
  %b2 = load i32, i32* %b
  %addtmp = add i32 %a1, %b2
  %times3 = load i32, i32* %times
  %subtmp = sub i32 %times3, 1
  %times4 = load i32, i32* %times
  %ifcond_var = icmp ne i32 %times4, 0
  br i1 %ifcond_var, label %label, label %end

end:                                              ; preds = %label
}
```

# ���¶���һ��ͼ���걸���﷨��
```comment               // Block comments

[var](value)             // Input(Literal,Arithmetic)

>                        // Output

`a+b`                    // Arithmetic(+,-,*) 

**label**                // Mark as a label

![condition](tag)       // Jump label if condition != 0

```