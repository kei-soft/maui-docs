---
layout: post
title: Tick in .NET MAUI Slider control | Syncfusion 
description: Learn here all about adding the Tick feature of Syncfusion .NET MAUI Slider (SfSlider) control and more.
platform: maui
control: SfSlider
documentation: ug
---

# Tick in .NET MAUI Slider (SfSlider)

This section helps to learn about how to add major and minor ticks in the slider.

## Show major ticks

You can enable the major ticks on the track. It is a shape which is used to represent the major interval points of the track. The default value of [`ShowTicks`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_ShowTicks) property is `False`.

For example, if [`Minimum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Minimum) is 0.0 and [`Maximum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Maximum) is 10.0 and [`Interval`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Interval) is 2.0, the slider will render the major ticks at 0.0, 2.0, 4.0 and so on.

### Without Interval

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider ShowTicks="True" />

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.ShowTicks = true;

{% endhighlight %}

{% endtabs %}

![Slider ticks](images/ticks/show-ticks-without-interval.png)

### With Interval

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Interval="0.2" 
                  ShowTicks="True">
</sliders:SfSlider>

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Interval = 0.2;
slider.ShowTicks = true;

{% endhighlight %}

{% endtabs %}

![Slider ticks](images/ticks/show-ticks.png)

## Show minor ticks

It is used to represent the number of smaller ticks between two major ticks. For example, if [`Minimum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Minimum) is 0.0 and [`Maximum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Maximum) is 10.0 and [`Interval`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Interval) is 2.0, the slider will render the major ticks at 0.0, 2.0, 4.0 and so on. If [`MinorTicksPerInterval`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MinorTicksPerInterval) is 1, then smaller ticks will be rendered on 1.0 and 3.0 and so on. The default value of [`MinorTicksPerInterval`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MinorTicksPerInterval) property is Zero.

### Without Interval

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Minimum="0"
                  Maximum="10"
                  Value="6"
                  ShowLabels="True" 
                  MinorTicksPerInterval="3" 
		  ShowTicks="True">
</sliders:SfSlider>

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Minimum = 0;
slider.Maximum = 10;
slider.Interval = 2;
slider.MinorTicksPerInterval = 1;
slider.ShowTicks = true;
slider.ShowLabels = true;

{% endhighlight %}

{% endtabs %}

![Slider minor ticks](images/ticks/show-minorticks-without-interval.png)

### With Interval

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Minimum="0"
                  Maximum="10"
                  Value="6"
                  Interval="2" 
                  ShowLabels="True" 
                  MinorTicksPerInterval="1" 
		  ShowTicks="True">
</sliders:SfSlider>

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Minimum = 0;
slider.Maximum = 10;
slider.Interval = 2;
slider.MinorTicksPerInterval = 1;
slider.ShowTicks = true;
slider.ShowLabels = true;

{% endhighlight %}

{% endtabs %}

![Slider minor ticks](images/ticks/show-minor-ticks.png)

## Major ticks color

You can change the active and inactive major ticks color of the slider using the [`ActiveFill`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_ActiveFill) and [`InactiveFill`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_InactiveFill) properties of the [`MajorTickStyle`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MajorTickStyle) class.

The active side of the slider is between the [`Minimum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Minimum) value and the thumb.

The inactive side of the slider is between the thumb and the [`Maximum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Maximum) value.

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Interval="0.2" 
                  ShowTicks="True">
   <sliders:SfSlider.MajorTickStyle>
      <sliders:SliderTickStyle ActiveFill="#EE3F3F" 
                               InactiveFill="#F7B1AE"/>
    </sliders:SfSlider.MajorTickStyle>
</sliders:SfSlider>

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Interval = 0.2;
slider.ShowTicks = true;
slider.MajorTickStyle.ActiveFill = new SolidColorBrush(Color.FromArgb("#EE3F3F"));
slider.MajorTickStyle.InactiveFill = new SolidColorBrush(Color.FromArgb("#F7B1AE"));

{% endhighlight %}

{% endtabs %}

![Slider major ticks color](images/ticks/major-ticks-color.png)

## Minor ticks color

