title: Flutter
speaker: ethantang
css: [./main.css]

<slide class="aligncenter" image="./img/blue-triangle.png .homepage">

# !![](./public/img/flutter.png .logo) Flutter {.text-shadow}

 <p class="text-intro text-blue animated fadeInUp delay-500 mp-32">
极速构建漂亮的原生应用
</p>

Ethan Tang {.text-intro.animated.flipInX.delay-1200}

<slide class="bg-gradient-v aligncenter" .slide-top>

## Fluter 简介

<p  class="blue text-intro text-left animated fadeInUp delay-500 mp-32">
Flutter 是谷歌的移动 UI 框架，可以快速在 iOS 和 Android 上构建高质量的原生用户界面。 Flutter 可以与现有的代码一起工作。在全世界，Flutter 正在被越来越多的开发者和组织使用，并且 Flutter 是完全免费、开源的。</p>

:::ul{.clients.flexblock.animated.flipInX.delay-1200}

<li>

<figcaption style="padding-top:10px;">
<h3 class="text-blue">快速开发</h3>
毫秒级的热重载，修改后，您的应用界面会立即更新。使用丰富的、完全可定制的 widget 在几分钟内构建原生界面。</figcaption>
</li>

<li>

<figcaption  style="padding-top:10px;">
<h3 class="text-blue">富有表现力和灵活的UI</h3>
快速发布聚焦于原生体验的功能。分层的架构允许您完全自定义，从而实现难以置信的快速渲染和富有表现力、灵活的设计。</figcaption>
</li>

<li>

<figcaption  style="padding-top:10px;">
<h3 class="text-blue">原生性能</h3>
Flutter包含了许多核心的widget，如滚动、导航、图标和字体等，这些都可以在iOS和Android上达到原生应用一样的性能。</figcaption>
</li>

<slide class="bg-white fullscreen " .slide-top>

:::div{.card-50.bg-white}

<figure>
<div class="bg-app"></div>
</figure>

:::div{.flex-content.content-center}

### 常见 App 框架

:::div{.content-center.mp-32}

- 原生 Native{.aligncenter.animated.fadeInUp.slow.delay-400}
- ReactNative{.aligncenter.animated.fadeInUp.slow.delay-800s}
- Weex{.aligncenter.animated.fadeInUp.slow.delay-1200}
- Hybird{.aligncenter.animated.fadeInUp.slow.delay-1600}
- Flutter{.aligncenter.animated.fadeInUp.slow.delay-2s}
- PWA{.aligncenter.animated.fadeInUp.slow.delay-2400}
- ...{.aligncenter.animated.fadeInUp.slow.delay-2800}
  :::
  :::

<slide class="slide bg-black background light" image="./img/th2.jpg  .light">
### 移动应用程序开发的简要历史{.content-center}

<p class="content-center mp-32" style="font-size:3.2rem">移动应用程序开发是一个相对较新的领域。 第三方开发人员已经能够在不到十年的时间内开发移动应用程序，所以工具仍在不断发展并不奇怪。</p>

<slide class="slide-top bg-white background fullscreen" >

:::div{.card-40.bg-white}

!![](./public/img/oem.png .aligncenter.h-300)

:::div{.flex-content.content-left}

### OEM SDKs

<p>Apple iOS SDK于2008年发布，2009年发布Google Android SDK。这两个SDK分别基于不同的语言：Objective-C和Java。</p>
<p>您的应用程序会与平台进行交谈，以创建widgets或访问相机等服务。 widgets呈现给屏幕画布，并且事件被传回给widgets。 这是一个简单的架构，但是您几乎必须为每个平台创建单独的应用程序，因为这些widgets是不同的，更不用说语言。</p>
:::

<slide class="slide-top bg-white background fullscreen" >
:::div{.card-40.bg-white}
!![](./public/img/webview.png .aligncenter.h-300)
:::div{.flex-content.content-left}
### WebView
<p>
第一个跨平台框架基于JavaScript和WebViews。 例如Titanium和一系列相关的框架：PhoneGap，Apache Cordova，Ionic等等。 在苹果发布iOS SDK之前，他们鼓励第三方开发者为iPhone构建webapps，所以用web技术构建跨平台的应用程序是一个显而易见的步骤。
</p>
<p>您的应用程序创建HTML并将其显示在平台上的WebView中。 请注意，像JavaScript这样的语言很难直接与本地代码(like thee services)交谈，所以它们会经历一个在JavaScrip领域和Native 领域之间进行上下文切换的“Bridge”。 因为平台服务通常不是经常被调用的，所以这不会导致太多的性能问题。</p>
:::
:::

<slide class="slide-top bg-white background fullscreen" >
:::div{.card-40.bg-white}
!![](./public/img/reactive.png .aligncenter.h-300)
:::div{.flex-content.content-left}
### Reactive Views
<p>
像ReactJS（和其他）这样的响应式Web框架已经变得流行，主要是因为它们通过使用从响应式编程中借用的编程模式来简化Web视图的创建。 2015年，创建了React Native将响应式视图的诸多好处带给移动应用程序。
</p>
<p>React Native非常受欢迎（并且是值得的），但是由于JavaScript领域访问Native领域的OEM widgets，因此它也必须通过这个桥梁。 通常访问widgets的频率非常高（在动画，转换过程中，或者用户用手指在屏幕上滑动某些东西时，每秒可达60次）。</p>
:::
:::

