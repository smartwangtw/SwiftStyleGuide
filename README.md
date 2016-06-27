這份文件 Swift Style Guide 係參考以下連結：
https://github.com/raywenderlich/swift-style-guide

# Swift Style Guide

##命名
class大寫
variable, method小寫

enum的名字和case都大寫
```
enum Shape {
  case Rectangle
  case Square
  case Triangle
  case Circle
}
```

##縮排
維持預設4個字
可以利用 Control-i 來自動縮排
格式：
```
if user.isHappy {
  // Do something
} else {
  // Do something else
}
```

##註解
程式本身就需具可讀性
避免 inline 的註解

##self
利用 self 來區分 class 的屬性和參數或區域變數

##符合 protocol
利用 extension 與 MARK: 來區分實作 protocol 的段落
```
class MyViewcontroller: UIViewController {
  // class stuff here
}

// MARK: - UITableViewDataSource
extension MyViewcontroller: UITableViewDataSource {
  // table view data source methods
}

// MARK: - UIScrollViewDelegate
extension MyViewcontroller: UIScrollViewDelegate {
  // scroll view delegate methods
}
```
##FIXME, TODO
程式區段可以利用FIXME或TODO來提醒自己未完成的內容
```
// FIXME: something needs to fix
your code
```

##計算屬性
屬性唯讀時，直接利用 return, 而不是再放一個 get

##function 宣告
名稱與屬性儘量維持一行

##資料型態
儘量使用 swift 原生資料型態
特殊應用，例如 Sprite Kit, 儘量利用應用中的資料型態，避免型態轉換

##常數
不會改變就用 let 宣告

##optional
變數允許 nil 時才使用 optional
後續有很多運算時，使用 optional binding 來減少 unwrap 的次數
變數名字不要加 optional

##Control Flow
儘量使用 for-in

##分號
swift 可以不使用分號

##語言
使用美式英語，比較符合 Apple API

建議：
```
let color = "red"
```

不建議：
```
let colour = "red"
```
