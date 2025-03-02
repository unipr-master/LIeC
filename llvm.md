

 clang -Xclang -disable-O0-optnone -S -emit-llvm source.c -o source.ll

llvm-extract -S -func='main' -o main.ll source.ll

opt -passes=dot-cfg main.ll -o /dev/null

xdot .main.dot


---

controlla come si usa clang-tidy

---