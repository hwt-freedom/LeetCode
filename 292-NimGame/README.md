## LeetCode 292-NimGame

### 结论
* 当序号是4的倍数时，必将输掉比赛
### 推导
* 假设序号是1、2、3其中任意一个，只要先移动石头，即可赢得比赛
* 假设序号是4，只要先移动，无论移动几块，对手都可以继续移动赢得比赛
* 假设序号是5、6、7，只要先移动，把必输的序号4留给对手即可
* 假设序号是8，同理无论移动几块，对手都可以移动后将必输的序号4留给本方
* ...依次类推，得出只要在本方和对手都采取最佳策略时，序号为4的倍数的一方都将输掉比赛
