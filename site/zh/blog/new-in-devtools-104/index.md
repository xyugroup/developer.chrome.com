---
layout: "layouts/blog-post.njk"
title: "DevTools 新功能（Chrome 104）"
authors:
  - jecelynyeen
date: 2022-07-13
updated: 2022-07-13
description: "Restart frame during debugging, slow replay options in the Recorder panel, and more."
描述：“调试时的框架重启，记录面板中的慢速复盘选项，以及其他功能”
hero: 'image/dPDCek3EhZgLQPGtEG3y0fTn4v82/VojSLwN9rFRkALzi6RZh.jpg'
alt: ''
tags:
  - new-in-devtools
  - devtools
  - chrome-104
draft: true
---

*感谢 [流浪大法师 @liuliangsir](https://github.com/liuliangsir) 提供的翻译*。

{% include 'partials/devtools/zh/banner.md' %}

<!-- start: translation instructions -->
<!-- + 1. Remove the "draft: true" tag above when submitting PR -->
<!-- + 2. Provide translations under each of the English commented original content -->
<!-- + 3. Translate the "description" tag above -->
<!-- + 4. Translate all the <img> alt text -->
<!-- + 5. Update the whats-new.md file -->

<!-- ## Restart frame during debugging {: #restart-frame } -->
<!-- ## 调试时的框架重启 {: #框架重启 } -->


<!-- The **框架重启** 功能回归了! 你可以重新执行前部的代码当你在停止在一个功能的某部分时. 为了维护系统的稳定性， ”框架功能” 曾经在 Chrome 92 的时候被弃用。  -->

<!-- 在这个 [例子](https://jec.fyi/), 调试器一开始的时候停置在断点（343行） ，靠近`toggleColorScheme`功能的尾端。 为了从`toggleColorSchme`功能的起点处重启调试器 , 扩张调试器面板中的**调用栈** 部分, 在 `toggleColorScheme`上右点击 并选取**框架重启**.  -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/uBcTkuIaoHHTgJCiGNED.png", alt="调试时的框架重启", width="800", height="499" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/7f6749f5cbbfc7d3c89cb2b6b3557d0ff33536ad #}

Chromium issue: [1303521](https://crbug.com/1303521)


<!-- ## 记录面板中的慢速复盘选项 {: #重置 } -->

<!-- 你可以对用户流程进行慢速复盘 - 可以选择慢、很慢和极慢。 这个功能让你可以更好地观察到屏幕上复盘的每一个步骤。 -->

<!-- [Open](/docs/devtools/recorder/#open) the **记录** 面板和 [开始一个新的记录](/docs/devtools/recorder/#record). 当一个记录被完成后， 点击“复盘”下拉按钮。 选择一个速度以开始一个复盘 -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/yLIIMlaew0EWfEYdDbXJ.png", alt="记录面板中的慢速复盘选项", width="800", height="486" %}

Chromium issue: [1306756](https://crbug.com/1306756)


<!-- ## 为记录面板创建一个挂件 {: #记录挂件 } -->

<!-- 你可以使用你喜好的格式来创建或安装一个Chrome 挂件的复盘脚本 . 见 [复盘挂件软件编程界面（API）](/docs/extensions/reference/devtools_recorder/) 文档以学习如何创建一个挂件. -->

<!-- 安装一个演示挂件, 参考 [这些步骤](https://github.com/puppeteer/replay#create-a-chrome-extension-for-recorder-available-from-chrome-104-onwards) 文档中的大纲.  -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/xRO1d79tBe0ILcBoD0oh.png", alt="属于记录面板的客制化挂件", width="800", height="486" %}

Chromium issue: [1325751](https://crbug.com/1325751)


<!-- ## 在源面板中选择撰写/部署选项来对文件进行分组 {: #被撰写-被部署 } -->

<!-- 在源面板中加入新的 **撰写/部署选项来对文件进行分组** 选项来整理文件。 当使用框架(例如: React, Angular)开发网络应用程序的时候 , 构建工具生成的缩小文件(例如： Webpack, Vite)会导致源文档的浏览变得困难。-->
 
<!-- 通过复选框，你可以将文件组合成2个种类，以方便快速的文件搜索: -->
 
<!-- - **被撰写**. 如同你在集成开发环境IDE中浏览源文档。DevTools 根据源图产生那些文件 (由你的构建工具提供).
- **被部署**. 浏览器阅读的真正文档。那些文档通常被缩图. -->
 
<!-- 自己去测试这些 [React 演示](https://reactjs.org/)! -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/5E1qbkl0Gx1REx7FdqEr.png", alt="源面板中的撰写/部署功能对文件进行整理", width="800", height="521" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/6bc65d0595702fc826ca87e2cfe519a134b62d90 #}
 
Chromium issue: [960909](https://crbug.com/960909)


<!-- ## New User Timings track in the Performance insights panel {: #performance } -->

<!-- Visualize `performance.measure()` marks in your recording with the new **User Timings** track in the **Performance insights** panel. -->

<!-- For example, this [web page](https://jec.fyi/demo/perf-measure) uses the [`performance.measure()`](https://web.dev/usertiming/#calculating-measurements-with-measure()) method to calculate the elapsed time of text loading. -->

<!-- When you start [measuring the page load](/docs/devtools/performance-insights/#record), the **User Timings** track shows in the recording. Click on the timings item to view its details on the side pane. -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/nxPCp6UaiGWJCWWx4Laa.png", alt="User Timings track in the Performance insights panel", width="800", height="499" %}

Chromium issue: [1322808](https://crbug.com/1322808)

 
<!-- ## Reveal assigned slot of an element {: #slot } -->

<!-- Slotted elements in the **Elements** panel have a new `slot` badge. When debugging layout issues, use this feature to identify the element which affects the node's layout quicker.  -->

<!-- This [example](https://mdn.github.io/web-components-examples/slotted-pseudo-element/) contains cards with a few named slots. Inspect the `person-occupation` slot of a card, click the `slot` badge next to it to reveal its assigned slot. -->

<!-- [Learn](https://developer.mozilla.org/docs/Web/Web_Components/Using_templates_and_slots) how to use [<template>](https://developer.mozilla.org/docs/Web/HTML/Element/template) and [<slot>](https://developer.mozilla.org/docs/Web/HTML/Element/slot) elements to create a flexible template that can then be used to populate the shadow DOM of a web component. -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/7uQGHp9WoMCG1RIAkgIF.png", alt="Reveal assigned slot of an element", width="800", height="486" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/164e238dabefc08018318a981131eedf2e81736b #}

Chromium issue: [1018906](https://crbug.com/1018906)


<!-- ## Simulate hardware concurrency for Performance recordings {: #simulate } -->
 
<!-- The new **Hardware concurrency** setting in the **Performance** panel allows developers to configure the value reported by `navigator.hardwareConcurrency`. -->
 
<!-- Some applications use `navigator.hardwareConcurrency` to control the degree of parallelism of their application, for example, to control Emscripten pthread pool size. With this feature, developers can test their application performance with different core counts. -->
 
{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/PyykGRv29FZbBKJAwWOW.png", alt="Simulate hardware concurrency for Performance recordings", width="800", height="536" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/b26de259d74a45e700d989ad9178c5e3a8b73145 #}
 
Chromium issue: [1297439](https://crbug.com/1297439)


<!-- ## Preview non-color value when autocompleting CSS variables {: #css-var } -->

<!-- When autocompleting CSS variables, DevTools now populates the non-color variable with a meaningful value so that you can preview what kind of change the value will have on the node. -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/V4slwNtX9HwLPdAyr8JF.png", alt="Preview non-color value when autocompleting CSS variables", width="800", height="431" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/977cc58cb5654a2b68142ef8ac1b3f9ac2822694 #}

Chromium issue: [1285091](https://crbug.com/1285091)

        
<!-- ## Identify blocking frames in the Back/forward cache pane {: #bfcache } -->

<!-- The [Back/forward cache](/docs/devtools/application/back-forward-cache/) pane in the **Application** panel has new **frames** section to help you identify blocking frames that may be preventing the page from being eligible for bfcache. -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/UaRYEoYYoXhjSIn9seYK.png", alt="Identify blocking frames in the Back/forward cache pane", width="800", height="486" %}
 
{# https://chromium.googlesource.com/devtools/devtools-frontend/+/897799b24fff0639d483111dd2d957288ba2bd06 #}
 
Chromium issue: [1288158](https://crbug.com/1288158) 
 
 
<!-- ## Improved autocomplete suggestions for JavaScript objects {: #autocomplete } -->

<!-- The the autocompletion for JavaScript object properties now display based on this order: -->

<!-- 1. Own enumerable properties
2. Own non-enumerable properties
3. Inherited enumerable properties
4. Inherited non-enumerable properties -->

<!-- Previously, developers found it harder to find relevant properties because the suggestion only favored own properties over inherited properties, and all inherited properties were given equal priority. -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/IvFTcOWrBOTTMRHqn8u4.png", alt="Improved autocomplete suggestions for JavaScript objects", width="800", height="563" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/cee5205ae93c95b1dce49e220b9ebfa8c998d5a6 #}
 
Chromium issue: [1299241](https://crbug.com/1299241)

 
<!-- ## Sourcemaps improvements {: #sourcemaps } -->
 
<!-- Here are a few fixes on sourcemaps to improve the overall debugging experience: -->
 
<!-- - Breakpoints now work in inline `<script>` with sourceURL annotations. -->
<!-- - The debugger now resolves block scoped variables in the **Scope** view with source maps. -->
  {% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/gv9cGnDMF7OVlXPWntII.png", alt="Resolves block scoped variables", width="800", height="532" %}
<!-- - The debugger now resolves variables in arrow functions in the **Scope** view with source maps. -->
  {% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/CZk0xjwMQAqknkW5G4Xf.png", alt="Resolves variables in arrow functions", width="800", height="479" %}

Chromium issues: [1329113](https://crbug.com/1329113), [1322115](https://crbug.com/1322115)
 
 
<!-- ## Miscellaneous highlights {: #misc } -->
 
<!-- These are some noteworthy fixes in this release: -->
 
<!-- - Fixed the **Auto-completion** setting for the **Sources** panel. Previously, the auto-complete always on even the setting is disabled. ([1323286](https://crbug.com/1323286)) -->
<!-- - Updated the **Manifest** tab in the **Application** panel to parse the latest color scheme format. ([1318305](https://crbug.com/1318305)) -->
<!-- - Improved the suggestions for the `<script async>` rendering blocking issues in the **Performance insights** panel. Previously,  DevTools suggested to `add async attribute to the script tag` even though the script is already marked as async. ([1334096](https://crbug.com/1334096)) -->
<!-- - The **Performance insights** panel now detects iframes as potential causes for layout shifts. You can view the iframe details in the **Details** pane. ([1328873](https://crbug.com/1328873)) -->
<!-- - When [open file](/docs/devtools/resources/#open) in the **Command menu**, the authored files (files generated by sourcemaps) are now ranked higher so they appear above similarly named deployed scripts. ([1312929](https://crbug.com/1312929))  -->


{% include 'partials/devtools/zh/reach-out.md' %}
{% include 'partials/devtools/zh/whats-new.md' %}
