# 🐱‍👤 Simplest-LeetCode-Cpp-Solutions
Leet Code 刷题笔记 - - 不求最快最省，但求最简最优雅 ✒，Simpler is better here.

# 前言
- 为了快速找到题目可以按 [**Ctrl键 + F键**] 输入题目序号或名字定位。
- 欢迎加入**QQ交流群**：902025048 [∷二维码](QR.png) 群内提供更多相关资料~

# 题库解析
此专栏追求代码的**精简**和**技巧性**，默认已看过题目，🤖 没看过的话点标题可以跳转链接，一起体验炫酷的 Cpp

## [1108. Defanging an IP Address](https://leetcode.com/problems/defanging-an-ip-address/)
```cpp
class Solution {
public:
    string defangIPaddr(string address) {
        for(int i = address.size(); i >= 0; i--){
            if(address[i] == '.'){
                address.replace(i, 1, "[.]");
            }
        }
        return address;
    }
};
```
- 逆遍历字符串并替换 `.` 为 `[.]`
- 本题若正遍历，每次替换完，下一个字符会变成 `.`，进入死循环
