# 6: Intro to Xcode Project with UI

## Storyboard tips
### Auto-layout
Make use of Auto-layout. Put objects which are in the same category into a stack view. The key part is to have use layer concept to building the whole thing.
<br>

### Button tips
When we want to create a button with an image, we sometimes create a view and put both an image and a button in it. Then set the image to be on top of the button. We don't prefer using the background image of button because the size of image may not fit the size of button we want (e.g. we want the button to be larger than the image). So it is better to separate them.
<br><br>

## Image tips
We can put a list of images into the a list in class, so that we can use the list element directly. Type 'image literal', then press 'enter', we can select images directly.
<br><br>



## Playground: Define a layout

```swift
import Foundation
import UIKit

public class GameViewController: UIViewController {
    
    let allCharacters = ["👦", "🐒", "🐷", "👻"]
    
    var myChoices = ["👦", "🐒", "🐷"]
    var pcChoices = [String]()
    var myChoice_labels = [UILabel]()
    var pcChoice_lables = [UILabel]()
    var gameScoreLabel = UILabel()
    var score = 0
    
    public override func loadView() {
        // Setup PC choices
        for _ in 0..<myChoices.count {
            pcChoices.append(allCharacters.randomElement()!)
        }
        
        //Setup base view
        let view = UIView()
        view.backgroundColor = .white
        
        
        let gameView = UIView()
        gameView.clipsToBounds = true    // UI stick to the border of the screen
        gameView.layer.cornerRadius = 8.0    // Set corner radius
        gameView.backgroundColor = .white
        self.view.addSubview(gameView)    //add myself to the main view
        
        
    }
    
}
```

## Xcode project: journey to the West

### 1. Setup a Xcode project
1. Choose 'ios', 'single view', and 'story board' as the user interface. <br>

### 2. Setup storyboard
In ```main.storyboard``` page, you can drag and drop anything you want to put into the page. <br>

#### Objects in page 1
Image 1: <br>
Constraints: top, left, right and height. <br>
Label 1: <br>
Constraints: top, left, right and height. <br>
Label 2:  <br>
Constraints: top, left, right <br>
Button 1: <br>
Constraints: bottom, left, right and height. <br>

Note that Label 2 doesn't fix its height, because we don't know its height on every phone. <br>



#### Objects in page 2
Image 1: <br>
Constraints: top, horizontally in container, width and height. <br>
View 1: <br>
Constraints: top, left, horizontally in container and height. <br>

Therefore, we either have **left distance fixed with horizontally in container**, or **a fixed width with horiontally in container**.
<br><br>




