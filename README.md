# LAB4-1 Firmware 控制 User-project
* 利用firmware控制user project 並且執行 
* firmware Code input "user project memeory"(exmem 0x3800) from spi-flash(0x1000) 並且執行
* "wishbond" bus interface to "sram" interface

## **caravel soc 架構**
![image](https://hackmd.io/_uploads/HyEiRVeLa.png)

## 簡單執行
### 下載檔案
https://github.com/bol-edu/caravel-soc_fpga-lab/tree/main/lab-exmem_fir
### Design Firmware Code
檔案位置  FIR Code
lab-exmem_fir/testbench/counter_la_fir/fir.h  
lab-exmem_fir/testbench/counter_la_fir/fir.c  
  
#### 開始設計檔案
![image](https://hackmd.io/_uploads/S1njldeLT.png)
#### 1. fir.h 定義參數
![image](https://hackmd.io/_uploads/H1nN4UmUp.png)
taps: 設定 11個coeff
inputsignal :11個input
#### 2. fir.c 設計功能
**公式:**
![image](https://hackmd.io/_uploads/B1wvnxVU6.png)
**實作:**
![image](https://hackmd.io/_uploads/HyKVUPmU6.png)
> note: 此fir全部都在CPU內執行
### Simulation for FIR
```
cd ~/lab-exmem-fir/testbench/counter_la_fir
source run_clean
source run_sim
```



## LAB4 實驗步驟
LAB4基礎知識   
https://hackmd.io/@861r6vBbQbu3FLGNe3SkyQ/SkC0vJ1UT  
https://github.com/MODKWODK/LAB4-BACKGROUND  
LAB4-0  
https://hackmd.io/@861r6vBbQbu3FLGNe3SkyQ/SkC0vJ1UT  
https://github.com/MODKWODK/LAB4-0-caravel-SOC-simulation-  
LAB4-1  
https://hackmd.io/@861r6vBbQbu3FLGNe3SkyQ/HybFQWkIT  
https://github.com/MODKWODK/LAB4-1-Firmware-User-project  
LAB4-2  
https://hackmd.io/@861r6vBbQbu3FLGNe3SkyQ/BJXPryyIp  
https://github.com/MODKWODK/LAB4-2-MIX-LAB3-FIR-LAB4-1-WITH-WISHBOND  

參考文件:  
https://blog.csdn.net/alangaixiaoxiao/article/details/81592437 









