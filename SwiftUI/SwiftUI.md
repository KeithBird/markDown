SwiftUI
---

Ctrl: Extract Subview + Inspect


Modifiers: shift + command + L

扩充  

```swift
.frame(maxWidth: .infinity, maxHeight: .infinity)
```

安全区  

```swift 
.edgesIgnoringSafeArea(.all)
```

圆角  

```swift 
.cornerRadius
```

偏移 

```swift
.offset(x: , y: ) 
```

旋转 

```swift
.rotationEffect(Angle(degrees: 15))
.rotation3DEffect(Angle(degrees: 50), axis: (x: , y: , z: ))
```

投影 

```
.blendMode(.hardLight)
```

点击开关 

```swift
.tapAction { self.show.toggle() }
```

弹性动画 

```swift
.animation(.spring())
```

