## LeetCode 824.Goat Latin

### 自己的方法
#### 解决思路：    
* 利用空格，首先得到这句话中的每个单词
* 再判断元音开头的单词，并对每个单词进行后期处理
#### 注意事项：
* 由于最后一个单词后没有空格，本方案采用下标序号来判断是否为最后一个单词

### 大神的方法
#### 解决思路：
* 利用C++中stringstream去除空格，进而得到这句话中的每个单词
* 利用C++中string类的成员函数find/find_first_of来判断首字母是否为元音字母
#### 涉及的知识点：
* [C++ stringstream介绍，使用方法与例子](https://www.cnblogs.com/wuchanming/p/3906176.html)
* [string类成员函数find/find_first_of用法详解](https://blog.csdn.net/iot_change/article/details/8496977)
#### 具体代码

```c++
string toGoatLatin(string S) {
    stringstream iss(S), oss;
    string vowels("aeiouAEIOU"), word, a;
    while (iss >> word) {
        a.push_back('a');
        if (vowels.find_first_of(word[0]) != string::npos) // begin with a vowel, hint:  here "string::npos"means find failed
            oss << ' ' << word << "ma" << a;
        else // begin with a consonant
            oss << ' ' << word.substr(1) << word[0] << "ma" << a;
    }
    return oss.str().substr(1);
}
```
