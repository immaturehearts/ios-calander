# ios-calander
//
//  main.swift
//  自强
//
//  Created by 王珂欣 on 2018/10/16.
//  Copyright © 2018 王珂欣. All rights reserved.
//


//输入某年的年份及一月一日是周几，能够打印出该年一月的月历
import Foundation

print("Please input a year：")
let theInput1 = readLine()
print("What day is Jan 1st in this year：")
let theInput2 = readLine()


switch theInput2 {
case "Monday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n  1       2        3        4        5       6       7\n  8       9        10       11       12      13      14\n  15      16       17       18       19      20      21\n  22      23       24       25       26      27      28\n  29      30       31")
case "Tuesday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n          1        2        3        4        5       6\n  7       8        9        10       11       12      13\n  14      15       16       17       18       19      20\n  21      22       23       24       25       26      27\n  28      29       30       31")
case "Wednesday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n                    1        2       3        4       5\n  6       7         8        9       10       11      12\n  13      14        15       16      17       18      19\n  20      21        22       23      24       25      26 \n  27      28        29       30      31")
case "Thursday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n                             1       2       3       4\n  5       6        7         8       9       10      11\n  12      13       14        15      16      17      18\n  19      20       21        22      23      24      25\n  26      27       28        29      30      31")
case "Friday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n                                     1       2       3\n  4       5        6         7       8       9       10\n  11      12       13        14      15      16      17\n  18      19       20        21      22      23      24\n  25      26       27        28      29      30      31")
case "Saturday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n                                             1       2\n  3       4         5        6       7       8       9\n  10      11        12       13      14      15      16\n  17      18        19       20      21      22      23\n  24      25        26       27      28      29      30\n  31")
case "Sunday":
    print("Monday Tuesday  Wednesday Thursday Friday Saturday Sunday \n                                                      1\n  2       3         4         5       6       7       8\n  9       10        11        12      13      14      15\n  16      17        18        19      20      21      22\n  23      24        25        26      27      28      29\n  30      31")
default:
    print("Not true! Please check your answer.")
}






