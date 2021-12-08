---
layout: post
title: Getting started with .NET MAUI Range Slider control | Syncfusion
description: This section explains about the getting started with Syncfusion MAUI Range Slider (SfRangeSlider) control.
platform: maui
control: SfRangeSlider
documentation: ug
---

# Getting Started with .NET MAUI Range Slider

This section explains the steps required to add the range slider control and its elements such as numeric and date values, ticks, labels and tooltip. This section covers only basic features needed to know to get started with Syncfusion Range Slider.

## Creating an application with .NET MAUI Slider

1. Create a new .NET MAUI application in Visual Studio.
2. Syncfusion .NET MAUI components are available in [nuget.org](https://www.nuget.org/). To add SfRangeSlider to your project, open the NuGet package manager in Visual Studio, search for Syncfusion.Maui.Sliders and then install it.
3. To initialize the control, import the Range Slider namespace.
4. Initialize SfRangeSlider.

{% tabs %}

{% highlight xaml %}

<ContentPage
    . . .
    xmlns:slider="clr-namespace:Syncfusion.Maui.Sliders;assembly=Syncfusion.Maui.Sliders">
    <Grid>
        <slider:SfRangeSlider/>
    </Grid>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Sliders;

namespace SliderGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            SfRangeSlider rangeSlider = new SfRangeSlider();
        }
    }
}

{% endhighlight %}

{% endtabs %}

## Register the handler

Syncfusion.Maui.Core nuget is a dependent package for all Syncfusion controls of .NET MAUI. In the MauiProgram.cs file, register the handler for Syncfusion core.

{% highlight C# %}

using Microsoft.Maui;
using Microsoft.Maui.Hosting;
using Microsoft.Maui.Controls.Compatibility;
using Microsoft.Maui.Controls.Hosting;
using Microsoft.Maui.Controls.Xaml;
using Syncfusion.Maui.Core.Hosting;

namespace SliderGettingStarted
{
    public static class MauiProgram
    {
        public static MauiApp CreateMauiApp()
        {
            var builder = MauiApp.CreateBuilder();
            builder
            .UseMauiApp<App>()
            .ConfigureSyncfusionCore()
            .ConfigureFonts(fonts =>
            {
                fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");
            });

            return builder.Build();
        }
    }
}


{% endhighlight %}

## Initialize range slider

Import the `SfRangeSlider` namespace and initialize the range slider as shown below.

{% tabs %}

{% highlight xaml %}

<ContentPage
    . . .
    xmlns:slider="clr-namespace:Syncfusion.Maui.Sliders;assembly=Syncfusion.Maui.Sliders">
    <Grid>
        <slider:SfRangeSlider />
    </Grid>
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Sliders;

namespace SliderGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            SfRangeSlider rangeSlider = new SfRangeSlider();
        }
    }
}

{% endhighlight %}

{% endtabs %}

## Set date value

Set the 'DateTime' values to the `Minimum`, `Maximum`, and `Value` properties to display date labels in the range slider.

## Enable ticks

The `ShowTicks` property enables ticks in the range slider, while the `MinorTicksPerInterval` property enables minor ticks between the major ticks.

## Orientation

The `Orientation` property allows you to show the range slider in both horizontal and vertical directions. The default value of the `Orientation` property is `Horizontal`.

## Inverse the slider

You can invert the range slider using the `IsInversed` property. The default value of the `IsInversed` property is `False`.

## Add prefix/suffix to labels

You can add prefix or suffix to the labels using the `NumberFormat` or `DateFormat` properties.

N> The format type (numeric or date) of the range slider is determined based on the values specified in `Minimum`, `Maximum` properties.