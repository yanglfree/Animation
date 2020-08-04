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