<slide class="slide-top bg-white background fullscreen" >
:::div{.card-40.bg-white}
!![](./public/img/flutterframe.png .aligncenter.h-300)
:::div{.flex-content.content-left}
### Flutter
<p>
Flutter有一个新的架构，包括外观和感觉不错，快速，可定制和可扩展的Widgets。 没错，Flutter不使用OEM Widgets（或DOM WebViews），它提供了自己的Widgets
</p>
<p>Flutter将Widgets和渲染器从平台移动到应用程序中，从而使其可以自定义和扩展。 Flutter对平台的需求平台是一个画布，在这个画布中，Widgets可以呈现在设备屏幕上，并可以访问事件（触摸，定时器等）和服务（位置，摄像机等）。
Dart程序（绿色）和本地平台代码（iOS或Android蓝色）之间仍然存在一个接口，可以进行数据编码和解码，但这可能比JavaScript Bridge 快几个数量级。</p>
:::
:::

<slide class="slide-top bg-white background fullscreen" >
:::div{.card-30.bg-white}
!![](./public/img/flutterframe2.png .aligncenter.h-300)
:::div{.flex-content.content-left}
### Flutter框架结构
##### Flutter Framework是一个完全由Dart语言构建的SDK，它实现了一整套自底而上的基础库。

1. 底部两层(Foundation 和 Animation、Painting、Gestures)是 Flutter 引擎暴露的底层 UI 库，提供动画、手势及绘制能力。
2. Rendering 层是一个抽象的布局层，它依赖于 dart UI 层。Rendering 层会构建一个 UI 树，当 UI 树有变化时，它会随即计算出有变化的部分，然后更新 UI 树，最终将 UI 树绘制到屏幕上。这个过程类似于 React 中的虚拟 DOM。Rendering 层可以说是 Flutter UI 框架最核心的部分，它除了确定每个 UI 元素的位置、大小之外，还要进行坐标变换和绘制(调用底层 dart:ui)。
3. Widgets 层是 Flutter 提供的一套基础组件库，在基础组件库之上，Flutter 还提供了 Material 和 Cupertino 两种视觉风格的组件库。

<p>Flutter Engine：这是一个完全由 C++实现的 SDK，其中包括了 Skia引擎、Dart运行时和文字排版引擎等。在代码调用 dart:ui库时，调用最终会走到Engine层，然后实现真正的绘制逻辑。</p>
:::
:::

<slide class="slide-top bg-black-blue background light" image="./img/th5.jpg  .dark">
### 一切都是部件（widget）
<p class="mp-32">
在Android和iOS上，部件所对应的就是各种View类。Flutter 采用了不同的概念，部件不仅仅是结构化的元素。Flutter 的部件架构更多地使用了组合，而不是继承，所以部件架构更加强大和灵活。Flutter 官方文档写道：在 Flutter 里，行为也是部件（如 GestureDetector）。InheritedWidget 可用于进行状态管理，AnimatedWidget 可用于构建动画。遵循组合大于集成的原则，Flutter从简单的元部件开始，可以构建出非常复杂的部件。Flutter的Container Widget就是由一系列元部件组成的</p>

<slide class="slide-top bg-black background light" image="./img/th3.jpeg  .dark">
### **Why Dart?**
<p></p>
1. Dart 的性能更好。Dart在 JIT模式下，速度与 JavaScript基本持平。但是 Dart支持 AOT，当以 AOT模式运行时，JavaScript便远远追不上了。速度的提升对高帧率下的视图数据计算很有帮助。
2. Native Binding。在 Android 上，v8 的 Native Binding 可以很好地实现，但是 iOS 上的 JavaScriptCore 不可以，所以如果使用 JavaScript，Flutter 基础框架的代码模式就很难统一了。而 Dart 的 Native Binding 可以很好地通过 Dart Lib 实现。
3. Fuchsia OS，看起来不像原因的一个原因。Fuchsia OS 内置的应用浏览器就是使用 Dart 语言作为 App 的开发语言。而且实际上，Flutter 是 Fuchisa OS 的应用框架概念上的一个子集。（Flutter 源代码和编译工具链也充斥了大量的 Fuchsia 宏）
4. Dart 是类型安全的语言，拥有完善的包管理和诸多特性。Google 召集了如此多个编程语言界的设计专家开发出这样一门语言，旨在取代 JavaScript，所以 Fuchsia OS 内置了 Dart。Dart 可以作为 embedded lib 嵌入应用，而不用只能随着系统升级才能获得更新，这也是优势之一。

<slide class="slide-top bg-white background light" image="img/hummingbird.png .right-top .hum">

## 不止步于移动平台{.text-intro}

<p>Hummingbird 是一个基于 Web 实现的 Flutter 运行时环境。它利用了 Dart 语言能被编译成 JavaScript 的特性。这个项目让 Flutter 应用程序能够无需改动地运行在标准 Web 平台。</p>
!![](./public/img/hum.gif .aligncenter.h-400)

<slide class="slide-top bg-black-blue" image="./img/th4.jpg  .dark">

### 目前的不足

<p class="mp-32">Flutter还很年轻，所以肯定会存在一些局限和已知问题，而且未知的问题也会越来越多</p>

1. 框架年轻，轮子较少
2. 框架成熟度及稳定性仍有待完善。
3. 首屏渲染时间较长
4. iOS 包体积过大
5. 无法保存实例状态（Android）。所以，如果应用在后台被终止，应用状态就会丢失。
6. 热更新技术缺失，原理上可行。
