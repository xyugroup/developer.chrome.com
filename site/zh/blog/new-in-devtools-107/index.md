---
layout: 'layouts/blog-post.njk'
title: 'DevTools 新功能（Chrome 107）'
authors:
  - jecelynyeen
date: 2022-09-20
description: 'Customize keyboard shortcuts, highlight C/C++ objects in the Memory Inspector and more.'
hero: 'image/dPDCek3EhZgLQPGtEG3y0fTn4v82/wchUXKvGXO7WtfDYmrsj.svg'
alt: ''
tags:
  - new-in-devtools
  - devtools
  - chrome-107
draft: true
---

*感谢 [Poong Zui Yong](https://www.linkedin.com/in/zui-yong-poong-1b507b14/) 提供的翻译*

{% include 'partials/devtools/zh/banner.md' %}

<!-- Translation instructions:
  1. Remove the "draft: true" tag above when submitting PR
  2. Provide translations under each of the English commented original content
  3. Translate the "description" tag above
  4. Translate all the <img> alt text
  5. Update the whats-new.md file -->

<!-- Content starts here -->

<!-- ## 在DevTools中客制化键盘快捷键 {: #shortcuts } -->

<!-- 你现在可以在DevTools中客制化你喜爱使用的命令. -->

<!-- 去到 **Settings（设置）** > **Shortcuts(快捷键）**, 将鼠标放置在一个命令上并点击 **Edit（编辑）** 按钮 (钢笔图标) 来对键盘快捷键进行客制化。 你也可以创建组合键 chords (a.k.a 多键快捷键)。  -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/973EfWpxwGOdEF1nN1vv.png", alt="在DevTools中客制化键盘快捷键", width="800", height="516" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/d061128ff63a97ab2c6c0d2b5e655e6fcbed829c #}

Chromium issues: [1335274](https://crbug.com/1335274), [174309](https://crbug.com/174309)


<!-- ## 使用快捷键对光亮与暗黑主题进行快速切换 {: #toggle-themes } -->

<!-- 便利地设置一个快捷键来进行快速切换 [光亮与暗黑主题](/docs/devtools/rendering/emulate-css/#emulate-css-media-feature-prefers-color-scheme) . 这个行为并没有被预设为任何键盘快捷键 -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/7oGdE2eRsgwokWXW9XvA.png", alt="使用快捷键对光亮与暗黑主题进行快速切换", width="800", height="576" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/4853b34457f43e41ae9cebc7dfc97c0b734f463a #}
{# https://chromium.googlesource.com/devtools/devtools-frontend/+/029ac9db0b7e7d08945bcf7a16b407bde50183a1 #}

Chromium issues: [1280398](https://crbug.com/1280398), [1226363](https://crbug.com/1226363)


<!-- ## 在记忆检查器中强标C/C++对象 {: #memory } -->

<!-- The [Memory Inspector](/docs/devtools/memory-inspector/) 强标所有属于C/C++记忆对象的字节。 -->

<!-- 在围绕在网络组件记忆中辨别一个对象的字节一直是一个痛点。 您需要知道对象体积并从对象初始时就可以计数。  -->

<!-- 使用这个功能,  可以帮助您只是它们从围绕记忆中分离出来。 参阅 [延伸C/C++侦错的记忆检查器](/blog/memory-inspector-extended-cpp/)来了解这个改良 -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/zqOv2zJTc8ucoeDmQiTo.png", alt="强标所有属于C/C++记忆对象的字节。", width="800", height="527" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/d5f3befb47eaaa373d697b42dec6f179baf9d42c #}
{# https://chromium.googlesource.com/devtools/devtools-frontend/+/c4e6bdb4321cbc0b783647e855a616096beaabfd #}

Chromium issue: [1336568](https://crbug.com/1336568)


<!-- ## 支持HAR文件导入的完整初始者讯息 {: #har } -->

<!-- 得到完整 **Initiator** 讯息现在i现有版本是可行的  [HAR文件导入](/docs/devtools/network/reference/#save-as-har). 在之前的版本, **Network（网络）** 界面在导入HAR 文件时只显示部分初始者讯息。 -->

<!-- 初始这讯息帮助开发者追踪网络请求的源头并确认网络相关问题。  -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/cthh3ZrpDwo4LJiaY4Uo.png", alt="支持HAR文件导入的完整初始者讯息", width="800", height="376" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/3a659b0711f52a2e200395b85f16ed9f266d1571 #}

Chromium issue: [1343185](https://crbug.com/1343185)



<!-- ## 点击`Enter(输入）`键时开始DOM搜索 {: #search-type } -->

<!-- 你现在可以禁止**Search as you type （输入即搜索）** 设置来指示工具在你点击<kbd>Enter</kbd>的时候开始搜索DOM  -->

<!-- 在**Elements（元素）** 界面中, 使用<kbd>Control</kbd>或<kbd>Command</kbd> + <kbd>F</kbd>来切换搜索栏 . 当你在搜索输入栏中输入一个查询时， DOM会跳到第一个适配元素和并预标准。  -->

<!-- 对于用户, 特别是经常使用长查询语句的测试者， 这种行为并不是理想的。DOM 树有可能在用户输入长查询语句的过程中进行多次跳跃 (e.g. `//div[@id="example"]`). 这个行为制造了无用的操作 . -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/KgTTYf8XaKkHQ2udJc33.png", alt="DOM search.", width="800", height="505" %}

<!-- 来到 **Settings（设置）** > **Preferences（喜好）**, 禁止 **Search as you type（输入即搜索）**. 使用这个设置， 搜索只会在你点击<kbd>Enter</kbd>时才发生 -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/HBLiQ5e60g5urU8UT5J7.png", alt="Search as you type setting.", width="800", height="449" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/b4643a4703b4a26945d1446eedc907ac81373e23 #}

Chromium issue: [1344526](https://crbug.com/1344526)


<!-- ## 在`align-content（对齐内容）`功能中的CSS Flexbox属性面板中显示`start（开始）` 和 `结束` 图示 {: #flexbox } -->

<!-- 在 **Styles（风格）** 界面中, 对CSS类的 `align-content` 属性进行`display: flex` 或 `display: inline-flex`的编辑。 `start（开始）` 和 `end（结束）` 图示会在自动完成的下拉清单中显示。 -->

{% Img src="image/dPDCek3EhZgLQPGtEG3y0fTn4v82/fo10I2mt6bQ357itnYhl.png", alt="align-content flexbox properties.", width="800", height="424" %}

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/ce2b426818106768d4e6d907cc1f4cd3b9636ca6 #}

Chromium issue: [1139945](https://crbug.com/1139945)


<!-- ## 其他亮点 {: #misc } -->

<!-- - 在**Console**界面中显示争取的修改讯息数量。 在以前的版本, 这个技术在请客console讯息时不会被刷新。  ([1343311](https://crbug.com/1343311)) -->

{# https://chromium.googlesource.com/devtools/devtools-frontend/+/5dd8494912fa43dfe998c9764ceb1e1763784617 #}


{% include 'partials/devtools/zh/reach-out.md' %}
{% include 'partials/devtools/zh/whats-new.md' %}
