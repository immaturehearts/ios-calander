//
//  main.swift
//  自强
//
//  Created by 王珂欣 on 2018/10/16.
//  Copyright © 2018 王珂欣. All rights reserved.
//


//输入某年的年份及一月一日是周几，能够打印出该年一月的月历
import Foundation

func isPurnInt(string: String) -> Bool {
    
    let scan: Scanner = Scanner(string: string)
    
    var val:Int = 0
    
    return scan.scanInt(&val) && scan.isAtEnd
    
}


print("Please input a year：")
let theInput1 = readLine()

if isPurnInt(string: theInput1!) {
}
else {
    print("Please input only numbers! Try again.")
    exit(0)
}

print("What day is Jan 1st in this year：")
let theInput2 = readLine()
let headline = "\n\nJanuary, \(theInput1!) is as followed:\n"
print(headline)

var a = 0
switch theInput2 {
case "Monday","星期一","周一","1","一" :
    a = 1
case "Tuesday","星期二","周二","2","二" :
    a = 2
case "Wednesday","星期三","周三","3","三" :
    a = 3
case "Thursday","星期四","周四","4","四" :
    a = 4
case "Friday","星期五","周五","5","五" :
    a = 5
case "Saturday","星期六","周六","6","六" :
    a = 6
case "Sunday","星期日","星期天","周日","周天","7","日","天" :
    a = 7
default:
    print("Not true! Please check your answer.")
    exit(0)
}

//print("Monday\tTuesday\tWednesday\tThursday\tFriday\tSaturday\tSunday")
print("Mon\t\tTue\t\tWed\t\tThu\t\tFri\t\tSat\t\tSun")
//let i = 1
//let str = String(format: "%03d", i)

let f = a - 1
for _ in 1...f{
    print("\t\t", terminator: "")
}

for b in 01...31 {
    let c = a + b
    let d:String = String(format: "%02d", b)
    switch c{
    case 8,15,22,29,36:
        print(d)
    default:
        print("\(d) ","\t", terminator: "")
    }
}






//计算一年有几个周日
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

//考虑到闰年的情况
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

