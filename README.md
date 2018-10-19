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
let headline = "\n\n January, \(theInput1!) is as followed:\n"
print(headline)

switch theInput2 {
case "Monday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n1\t2\t3\t4\t5\t6\t7\n8\t9\t10\t11\t12\t13\t14\n15\t16\t17\t18\t19\t20\t21\n22\t23\t24\t25\t26\t27\t28\n29\t30\t31")
case "Tuesday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n\0\t1\t2\t3\t4\t5\t6\n7\t8\t9\t10\t11\t12\t13\n14\t15\t16\t17\t18\t19\t20\n21\t22\t23\t24\t25\t26\t27\n28\t29\t30\t31")
case "Wednesday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n\0\t\0\t1\t2\t3\t4\t5\n6\t7\t8\t9\t10\t11\t12\n13\t14\t15\t16\t17\t18\t19\n20\t21\t22\t23\t24\t25\t26\n27\t28\t29\t30\t31")
case "Thursday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n\0\t\0\t\0\t1\t2\t3\t4\n5\t6\t7\t8\t9\t10\t11\n12\t13\t14\t15\t16\t17\t18\n19\t20\t21\t22\t23\t24\t25\n26\t27\t28\t29\t30\t31")
case "Friday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n\0\t\0\t\0\t\0\t1\t2\t3\n4\t5\t6\t7\t8\t9\t10\n11\t12\t13\t14\t15\t16\t17\n18\t19\t20\t21\t22\t23\t24\n25\t26\t27\t28\t29\t30\t31")
case "Saturday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n\0\t\0\t\0\t\0\t\0\t1\t2\n3\t4\t5\t6\t7\t8\t9\n10\t11\t12\t13\t14\t15\t16\n17\t18\t19\t20\t21\t22\t23\n24\t25\t26\t27\t28\t29\t30\n31")
case "Sunday":
    print("Mon\tTue\tWed\tThu\tFri\tSat\tSun\n\0\t\0\t\0\t\0\t\0\t\0\t1\n2\t3\t4\t5\t6\t7\t8\n9\t10\t11\t12\t13\t14\t15\n16\t17\t18\t19\t20\t21\t22\n23\t24\t25\t26\t27\t28\t29\n30\t31")
default:
    print("Not true! Please check your answer.")
}

var dates = 1
var n = 0
var i = 0
for dates in 1...365 {
    for n in 1...9999 {
        if dates == 7*n {
            i += 1
        }
    }
}

let j = i + 1
let theInput3 = Int(theInput1!)
if theInput3 == 4*n {
    switch theInput2 {
    case "Sunday","Saturday":
        print("\n\n\n There are \(j) Sundays in \(theInput1!)")
    default:
        print("\n\n\n There are \(i) Sundays in \(theInput1!)")
    }

}
else {
    switch theInput2 {
    case "Sunday":
        print("\n\n\n There are \(j) Sundays in \(theInput1!)")
    default:
        print("\n\n\n There are \(i) Sundays in \(theInput1!)")
    }
}