You can change the active and inactive minor ticks color of the slider using the [`ActiveFill`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_ActiveFill) and [`InactiveFill`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_InactiveFill) properties of the [`MinorTickStyle`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MinorTickStyle) class.

The active side of the slider is between the [`Minimum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Minimum) value and the thumb.

The inactive side of the slider is between the thumb and the [`Maximum`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_Maximum) value.

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Minimum="0" 
                  Maximum="10"
                  Interval="2" 
                  ShowTicks="True"
                  ShowLabels="True" 
                  MinorTicksPerInterval="1">
     <sliders:SfSlider.MinorTickStyle>
        <sliders:SliderTickStyle ActiveFill="#EE3F3F" 
                                 InactiveFill="#F7B1AE"/>
      </sliders:SfSlider.MinorTickStyle>
</sliders:SfSlider> 

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Minimum = 0;
slider.Maximum = 10;
slider.Interval = 2;
slider.ShowTicks = true;
slider.ShowLabels = true;
slider.MinorTicksPerInterval = 1;
slider.MinorTickStyle.ActiveFill = new SolidColorBrush(Color.FromArgb("#EE3F3F"));
slider.MinorTickStyle.InactiveFill = new SolidColorBrush(Color.FromArgb("#F7B1AE"));

{% endhighlight %}

{% endtabs %}

![Slider minor ticks color](images/ticks/minor-ticks-color.png)

## Ticks size

You can change the major and minor ticks size of the slider using the [`ActiveSize`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_ActiveSize) and [`InactiveSize`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_InactiveSize) property of the [`MajorTickStyle`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MajorTickStyle) and [`MinorTickStyle`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MinorTickStyle)  classes. The default value is is `Size(2.0, 8.0)`.

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Interval="0.2" 
                  ShowTicks="True" 
		  MinorTicksPerInterval="1">
     <sliders:SfSlider.MinorTickStyle>
         <sliders:SliderTickStyle ActiveSize="2,10" 
                                  InactiveSize="2, 10"/>
     </sliders:SfSlider.MinorTickStyle>
     <sliders:SfSlider.MajorTickStyle>
         <sliders:SliderTickStyle ActiveSize="2,15" 
                                  InactiveSize="2, 15"/>
     </sliders:SfSlider.MajorTickStyle>
</sliders:SfSlider>

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Interval = 0.2;
slider.ShowTicks = true;
slider.MinorTicksPerInterval = 1;
slider.MinorTickStyle.ActiveSize = new Size(2, 10);
slider.MinorTickStyle.InactiveSize = new Size(2, 10);
slider.MajorTickStyle.ActiveSize = new Size(2, 15);
slider.MajorTickStyle.InactiveSize = new Size(2, 15);
    
{% endhighlight %}

{% endtabs %}

![Slider tick size](images/ticks/tick-size.png)

## Ticks offset

You can adjust the space between track and ticks of the slider using the [`Offset`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_Offset) property of the [`MajorTickStyle`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MajorTickStyle) and [`MinorTickStyle`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderBase.html#Syncfusion_Maui_Sliders_SliderBase_MinorTickStyle). The default value of the [`Offset`](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Sliders.SliderTickStyle.html#Syncfusion_Maui_Sliders_SliderTickStyle_Offset) property is `3.0`.

{% tabs %}

{% highlight xaml %}

<sliders:SfSlider Interval="0.2"  
                  ShowTicks="True" 
                  MinorTicksPerInterval="1">
   <sliders:SfSlider.MinorTickStyle>
       <sliders:SliderTickStyle Offset="5"/>
   </sliders:SfSlider.MinorTickStyle>
   <sliders:SfSlider.MajorTickStyle>
       <sliders:SliderTickStyle Offset="6"/>
    </sliders:SfSlider.MajorTickStyle>
</sliders:SfSlider>

{% endhighlight %}

{% highlight C# %}

SfSlider slider = new SfSlider();
slider.Interval = 0.2;
slider.ShowTicks = true;
slider.MinorTicksPerInterval = 1;
slider.MinorTickStyle.Offset = 5;
slider.MajorTickStyle.Offset = 6;

{% endhighlight %}

{% endtabs %}

![Slider tick offset](images/ticks/tick-offset.png)
