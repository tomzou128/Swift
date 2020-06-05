# Question book
## 1. Which is wrong?
```swift
var c = ["a", "b", "c"]

c.remove(at: 2)    //1
c.append(["d", "e"])    //2
c.append("d")    //3
c += ["d", "e"]    //4
```
The second one is wrong.
</br>

## 2. Which is wrong?
```swift
func Hello(to id: Int) {    //1
	print("Hello" + id)
}
func Hello(to id: Character) {    //2
	print("Hello" + id)
}
func Hello(to name: String) {    //3
	print("Hello \(name)!")
}
func Hello(to name: String) -> string {    //4
	return "Hello \(name)!"
}
```
1. is wrong because ```String``` can't to add with ```Int``` directly.
2. is wrong because ```Character``` can't conver to ```String```.
3. is correct.
4. is wrong because it should be ```String``` instead of ```string```.
</br>

## 3. Which is wrong?
```swift
var color = ["red", "yellow", "blue"]

color[(0...color.count).randomElement()!]    //1
color[(0...color.count - 1).randomElement()!]    //2
color[(0...<color.count).randomElement()!]    //3
color.randomElement()    //4
```
2, 3, 4 are correct, 1 is wrong.

## Which is correct?
```swift
var f: [String] = "apple" + "banana"    //1
var f2: [String] = ["apple"] + "banana"    //2
var f3: [String] = ["apple"]    //3
var f4: [String] = ["apple"] + ["banana"]    //4
```
1, 2 are wrong, 3, 4 are correct.
