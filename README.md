# LCD-Desktop-Monitor-Tool-by-Aida64
利用Aida64-设置-LCD中POS或Pertelian做串口输出数据的电脑性能监视工具
#!/bin/bash
# 循环 0x08 ~ 0x77
for ((i=0x08; i<=0x77; i++)); do
    # 转成十六进制字符串，带0x前缀
    hex=$(printf "0x%02X" $i)
    echo "===== 正在执行: python3 12.py $hex ====="
    python3 12.py "$hex"
    # 可选：每条执行完停顿一下，去掉注释启用
    # sleep 0.2
done
echo "全部参数跑完！"
