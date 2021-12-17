---
layout: post
title: Customization in .NET MAUI Effects View control | Syncfusion
description: Learn here all about Customization support in Syncfusion .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui
control: Effects View
documentation: ug
---

# Customization in .NET MAUI Effects View (SfEffectsView)

The `SfEffectsView` control provides support to customize the animation duration, color, and more. This section explains how to customize the effects view control.

## RippleAnimationDuration

The `RippleAnimationDuration` property of `SfEffectsView` is used to customize the duration of ripple animation.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView RippleAnimationDuration="800">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView()
{
    RippleAnimationDuration = 800
};

{% endhighlight %}

{% endtabs %}

## ScaleAnimationDuration

The `ScaleAnimationDuration` property of `SfEffectsView` is used to customize the duration of scale animation.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView
    ScaleAnimationDuration="800"
    LongPressEffects="Scale"
    ScaleFactor="0.85">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView()
{
    ScaleAnimationDuration = 800,
    LongPressEffects = SfEffects.Scale,
    ScaleFactor = 0.85
};

{% endhighlight %}

{% endtabs %}

## RotationAnimationDuration

The `RotationAnimationDuration` property of `SfEffectsView` is used to customize the duration of rotation animation.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView
    RotationAnimationDuration="800"
    Angle="180"
    TouchDownEffects="Rotation">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView()
{
    RotationAnimationDuration = 800,
    Angle = 180,
    TouchDownEffects = SfEffects.Rotation
};

{% endhighlight %}

{% endtabs %}

## InitialRippleFactor

The `InitialRippleFactor` property of `SfEffectsView` is used to customize the radius of the ripple when ripple animation starts.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView InitialRippleFactor="0.1">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView
{
    InitialRippleFactor = 0.1
};

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View InitialRippleFactor customization](Customization_images/EffectsView_InitialRippleFactor.gif)

## ScaleFactor

The `ScaleFactor` property of `SfEffectsView` is used to customize the scale of the view.

{% tabs %} 

{% highlight xaml %} 

 <syncEffectsView:SfEffectsView
     ScaleFactor="0.85"
     LongPressEffects="Scale"
     TouchDownEffects="None"
     TouchUpEffects="None">
 </syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView
{
    ScaleFactor = 0.85,
    LongPressEffects = SfEffects.Scale,
    TouchDownEffects = SfEffects.None,
    TouchUpEffects = SfEffects.None
};

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View ScaleFactor customization](Customization_images/EffectsView_Scale.gif)

## HighlightBackground

The `HighlightBackground` property of `SfEffectsView` is used to customize the color of highlight effect.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView
     HighlightBackground="#2196F3"
     TouchDownEffects="Highlight">
 </syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView
{
    effectsView.HighlightBackground = new SolidColorBrush(Colors.Aqua),
    TouchDownEffects = SfEffects.Highlight
};

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View highlight background customization](Customization_images/EffectsView_Highlight.png)

## RippleBackground

The `RippleBackground` property of `SfEffectsView` is used to customize the color of ripple.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView RippleBackground="#2196F3">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView
{
    RippleBackground = new SolidColorBrush(Colors.Aqua)
};
            
{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View ripple background customization](Customization_images/EffectsView_RippleColor.gif)

## SelectionBackground

The `SelectionBackground`property of `SfEffectsView` is used to customize the color of selection effect.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView
    LongPressEffects="Selection"
    SelectionBackground="#2196F3">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView
{
    LongPressEffects = SfEffects.Selection,
    SelectionBackground = new SolidColorBrush(Colors.Aqua)
};

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View selection background customization](Customization_images/EffectsView_Selection.png)

## Angle

The `Angle` property of `SfEffectsView` is used to customize the rotation angle.

{% tabs %} 

{% highlight xaml %} 

<syncEffectsView:SfEffectsView
    Angle="180"
    TouchDownEffects="Ripple,Rotation">
</syncEffectsView:SfEffectsView>

{% endhighlight %}

{% highlight C# %} 

var effectsView = new SfEffectsView
{
    Angle = 180,
    TouchDownEffects = SfEffects.Ripple | SfEffects.Rotation
};
            
{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View rotation angle customization](Customization_images/EffectsView_Rotation.png)
