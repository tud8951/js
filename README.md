# Guess Number
## 源代码：

import random

def guess_number():
    number_to_guess = random.randint(1, 100)
    attempts = 0

    print("欢迎来到猜数字游戏！")
    print("我已经想好了一个1到100之间的数字。")

    while True:
        try:
            guess = int(input("请输入你的猜测: "))
            attempts += 1

            if guess < number_to_guess:
                print("太小了！再试一次。")
            elif guess > number_to_guess:
                print("太大了！再试一次。")
            else:
                print(f"恭喜你，猜对了！你总共猜了 {attempts} 次。")
                break
        except ValueError:
            print("请输入一个有效的数字。")

if __name__ == "__main__":
    guess_number()
