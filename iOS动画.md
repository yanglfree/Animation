## Spring动画

## Transition动画

## 帧动画 Keyframe Animations

## 约束动画 Constraint Animations

## 属性动画 Layer Animations

## Animation Key

## Groups

## Layer Spring 图层弹簧动画
 ```
    let pulse = CASpringAnimation(keyPath: "transform.scale")
    pulse.damping = 2.0
    pulse.fromValue = 1.25
    pulse.toValue = 1.0
    pulse.duration = pulse.settlingDuration 
    layer?.add(pulse, forKey: nil)
 ```

## Gradient Animations渐变动画

渐变动画就是CAGradientLayer图层对象，添加一个locations的属性动画


``` Swift
  let gradientLayer: CAGradientLayer = {
    let gradientLayer = CAGradientLayer()
    gradientLayer.startPoint = CGPoint(x: 0.0, y: 0.5)
    gradientLayer.endPoint = CGPoint(x: 1.0, y: 0.5)
    
    let colors = [
        UIColor.black.cgColor,
        UIColor.white.cgColor,
        UIColor.black.cgColor
    ]
    gradientLayer.colors = colors
    
    let locations: [NSNumber] = [
        0.25,
        0.5,
        0.75
    ]
    
    gradientLayer.locations = locations
    return gradientLayer
  }()
```

```Swift
    let gradiantAnimation = CABasicAnimation(keyPath: "locations")
    gradiantAnimation.fromValue = [0.0, 0.0, 0.25]
    gradiantAnimation.toValue = [0.75, 1.0, 1.0]
    gradiantAnimation.duration = 3.0
    gradiantAnimation.repeatCount = Float.infinity
    
    gradientLayer.add(gradiantAnimation, forKey: nil)
```



可以通过将gradientLayer的frame变大来使渐变更加柔和
![aj6Rcq.png](https://s1.ax1x.com/2020/08/12/aj6Rcq.png)
```
gradientLayer.frame = CGRect(x: -bounds.size.width, y: bounds.origin.y, width: 3 * bounds.size.width, height: bounds.size.height)

```

[![ajfsEV.md.gif](https://s1.ax1x.com/2020/08/12/ajfsEV.md.gif)](https://imgchr.com/i/ajfsEV)
