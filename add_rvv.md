## 目标:  
   V8-RISCV支持RVV指令  
## 需要的工作:
1. RVV和V8-SIMD相关调研
1. 汇编器支持RVV
1. Turbofan code-gen SIMD指令
1. Liftoff code-gen SIMD指令
1. 模拟器模拟RVV指令
1. RVV指令反汇编
1. RVV单元测试

##  工作量  
-   SIMD machine op : 128个
-   RVV 指令数: 大约198个
## RoadMap
#### Phase I:  开发准备
1. 调研RVV指令格式   @wangjianzhong 
    - 调研目前V8汇编器代码能否满足RVV的需求
    - 调研目前V8反汇编器代码能否满足RVV的需求
1. 调研TurboFan和LiftOff对于SIMD指令地处理流程:SIMD指令code-gen流程, 向量寄存器分配  @qjivy 
1. 调研QEMU  Spike如何模拟RVV指令  @luyahan 

#### Phase II: V8模拟执行WASM-SIMD程序

1. 增加一条WASM-SIMD
   -  在V8模拟器、Qemu上执行,并增加该指令的单元测试
1. 将RVV指令分类，分类进行开发
1. 在Simulator/QEMU/真实硬件上运行包含一条RVV指令的SIMD
1. 在Simulator/QEMU/真实硬件上运行采用WASM-SIMD编写的X*X矩阵乘法程序
1. 在Simulator/QEMU/真实硬件上运行TF.JS demo

## Question
1.  RVV中不同的平台可能会有不同的VLEN,SLEN,ELEN配置，是否需要支持根据配置参数来code-gen? 注：Spike支持配置

**工作进度**
- [ ] RVV指令添加 
- [ ] 在Simulator/QEMU/真实硬件上运行包含一条RVV指令的SIMD
```
#include <wasm_simd128.h>
int fun(v128_t a,v128_t b) {
  v128_t prod = wasm_i32x4_add(a, b);
  return prod[0];
}
int main() {
  v128_t a = {1,2,3,4};
  v128_t b = {5,4,6,8};
  return fun(a,b);
}

```
- [ ] 移植RVV到liftoff 
- [ ] 移植RVV到Turbofan
- [ ] 在Simulator/QEMU/真实硬件上运行采用WASM-SIMD编写的X*X矩阵乘法程序
- [ ] 在Simulator/QEMU/真实硬件上运行TF.JS demo
