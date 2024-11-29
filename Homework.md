### 姓名

范力维

### 开发中的快乐开源任务

利用 AI Studio 完成 PaddlePaddle 编译

### 本双周工作

1. **任务 X**

完成前期准备工作
拉取 PaddlePaddle/Paddle 仓库代码,并安装相关依赖。

1. git clone https://github.com/PaddlePaddle/Paddle.git

2. cd Paddle

3. pip3.8 install -r python/requirements.txt
注： 在运行 pip 命令前，可以先运行 python --version 命令查看 python 版本。

完成 PaddlePaddle 初次编译
4. mkdir build

5. cd build

6. time cmake .. -DPY_VERSION=3.8 -DWITH_GPU=OFF -DWITH_TESTING=ON
执行完成后截图 cmake 结果，注意需要包含时间和 commit 号(时间大概需要 4h)。

7. time make -j$(nproc)
执行完成后截图 make 结果。

注： 在初次编译的时候，我们就加上了 -DWITH_TESTING=ON，所以在运行单元测试的时候就可以不用再重新 cmake 和 make 了。

2. **任务 Y**

在修改文件的时候，在有注释的地方添加空格，然后保存即可。

修改头文件：Paddle/paddle/fluid/platform/enforce.h

8. time make -j$(nproc)
执行完成后截图 make 结果。

修改 cc 文件：Paddle/paddle/fluid/operators/center_loss_op.cc

9. time make -j$(nproc)
执行完成后截图 make 结果。

修改 python 文件：Paddle/python/paddle/tensor/math.py

10. time make -j$(nproc)
执行完成后截图 make 结果。

安装 whl 包
11. pip3.8 install /python/dist/paddlepaddle-0.0.0-cp38-cp38m-linux_x86_64.whl
执行完成后截图。

注: 这里安装的 whl 包可能会因为 python 版本等原因不同，没有必要一模一样粘贴命令运行，建议进入对应文件夹查看具体 whl 包名称后运行安装。
最终效果
![image](https://github.com/user-attachments/assets/a92cd9af-504a-4db2-91dc-c64e7745e96b)


3. **问题疑惑与解答**

   - 问题: 编译完成后二次编译失败
   ![52F074C515E4C6257E795A8BDD6F5E81](https://github.com/user-attachments/assets/93b8a27c-2835-478a-be1c-cab6ac7760c5)


   - 问题：之前也试过本地编译但是失败了
   ![image](https://github.com/user-attachments/assets/d5245e74-1a7f-4033-99da-673397a49d7d)


### 未来双周计划

1. 再次尝试编译Paddle
2. 报名文档编辑的任务
3. 完成热身任务
