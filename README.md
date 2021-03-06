[![](https://jitpack.io/v/swiggy/slither.svg)](https://jitpack.io/#swiggy/slither)
[![Build Status](https://travis-ci.org/Swiggy/slither.svg?branch=master)](https://travis-ci.org/Swiggy/slither)


<img src="./media/slither_logo_text.png" alt="Slither logo" title="slither" align="right" height="60" />

# Slither

A widget that helps you put facebook-shimmer in litho widgets 

## Getting Started

### Prerequisites

You should have some experience with facebook litho and facebook shimmer libraries

### Installing

Add following line to you project's root .gradle file

```
allprojects {
    repositories {
        //other repositories
        maven { url 'https://jitpack.io' }
    }
}
```

Add following line to your module(usually app) .gradle file

```
implementation 'com.github.swiggy:slither:1.0.3'
```

If you are using support library before androidx you can use following instead

```
implementation 'com.github.swiggy:slither:1.0.3:android28@aar'
```

Note: I am assuming that you are already working with litho ;)

How to use the widget

```
Slither.create(componentContext)
                .component(
                    Image.create(componentContext)
                        .drawableRes(R.drawable.slither_logo)
                        .build()
                )
                .shimmer(
                    Shimmer
                        .AlphaHighlightBuilder()
                        .setBaseAlpha(0.4f)
                        .setClipToChildren(true)
                        .setDropoff(0.8f)
                        .setTilt(15f)
                        .setDuration(2000).build()
                ).build()
```

 <img src="./media/example1.gif" alt="Example" title="example" align="center"/>

Check links for facebook shimmer below to know about more shimmer modifications

## Built With

* [Facebook Litho](https://fblitho.com/)
* [Facebook Shimmer](http://facebook.github.io/shimmer-android/)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.md](LICENSE.md) file for details
