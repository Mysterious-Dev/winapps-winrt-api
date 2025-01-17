---
-api-id: T:Microsoft.UI.Xaml.Media.Animation.DiscreteColorKeyFrame
-api-type: winrt class
---

<!-- Class syntax.
public class DiscreteColorKeyFrame : Windows.UI.Xaml.Media.Animation.ColorKeyFrame, Windows.UI.Xaml.Media.Animation.IDiscreteColorKeyFrame
-->

# Microsoft.UI.Xaml.Media.Animation.DiscreteColorKeyFrame

## -description
Animates from the [Color](/uwp/api/windows.ui.color) value of the previous key frame to its own [Value](colorkeyframe_value.md) using discrete values.

## -xaml-syntax
```xaml
<DiscreteColorKeyFrame .../>
```


## -remarks
Key-frame animations permit more than one target value that is reached at a point along the animation timeline. In other words each key frame can specify a different intermediate value, and the last key frame reached is the final animation value. By specifying multiple values to animate, you can make more complex animations. You can mix discrete, linear, and spline keyframes in the same keyframe collection.

For more info on how to use key-frame animations, see [Key-frame animations and easing function animations](/windows/apps/design/motion/key-frame-and-easing-function-animations).

## -examples
This XAML example uses the **ColorAnimationUsingKeyFrames** class to animate the [Background](../microsoft.ui.xaml.controls/panel_background.md) property of a [StackPanel](../microsoft.ui.xaml.controls/stackpanel.md). This animation uses three key frames in the following manner:

1. During the first two seconds, [LinearColorKeyFrame](linearcolorkeyframe.md) gradually changes the color from green to red. Linear key frames like [LinearColorKeyFrame](linearcolorkeyframe.md) create a smooth linear transition between values.
1. During the end of the next half second, DiscreteColorKeyFrame quickly changes the color from red to yellow. Discrete key frames like DiscreteColorKeyFrame create sudden changes between values; the animation occurs quickly and has no interpolation between values at all.
1. During the final two seconds, [SplineColorKeyFrame](splinecolorkeyframe.md) changes the color again, this time from yellow back to green. Spline key frames like [SplineColorKeyFrame](splinecolorkeyframe.md) create a variable transition between values according to the values of the [KeySpline](splinecolorkeyframe_keyspline.md) property. A [KeySpline](keyspline.md) provides a way to alter the relationship of time versus value during the animation duration to be nonlinear, and in particular the relationship can be a curve that would be difficult to produce with individual key frames. In this example, the change in color begins slowly and speeds up exponentially toward the end of the time segment.

[!code-xaml[Coloranimationusingkeyframes](../microsoft.ui.xaml.media.animation/code/coloranimationusingkeyframes/csharp/Page.xaml#SnippetColoranimationusingkeyframes)]


[!code-csharp[Coloranimationusingkeyframes_cs](../microsoft.ui.xaml.media.animation/code/coloranimationusingkeyframes/csharp/Page.xaml.cs#SnippetColoranimationusingkeyframes_cs)]

[!code-vb[Coloranimationusingkeyframes_cs](../microsoft.ui.xaml.media.animation/code/coloranimationusingkeyframes/vbnet/Page.xaml.vb#SnippetColoranimationusingkeyframes_cs)]

## -see-also
[Storyboarded animations](/windows/apps/design/motion/storyboarded-animations), [Key-frame animations and easing function animations](/windows/apps/design/motion/key-frame-and-easing-function-animations), [ColorKeyFrame](colorkeyframe.md), [ColorAnimationUsingKeyFrames](coloranimationusingkeyframes.md), [KeyTime](colorkeyframe_keytime.md), [Value](colorkeyframe_value.md), [KeyTime](colorkeyframe_keytime.md), [Value](colorkeyframe_value.md)
