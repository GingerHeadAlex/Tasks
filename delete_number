# Для каждого набора входных выведи наибольше число после удаления одной цифры из числа
# На вход первым числом поступает количество данных t с диапазоном от 1 до 100000 включительно
# После сами данные s с диапазоном от 1 до 100000 включительно
# Данные s не содержат ведущих нулей и сумма количества цифр по всем введенным числам не превосходит 1000000
# Если условия по t или s не выполняется, программа должна завершиться оператором return 0
# Если изначальное число t содержит всего одну цифру, после ее удаления в ответе будет 0
# Пример данных:
# Входные данные
# 3
# 9
# 0
# 9123
# Выходные данные
# 0
# 0
# 923

import sys

def fast_input():
    return sys.stdin.readline().rstrip("\r\n")

def fast_output(x):
    sys.stdout.write(str(x) + "\n")

def main():
    t = int(fast_input())

    if t < 1 or t > 100000:
        return 0

    results = []
    total_length = 0

    for _ in range(t):
        s = fast_input()
        size_of_s = len(s)
        total_length += size_of_s

        if size_of_s < 1 or size_of_s > 100000:
            return 0

        if total_length > 1000000:
            return 0

        if size_of_s == 1:
            results.append('0')
            continue

        max_str = ""  
        for j in range(size_of_s):
            candidate = s[:j] + s[j+1:]
            if candidate > max_str:
                max_str = candidate

        results.append(max_str)

    fast_output('\n'.join(results))

if __name__ == "__main__":
    main()
