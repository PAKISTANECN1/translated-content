---
title: 事件参考
slug: Web/Events
tags:
  - Event
  - Web
  - 事件
  - 参考
  - 总览
translation_of: Web/Events
---
<p>发送 DOM 事件是为了将发生的相关事情通知代码。每个事件都是继承自{{DOMxRef("Event")}} 接口的对象，可以包括自定义的成员属性及函数用于获取事件发生时相关的更多信息。事件可以表示任何从基本的用户交互、到发生在渲染模型自动通知的任何事情。</p>

<p>本文提供了一个可以发送的事件的列表；一些是官方标准中的标准事件，另一些则是在特定浏览器内部使用的事件；例如，列出的 Mozilla 特定事件，使<a href="/zh-CN/docs/Mozilla/Add-ons">附加组件</a>可以借助它们与浏览器进行交互。</p>

<h2 id="最常见的类别">最常见的类别</h2>

<table class="standard-table">
 <caption>
 <h3 id="资源事件">资源事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("error")}}</td>
   <td>资源加载失败时。</td>
  </tr>
  <tr>
   <td>{{Event("abort")}}</td>
   <td>正在加载资源已经被中止时。</td>
  </tr>
  <tr>
   <td>{{Event("load")}}</td>
   <td>资源及其相关资源已完成加载。</td>
  </tr>
  <tr>
   <td>{{Event("beforeunload")}}</td>
   <td>window，document 及其资源即将被卸载。</td>
  </tr>
  <tr>
   <td>{{Event("unload")}}</td>
   <td>文档或一个依赖资源正在被卸载。</td>
  </tr>
 </tbody>
</table>

<h3 id="网络事件">网络事件</h3>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("online")}}</td>
   <td>浏览器已获得网络访问。</td>
  </tr>
  <tr>
   <td>{{Event("offline")}}</td>
   <td>浏览器已失去网络访问。</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="焦点事件">焦点事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("focus")}}</td>
   <td>元素获得焦点（不会冒泡）。</td>
  </tr>
  <tr>
   <td>{{Event("blur")}}</td>
   <td>元素失去焦点（不会冒泡）。</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="WebSocket_事件">WebSocket 事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/open_websocket">open</a></code></td>
   <td>WebSocket 连接已建立。</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/message_websocket">message</a></code></td>
   <td>通过 WebSocket 接收到一条消息。</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>WebSocket 连接异常被关闭（比如有些数据无法发送）。</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/close_websocket">close</a></code></td>
   <td>WebSocket 连接已关闭。</td>
  </tr>
 </tbody>
</table>

<table>
 <caption>
 <h3 id="会话历史事件">会话历史事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("pagehide")}}</td>
   <td>A session history entry is being traversed from.</td>
  </tr>
  <tr>
   <td>{{Event("pageshow")}}</td>
   <td>A session history entry is being traversed to.</td>
  </tr>
  <tr>
   <td>{{Event("popstate")}}</td>
   <td>A session history entry is being navigated to (in certain cases).</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="CSS_动画事件">CSS 动画事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("animationstart")}}</td>
   <td>某个 CSS 动画开始时触发。</td>
  </tr>
  <tr>
   <td>{{Event("animationend")}}</td>
   <td>某个 CSS 动画完成时触发。</td>
  </tr>
  <tr>
   <td>{{Event("animationiteration")}}</td>
   <td>某个 CSS 动画完成后重新开始时触发。</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="CSS_过渡事件">CSS 过渡事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("transitionstart")}}</td>
   <td>A <a href="/zh-CN/docs/Web/CSS/CSS_Transitions">CSS transition</a> has actually started (fired after any delay).</td>
  </tr>
  <tr>
   <td>{{Event("transitioncancel")}}</td>
   <td>CSS 过渡被取消</td>
  </tr>
  <tr>
   <td>{{Event("transitionend")}}</td>
   <td>CSS 过渡已经完成</td>
  </tr>
  <tr>
   <td>{{Event("transitionrun")}}</td>
   <td>A <a href="/zh-CN/docs/Web/CSS/CSS_Transitions">CSS transition</a> has begun running (fired before any delay starts).</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="表单事件">表单事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("reset")}}</td>
   <td>点击重置按钮时</td>
  </tr>
  <tr>
   <td>{{Event("submit")}}</td>
   <td>点击提交按钮</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="打印事件">打印事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">时间名称</th>
   <th scope="col">何时触发</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("beforeprint")}}</td>
   <td>打印机已经就绪时触发</td>
  </tr>
  <tr>
   <td>{{Event("afterprint")}}</td>
   <td>打印机关闭时触发</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="文本写作事件">文本写作事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("compositionstart")}}</td>
   <td>The composition of a passage of text is prepared (similar to keydown for a keyboard input, but works with other inputs such as speech recognition).</td>
  </tr>
  <tr>
   <td>{{Event("compositionupdate")}}</td>
   <td>A character is added to a passage of text being composed.</td>
  </tr>
  <tr>
   <td>{{Event("compositionend")}}</td>
   <td>The composition of a passage of text has been completed or canceled.</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="视图事件">视图事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("fullscreenchange")}}</td>
   <td>An element was turned to fullscreen mode or back to normal mode.</td>
  </tr>
  <tr>
   <td>{{Event("fullscreenerror")}}</td>
   <td>It was impossible to switch to fullscreen mode for technical reasons or because the permission was denied.</td>
  </tr>
  <tr>
   <td>{{Event("resize")}}</td>
   <td>The document view has been resized.</td>
  </tr>
  <tr>
   <td>{{Event("scroll")}}</td>
   <td>The document view or an element has been scrolled.</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="剪贴板事件">剪贴板事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("cut")}}</td>
   <td>已经剪贴选中的文本内容并且复制到了剪贴板。</td>
  </tr>
  <tr>
   <td>{{Event("copy")}}</td>
   <td>已经把选中的文本内容复制到了剪贴板。</td>
  </tr>
  <tr>
   <td>{{Event("paste")}}</td>
   <td>从剪贴板复制的文本内容被粘贴。</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="键盘事件">键盘事件</h3>
 </caption>
 <tbody>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
  <tr>
   <td>{{Event("keydown")}}</td>
   <td>按下任意按键。</td>
  </tr>
  <tr>
   <td>{{Event("keypress")}}</td>
   <td>除 Shift、Fn、CapsLock 外的任意键被按住。（连续触发。）</td>
  </tr>
  <tr>
   <td>{{Event("keyup")}}</td>
   <td>释放任意按键。</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="鼠标事件">鼠标事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("auxclick")}}</td>
   <td>A pointing device button (ANY non-primary button) has been pressed and released on an element.</td>
  </tr>
  <tr>
   <td>{{Event("click")}}</td>
   <td>在元素上按下并释放任意鼠标按键。</td>
  </tr>
  <tr>
   <td>{{Event("contextmenu")}}</td>
   <td>右键点击（在右键菜单显示前触发）。</td>
  </tr>
  <tr>
   <td>{{Event("dblclick")}}</td>
   <td>在元素上双击鼠标按钮。</td>
  </tr>
  <tr>
   <td>{{Event("mousedown")}}</td>
   <td>在元素上按下任意鼠标按钮。</td>
  </tr>
  <tr>
   <td>{{Event("mouseenter")}}</td>
   <td>指针移到有事件监听的元素内。</td>
  </tr>
  <tr>
   <td>{{Event("mouseleave")}}</td>
   <td>指针移出元素范围外（不冒泡）。</td>
  </tr>
  <tr>
   <td>{{Event("mousemove")}}</td>
   <td>指针在元素内移动时持续触发。</td>
  </tr>
  <tr>
   <td>{{Event("mouseover")}}</td>
   <td>指针移到有事件监听的元素或者它的子元素内。</td>
  </tr>
  <tr>
   <td>{{Event("mouseout")}}</td>
   <td>指针移出元素，或者移到它的子元素上。</td>
  </tr>
  <tr>
   <td>{{Event("mouseup")}}</td>
   <td>在元素上释放任意鼠标按键。</td>
  </tr>
  <tr>
   <td>{{Event("pointerlockchange")}}</td>
   <td>鼠标被锁定或者解除锁定发生时。</td>
  </tr>
  <tr>
   <td>{{Event("pointerlockerror")}}</td>
   <td>可能因为一些技术的原因鼠标锁定被禁止时。</td>
  </tr>
  <tr>
   <td>{{Event("select")}}</td>
   <td>有文本被选中。</td>
  </tr>
  <tr>
   <td>{{Event("wheel")}}</td>
   <td>滚轮向任意方向滚动。</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="拖放事件">拖放事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("drag")}}</td>
   <td>正在拖动元素或文本选区（在此过程中持续触发，每 350ms 触发一次）</td>
  </tr>
  <tr>
   <td>{{Event("dragend")}}</td>
   <td>拖放操作结束。（松开鼠标按钮或按下 Esc 键）</td>
  </tr>
  <tr>
   <td>{{Event("dragenter")}}</td>
   <td>被拖动的元素或文本选区移入有效释放目标区</td>
  </tr>
  <tr>
   <td>{{Event("dragstart")}}</td>
   <td>用户开始拖动 HTML 元素或选中的文本</td>
  </tr>
  <tr>
   <td>{{Event("dragleave")}}</td>
   <td>被拖动的元素或文本选区移出有效释放目标区</td>
  </tr>
  <tr>
   <td>{{Event("dragover")}}</td>
   <td>被拖动的元素或文本选区正在有效释放目标上被拖动（在此过程中持续触发，每 350ms 触发一次）</td>
  </tr>
  <tr>
   <td>{{Event("drop")}}</td>
   <td>元素在有效释放目标区上释放</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="媒体事件">媒体事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("audioprocess")}}</td>
   <td>The input buffer of a {{DOMxRef("ScriptProcessorNode")}} is ready to be processed.</td>
  </tr>
  <tr>
   <td>{{Event("canplay")}}</td>
   <td>The browser can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content.</td>
  </tr>
  <tr>
   <td>{{Event("canplaythrough")}}</td>
   <td>The browser estimates it can play the media up to its end without stopping for content buffering.</td>
  </tr>
  <tr>
   <td>{{Event("complete")}}</td>
   <td>The rendering of an {{DOMxRef("OfflineAudioContext")}} is terminated.</td>
  </tr>
  <tr>
   <td>{{Event("durationchange")}}</td>
   <td>The <code>duration</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{Event("emptied")}}</td>
   <td>The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the <a href="/zh-CN/docs/XPCOM_Interface_Reference/NsIDOMHTMLMediaElement"><code>load()</code></a> method is called to reload it.</td>
  </tr>
  <tr>
   <td>{{Event("ended")}}</td>
   <td>Playback has stopped because the end of the media was reached.</td>
  </tr>
  <tr>
   <td>{{Event("loadeddata")}}</td>
   <td>The first frame of the media has finished loading.</td>
  </tr>
  <tr>
   <td>{{Event("loadedmetadata")}}</td>
   <td>The metadata has been loaded.</td>
  </tr>
  <tr>
   <td>{{Event("pause")}}</td>
   <td>Playback has been paused.</td>
  </tr>
  <tr>
   <td>{{Event("play")}}</td>
   <td>Playback has begun.</td>
  </tr>
  <tr>
   <td>{{Event("playing")}}</td>
   <td>Playback is ready to start after having been paused or delayed due to lack of data.</td>
  </tr>
  <tr>
   <td>{{Event("ratechange")}}</td>
   <td>The playback rate has changed.</td>
  </tr>
  <tr>
   <td>{{Event("seeked")}}</td>
   <td>A <em>seek</em> operation completed.</td>
  </tr>
  <tr>
   <td>{{Event("seeking")}}</td>
   <td>A <em>seek</em> operation began.</td>
  </tr>
  <tr>
   <td>{{Event("stalled")}}</td>
   <td>The user agent is trying to fetch media data, but data is unexpectedly not forthcoming.</td>
  </tr>
  <tr>
   <td>{{Event("suspend")}}</td>
   <td>Media data loading has been suspended.</td>
  </tr>
  <tr>
   <td>{{Event("timeupdate")}}</td>
   <td>The time indicated by the <code>currentTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{Event("volumechange")}}</td>
   <td>The volume has changed.</td>
  </tr>
  <tr>
   <td>{{Event("waiting")}}</td>
   <td>Playback has stopped because of a temporary lack of data.</td>
  </tr>
 </tbody>
</table>

<table class="standard-table">
 <caption>
 <h3 id="进度事件">进度事件</h3>
 </caption>
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Fired When</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/API/XMLHttpRequest/abort_event">abort</a></code></td>
   <td>Progression has been terminated (not due to an error).</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>Progression has failed.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/API/XMLHttpRequest/load_event">load</a></code></td>
   <td>Progression has been successful.</td>
  </tr>
  <tr>
   <td>{{Event("loadend")}}</td>
   <td>Progress has stopped (after "error", "abort" or "load" have been dispatched).</td>
  </tr>
  <tr>
   <td>{{Event("loadstart")}}</td>
   <td>Progress has begun.</td>
  </tr>
  <tr>
   <td>{{Event("progress")}}</td>
   <td>In progress.</td>
  </tr>
  <tr>
   <td>{{Event("timeout")}}</td>
   <td>Progression is terminated due to preset time expiring.</td>
  </tr>
 </tbody>
</table>

<h3 id="存储事件">存储事件</h3>

<p>{{Event("change")}} (参见 <a href="#非标准事件">非标准事件</a>)<br>
 {{Event("storage")}}</p>

<h3 id="更新事件">更新事件</h3>

<p>{{Event("checking")}}<br>
 {{Event("downloading")}}<br>
 {{Event("error")}}<br>
 {{Event("noupdate")}}<br>
 {{Event("obsolete")}}<br>
 {{Event("updateready")}}</p>

<h3 id="值变化事件">值变化事件</h3>

<p>{{Event("broadcast")}}<br>
 {{Event("CheckboxStateChange")}}<br>
 {{Event("hashchange")}}<br>
 {{Event("input")}}<br>
 {{Event("RadioStateChange")}}<br>
 {{Event("readystatechange")}}<br>
 {{Event("ValueChange")}}</p>

<h3 id="未分类的事件">未分类的事件</h3>

<p>{{Event("invalid")}}<br>
 <code><a href="/zh-CN/docs/Web/API/DedicatedWorkerGlobalScope/message_event">message</a></code><br>
 <code><a href="/zh-CN/docs/Web/API/EventSource/message_event">message</a></code><br>
 <code><a href="/zh-CN/docs/Web/API/EventSource/open_event">open</a></code><br>
 <code><a href="/zh-CN/docs/Web/API/Element/show_event">show</a></code></p>

<h2 id="不常见和非标准事件">不常见和非标准事件</h2>

<h3 id="Abortable_Fetch_events">Abortable Fetch events</h3>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Event name</th>
   <th scope="col">Fired when</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/API/AbortSignal/abort_event">abort</a></code></td>
   <td>A DOM request is aborted, i.e. using {{DOMxRef("AbortController.abort()")}}.</td>
  </tr>
 </tbody>
</table>

<h3 id="WebVR_events">WebVR events</h3>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Event name</th>
   <th scope="col">Fired when</th>
  </tr>
  <tr>
   <td>{{Event("vrdisplayactivate")}}</td>
   <td>When a VR display is able to be presented to, for example if an HMD has been moved to bring it out of standby, or woken up by being put on.</td>
  </tr>
  <tr>
   <td>{{Event("vrdisplayblur")}}</td>
   <td>when presentation to a {{DOMxRef("VRDisplay")}} has been paused for some reason by the browser, OS, or VR hardware — for example, while the user is interacting with a system menu or browser, to prevent tracking or loss of experience.</td>
  </tr>
  <tr>
   <td>{{Event("vrdisplayconnect")}}</td>
   <td>when a compatible {{DOMxRef("VRDisplay")}} is connected to the computer.</td>
  </tr>
  <tr>
   <td>{{Event("vrdisplaydeactivate")}}</td>
   <td>When a {{DOMxRef("VRDisplay")}} can no longer be presented to, for example if an HMD has gone into standby or sleep mode due to a period of inactivity.</td>
  </tr>
  <tr>
   <td>{{Event("vrdisplaydisconnect")}}</td>
   <td>When a compatible {{DOMxRef("VRDisplay")}} is disconnected from the computer.</td>
  </tr>
  <tr>
   <td>{{Event("vrdisplayfocus")}}</td>
   <td>When presentation to a {{DOMxRef("VRDisplay")}} has resumed after being blurred.</td>
  </tr>
  <tr>
   <td>{{Event("vrdisplaypresentchange")}}</td>
   <td>The presenting state of a {{DOMxRef("VRDisplay")}} changes — i.e. goes from presenting to not presenting, or vice versa.</td>
  </tr>
 </thead>
</table>

<h3 id="SVG_事件">SVG 事件</h3>

<p>{{Event("SVGAbort")}}<br>
 {{Event("SVGError")}}<br>
 {{Event("SVGLoad")}}<br>
 {{Event("SVGResize")}}<br>
 {{Event("SVGScroll")}}<br>
 {{Event("SVGUnload")}}<br>
 {{Event("SVGZoom")}}</p>

<h3 id="数据库事件">数据库事件</h3>

<p><code><a href="/zh-CN/docs/Web/Reference/Events/abort_indexedDB">abort</a></code><br>
 <code><a href="/zh-CN/docs/Web/Reference/Events/blocked_indexedDB">blocked</a></code><br>
 <code><a href="/zh-CN/docs/Web/Reference/Events/complete_indexedDB">complete</a></code><br>
 {{Event("error")}}<br>
 <code><a href="/zh-CN/docs/Web/Reference/Events/success_indexedDB">success</a></code><br>
 <code><a href="/zh-CN/docs/Web/Reference/Events/upgradeneeded_indexedDB">upgradeneeded</a></code><br>
 <code><a href="/zh-CN/docs/Web/Reference/Events/versionchange_indexedDB">versionchange</a></code></p>

<h3 id="脚本事件">脚本事件</h3>

<p>{{Event("afterscriptexecute")}}<br>
 {{Event("beforescriptexecute")}}</p>

<h3 id="菜单事件">菜单事件</h3>

<p>{{Event("DOMMenuItemActive")}}<br>
 {{Event("DOMMenuItemInactive")}}</p>

<h3 id="窗口事件">窗口事件</h3>

<p><code><a href="/zh-CN/docs/Mozilla/Tech/XUL/Events/close_event">close</a></code></p>

<h3 id="弹出事件">弹出事件</h3>

<p>{{Event("popuphidden")}}<br>
 {{Event("popuphiding")}}<br>
 {{Event("popupshowing")}}<br>
 {{Event("popupshown")}}</p>

<h3 id="Tab_事件">Tab 事件</h3>

<p>{{Event("visibilitychange")}}</p>

<ul>
</ul>

<h3 id="电池事件">电池事件</h3>

<p>{{Event("chargingchange")}}<br>
 {{Event("chargingtimechange")}}<br>
 {{Event("dischargingtimechange")}}<br>
 {{Event("levelchange")}}</p>

<h3 id="呼叫事件">呼叫事件</h3>

<p>{{Event("alerting")}}<br>
 {{Event("busy")}}<br>
 {{Event("callschanged")}}<br>
 {{Event("cfstatechange")}}<br>
 {{Event("connected")}}<br>
 {{Event("connecting")}}<br>
 {{Event("dialing")}}<br>
 {{Event("disconnected")}}<br>
 {{Event("disconnecting")}}<br>
 {{Event("error_(Telephony)","error")}}<br>
 {{Event("held")}}, {{Event("holding")}}<br>
 {{Event("incoming")}}<br>
 {{Event("resuming")}}<br>
 {{Event("statechange")}}<br>
 {{Event("voicechange")}}</p>

<h3 id="传感器事件">传感器事件</h3>

<p>{{Event("compassneedscalibration")}}<br>
 {{Event("devicemotion")}}<br>
 {{Event("deviceorientation")}}<br>
 {{Event("orientationchange")}}</p>

<h3 id="智能卡事件">智能卡事件</h3>

<p>{{Event("icccardlockerror")}}<br>
 {{Event("iccinfochange")}}<br>
 {{Event("smartcard-insert")}}<br>
 {{Event("smartcard-remove")}}<br>
 {{Event("stkcommand")}}<br>
 {{Event("stksessionend")}}<br>
 {{Event("cardstatechange")}}</p>

<h3 id="短信和USSD事件">短信和 USSD 事件</h3>

<p>{{Event("delivered")}}<br>
 {{Event("received")}}<br>
 {{Event("sent")}}<br>
 {{Event("ussdreceived")}}</p>

<h3 id="帧事件">帧事件</h3>

<p>{{Event("mozbrowserclose")}}<br>
 {{Event("mozbrowsercontextmenu")}}<br>
 {{Event("mozbrowsererror")}}<br>
 {{Event("mozbrowsericonchange")}}<br>
 {{Event("mozbrowserlocationchange")}}<br>
 {{Event("mozbrowserloadend")}}<br>
 {{Event("mozbrowserloadstart")}}<br>
 {{Event("mozbrowseropenwindow")}}<br>
 {{Event("mozbrowsersecuritychange")}}<br>
 {{Event("mozbrowsershowmodalprompt")}}<br>
 {{Event("mozbrowsertitlechange")}}</p>

<h3 id="DOM变异事件">DOM 变异事件</h3>

<p><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMAttributeNameChanged</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMAttrModified</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMCharacterDataModified</a></code><br>
 {{Event("DOMContentLoaded")}}<br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMElementNameChanged</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeInserted</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeInsertedIntoDocument</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeRemoved</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeRemovedFromDocument</a></code><br>
 <code><a href="/zh-CN/docs/DOM/Mutation_events">DOMSubtreeModified</a></code></p>

<h3 id="触摸事件">触摸事件</h3>

<p>{{Event("touchcancel")}}<br>
 {{Event("touchend")}}<br>
 {{Event("touchmove")}}<br>
 {{Event("touchstart")}}</p>

<h3 id="指针事件">指针事件</h3>

<p>{{Event("pointerover")}}<br>
 {{Event("pointerenter")}}<br>
 {{Event("pointerdown")}}<br>
 {{Event("pointermove")}}<br>
 {{Event("pointerup")}}<br>
 {{Event("pointercancel")}}<br>
 {{Event("pointerout")}}<br>
 {{Event("pointerleave")}}<br>
 {{Event("gotpointercapture")}}<br>
 {{Event("lostpointercapture")}}</p>

<h2 id="标准事件">标准事件</h2>

<p>这些事件在官方 Web 规范中定义，并且应在各个浏览器中通用。 每个事件都和代表事件接收方的对象（由此您可以查到每个事件提供的数据），定义这个事件的标准或标准链接会一起列出。</p>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">事件名称</th>
   <th scope="col">事件类型</th>
   <th scope="col">规范</th>
   <th scope="col">触发时机...</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("abort")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-abort">DOM L3</a></td>
   <td>资源载入已被中止</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/abort_(ProgressEvent)">abort</a></code></td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/progress-events/">Progress</a>and<a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-abort">XMLHttpRequest</a></td>
   <td>Progress 被终止 (不是 error 造成的)</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/abort_indexedDB">abort</a></code></td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#database-interface">IndexedDB</a></td>
   <td>事务已被中止</td>
  </tr>
  <tr>
   <td>{{Event("afterprint")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/html5/webappapis.html#printing">HTML5</a></td>
   <td>相关文档已开始打印或打印预览已被关闭</td>
  </tr>
  <tr>
   <td>{{Event("animationcancel")}}</td>
   <td>{{DOMxRef("AnimationEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>A <a href="/zh-CN/docs/CSS/CSS_animations">CSS animation</a> has aborted.</td>
  </tr>
  <tr>
   <td>{{Event("animationend")}}</td>
   <td>{{DOMxRef("AnimationEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>完成一个<a href="/zh-CN/docs/CSS/CSS_animations">CSS 动画</a></td>
  </tr>
  <tr>
   <td>{{Event("animationiteration")}}</td>
   <td>{{DOMxRef("AnimationEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>重复播放一个<a href="/zh-CN/docs/CSS/CSS_animations">CSS 动画</a></td>
  </tr>
  <tr>
   <td>{{Event("animationstart")}}</td>
   <td>{{DOMxRef("AnimationEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/css3-animations/#animation-events">CSS Animations</a></td>
   <td>一个 <a href="/zh-CN/docs/CSS/CSS_animations">CSS 动画</a>已开始</td>
  </tr>
  <tr>
   <td>{{Event("appinstalled")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="/zh-CN/docs/Web/Manifest">Web App Manifest</a></td>
   <td>A web application is successfully installed as a <a href="/en-US/Apps/Progressive">progressive web app</a>.</td>
  </tr>
  <tr>
   <td>{{Event("audioprocess")}}</td>
   <td>{{DOMxRef("AudioProcessingEvent")}} {{Deprecated_Inline}}</td>
   <td>{{SpecName('Web Audio API', '#AudioProcessingEvent', 'audioprocess')}}</td>
   <td>一个{{DOMxRef("ScriptProcessorNode")}} 的输入缓冲区可处理</td>
  </tr>
  <tr>
   <td>{{Event("audioend")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>用户代理捕捉到用以语音识别的音频</td>
  </tr>
  <tr>
   <td>{{Event("audiostart")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>用户代理开始捕捉用以语音识别的音频</td>
  </tr>
  <tr>
   <td>{{Event("beforeprint")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/html5/webappapis.html#printing">HTML5</a></td>
   <td>相关文档将要开始打印或准备打印预览</td>
  </tr>
  <tr>
   <td>{{Event("beforeunload")}}</td>
   <td>{{DOMxRef("BeforeUnloadEvent")}}</td>
   <td><a href="http://www.w3.org/TR/html5/browsers.html#unloading-documents">HTML5</a></td>
   <td>即将卸载 window，document 及其资源</td>
  </tr>
  <tr>
   <td>{{Event("beginEvent")}}</td>
   <td>{{DOMxRef("TimeEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>A <a href="/zh-CN/docs/SVG/SVG_animation_with_SMIL">SMIL</a> animation element begins.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/blocked_indexedDB">blocked</a></code></td>
   <td></td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>An open connection to a database is blocking a <code>versionchange</code> transaction on the same database.</td>
  </tr>
  <tr>
   <td>{{Event("blur")}}</td>
   <td>{{DOMxRef("FocusEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-blur">DOM L3</a></td>
   <td>An element has lost focus (does not bubble).</td>
  </tr>
  <tr>
   <td>{{Event("boundary")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechSynthesisEvent")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The spoken utterance reaches a word or sentence boundary</td>
  </tr>
  <tr>
   <td>{{Event("canplay")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-canplay">HTML5 media</a></td>
   <td>The user agent can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content.</td>
  </tr>
  <tr>
   <td>{{Event("canplaythrough")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-canplaythrough">HTML5 media</a></td>
   <td>The user agent can play the media up to its end without having to stop for further buffering of content.</td>
  </tr>
  <tr>
   <td>{{Event("change")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html">DOM L2</a>, <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/common-input-element-attributes.html#event-input-change">HTML5</a></td>
   <td>The <code>change</code> event is fired for {{HTMLElement("input")}}, {{HTMLElement("select")}}, and {{HTMLElement("textarea")}} elements when a change to the element's value is committed by the user.</td>
  </tr>
  <tr>
   <td>{{Event("chargingchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The battery begins or stops charging.</td>
  </tr>
  <tr>
   <td>{{Event("chargingtimechange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The <code>chargingTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{Event("click")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-click">DOM L3</a></td>
   <td>A pointing device button has been pressed and released on an element.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/close_websocket">close</a></code></td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A WebSocket connection has been closed.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/complete_indexedDB">complete</a></code></td>
   <td></td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#transaction">IndexedDB</a></td>
   <td>A transaction successfully completed.</td>
  </tr>
  <tr>
   <td>{{Event("complete")}}</td>
   <td>{{DOMxRef("OfflineAudioCompletionEvent")}} {{Deprecated_Inline}}</td>
   <td>{{SpecName('Web Audio API', '#OfflineAudioCompletionEvent-section', 'OfflineAudioCompletionEvent')}}</td>
   <td>The rendering of an {{DOMxRef("OfflineAudioContext")}} is terminated.</td>
  </tr>
  <tr>
   <td>{{Event("compositionend")}}</td>
   <td>{{DOMxRef("CompositionEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-compositionend">DOM L3</a></td>
   <td>The composition of a passage of text has been completed or canceled.</td>
  </tr>
  <tr>
   <td>{{Event("compositionstart")}}</td>
   <td>{{DOMxRef("CompositionEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-compositionstart">DOM L3</a></td>
   <td>The composition of a passage of text is prepared (similar to keydown for a keyboard input, but works with other inputs such as speech recognition).</td>
  </tr>
  <tr>
   <td>{{Event("compositionupdate")}}</td>
   <td>{{DOMxRef("CompositionEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-compositionupdate">DOM L3</a></td>
   <td>A character is added to a passage of text being composed.</td>
  </tr>
  <tr>
   <td>{{Event("contextmenu")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="https://html.spec.whatwg.org/multipage/forms.html#context-menus">HTML5</a></td>
   <td>The right button of the mouse is clicked (before the context menu is displayed).</td>
  </tr>
  <tr>
   <td>{{Event("copy")}}</td>
   <td>{{DOMxRef("ClipboardEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/clipboard-apis/#copy-event">Clipboard</a></td>
   <td>The text selection has been added to the clipboard.</td>
  </tr>
  <tr>
   <td>{{Event("cut")}}</td>
   <td>{{DOMxRef("ClipboardEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/clipboard-apis/#cut-event">Clipboard</a></td>
   <td>The text selection has been removed from the document and added to the clipboard.</td>
  </tr>
  <tr>
   <td>{{Event("dblclick")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-dblclick">DOM L3</a></td>
   <td>A pointing device button is clicked twice on an element.</td>
  </tr>
  <tr>
   <td>{{Event("devicechange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName("Media Capture")}}</td>
   <td>A media device such as a camera, microphone, or speaker is connected or removed from the system.</td>
  </tr>
  <tr>
   <td>{{Event("devicemotion")}}</td>
   <td>{{DOMxRef("DeviceMotionEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://dev.w3.org/geo/api/spec-source-orientation.html">Device Orientation Events</a></td>
   <td>Fresh data is available from a motion sensor.</td>
  </tr>
  <tr>
   <td>{{Event("deviceorientation")}}</td>
   <td>{{DOMxRef("DeviceOrientationEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://dev.w3.org/geo/api/spec-source-orientation.html">Device Orientation Events</a></td>
   <td>Fresh data is available from an orientation sensor.</td>
  </tr>
  <tr>
   <td>{{Event("dischargingtimechange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The <code>dischargingTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td><code>DOMActivate</code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMActivate">DOM L3</a></td>
   <td>A button, link or state changing element is activated (use {{Event("click")}} instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMAttributeNameChanged</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationNameEvent")}}</td>
   <td><a href="http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531/#event-type-DOMAttributeNameChanged">DOM L3</a> Removed</td>
   <td>The name of an attribute changed (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMAttrModified</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMAttrModified">DOM L3</a></td>
   <td>The value of an attribute has been modified (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMCharacterDataModified</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMCharacterDataModified">DOM L3</a></td>
   <td>A text or another <a href="/zh-CN/docs/DOM/CharacterData">CharacterData</a> has changed (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td>{{Event("DOMContentLoaded")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-end.html#the-end">HTML5</a></td>
   <td>The document has finished loading (but not its dependent resources).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMElementNameChanged</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationNameEvent")}}</td>
   <td><a href="http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531/#event-type-DOMElementNameChanged">DOM L3</a> Removed</td>
   <td>The name of an element changed (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code>DOMFocusIn</code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("FocusEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMFocusIn">DOM L3</a></td>
   <td>An element has received focus (use {{Event("focus")}} or {{Event("focusin")}} instead).</td>
  </tr>
  <tr>
   <td><code>DOMFocusOut</code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("FocusEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMFocusOut">DOM L3</a></td>
   <td>An element has lost focus (use {{Event("blur")}} or {{Event("focusout")}} instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeInserted</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeInserted">DOM L3</a></td>
   <td>A node has been added as a child of another node (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeInsertedIntoDocument</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeInsertedIntoDocument">DOM L3</a></td>
   <td>A node has been inserted into the document (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeRemoved</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeRemoved">DOM L3</a></td>
   <td>A node has been removed from its parent node (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMNodeRemovedFromDocument</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMNodeRemovedFromDocument">DOM L3</a></td>
   <td>A node has been removed from the document (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/DOM/Mutation_events">DOMSubtreeModified</a></code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("MutationEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMSubtreeModified">DOM L3</a></td>
   <td>A change happened in the document (use <a href="/zh-CN/docs/DOM/MutationObserver">mutation observers</a> instead).</td>
  </tr>
  <tr>
   <td>{{Event("drag")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-drag">HTML5</a></td>
   <td>An element or text selection is being dragged (every 350ms).</td>
  </tr>
  <tr>
   <td>{{Event("dragend")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragend">HTML5</a></td>
   <td>A drag operation is being ended (by releasing a mouse button or hitting the escape key).</td>
  </tr>
  <tr>
   <td>{{Event("dragenter")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragenter">HTML5</a></td>
   <td>A dragged element or text selection enters a valid drop target.</td>
  </tr>
  <tr>
   <td>{{Event("dragleave")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragleave">HTML5</a></td>
   <td>A dragged element or text selection leaves a valid drop target.</td>
  </tr>
  <tr>
   <td>{{Event("dragover")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragover">HTML5</a></td>
   <td>An element or text selection is being dragged over a valid drop target (every 350ms).</td>
  </tr>
  <tr>
   <td>{{Event("dragstart")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-dragstart">HTML5</a></td>
   <td>The user starts dragging an element or text selection.</td>
  </tr>
  <tr>
   <td>{{Event("drop")}}</td>
   <td>{{DOMxRef("DragEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/dnd.html#event-drop">HTML5</a></td>
   <td>An element is dropped on a valid drop target.</td>
  </tr>
  <tr>
   <td>{{Event("durationchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-durationchange">HTML5 media</a></td>
   <td>The <code>duration</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{Event("emptied")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-emptied">HTML5 media</a></td>
   <td>The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the <a href="/zh-CN/docs/XPCOM_Interface_Reference/NsIDOMHTMLMediaElement"><code>load()</code></a> method is called to reload it.</td>
  </tr>
  <tr>
   <td>{{Event("end_(SpeechRecognition)","end")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The speech recognition service has disconnected.</td>
  </tr>
  <tr>
   <td>{{Event("end_(SpeechSynthesis)","end")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechSynthesisEvent")}}</td>
   <td>{{SpecName("Web Speech API")}}</td>
   <td>The utterance has finished being spoken.</td>
  </tr>
  <tr>
   <td>{{Event("ended")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-ended">HTML5 media</a></td>
   <td>Playback has stopped because the end of the media was reached.</td>
  </tr>
  <tr>
   <td>{{Event("ended_(Web_Audio)", "ended")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName("Web Audio API")}}</td>
   <td>Playback has stopped because the end of the media was reached.</td>
  </tr>
  <tr>
   <td>{{Event("endEvent")}}</td>
   <td>{{DOMxRef("TimeEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>A <a href="/zh-CN/docs/SVG/SVG_animation_with_SMIL">SMIL</a> animation element ends.</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-error">DOM L3</a></td>
   <td>A resource failed to load.</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-error">XMLHttpRequest</a></td>
   <td>Progression has failed.</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A WebSocket connection has been closed with prejudice (some data couldn't be sent for example).</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://dev.w3.org/html5/eventsource/">Server Sent Events</a></td>
   <td>An event source connection has been failed.</td>
  </tr>
  <tr>
   <td>{{Event("error")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>A request caused an error and failed.</td>
  </tr>
  <tr>
   <td>{{Event("error_(SpeechRecognitionError)","error")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>A speech recognition error occurs.</td>
  </tr>
  <tr>
   <td>{{Event("error_(SpeechSynthesisError)","error")}}</td>
   <td>{{DOMxRef("SpeechSynthesisErrorEvent")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>An error occurs that prevents the utterance from being successfully spoken.</td>
  </tr>
  <tr>
   <td>{{Event("focus")}}</td>
   <td>{{DOMxRef("FocusEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focus">DOM L3</a></td>
   <td>An element has received focus (does not bubble).</td>
  </tr>
  <tr>
   <td>{{Event("focusin")}}</td>
   <td>{{DOMxRef("FocusEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focusIn">DOM L3</a></td>
   <td>An element is about to receive focus (bubbles).</td>
  </tr>
  <tr>
   <td>{{Event("focusout")}}</td>
   <td>{{DOMxRef("FocusEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-focusout">DOM L3</a></td>
   <td>An element is about to lose focus (bubbles).</td>
  </tr>
  <tr>
   <td>{{Event("fullscreenchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="https://dvcs.w3.org/hg/fullscreen/raw-file/tip/Overview.html#api">Full Screen</a></td>
   <td>An element was turned to fullscreen mode or back to normal mode.</td>
  </tr>
  <tr>
   <td>{{Event("fullscreenerror")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="https://dvcs.w3.org/hg/fullscreen/raw-file/tip/Overview.html#api">Full Screen</a></td>
   <td>It was impossible to switch to fullscreen mode for technical reasons or because the permission was denied.</td>
  </tr>
  <tr>
   <td>{{Event("gamepadconnected")}}</td>
   <td>{{DOMxRef("GamepadEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/gamepad/#the-gamepadconnected-event">Gamepad</a></td>
   <td>A gamepad has been connected.</td>
  </tr>
  <tr>
   <td>{{Event("gamepaddisconnected")}}</td>
   <td>{{DOMxRef("GamepadEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/gamepad/#the-gamepaddisconnected-event">Gamepad</a></td>
   <td>A gamepad has been disconnected.</td>
  </tr>
  <tr>
   <td>{{Event("gotpointercapture")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-gotpointercapture-event">Pointer Events</a></td>
   <td>Element receives pointer capture.</td>
  </tr>
  <tr>
   <td>{{Event("hashchange")}}</td>
   <td>{{DOMxRef("HashChangeEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-hashchange">HTML5</a></td>
   <td>The fragment identifier of the URL has changed (the part of the URL after the #).</td>
  </tr>
  <tr>
   <td>{{Event("lostpointercapture")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-lostpointercapture-event">Pointer Events</a></td>
   <td>Element lost pointer capture.</td>
  </tr>
  <tr>
   <td>{{Event("input")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/html5/forms.html#common-event-behaviors">HTML5</a></td>
   <td>The value of an element changes or the content of an element with the attribute <a href="/zh-CN/docs/DOM/Element.contentEditable">contenteditable</a> is modified.</td>
  </tr>
  <tr>
   <td>{{Event("invalid")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/association-of-controls-and-forms.html#constraint-validation">HTML5</a></td>
   <td>A submittable element has been checked and doesn't satisfy its constraints.</td>
  </tr>
  <tr>
   <td>{{Event("keydown")}}</td>
   <td>{{DOMxRef("KeyboardEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keydown">DOM L3</a></td>
   <td>A key is pressed down.</td>
  </tr>
  <tr>
   <td>{{Event("keypress")}}</td>
   <td>{{DOMxRef("KeyboardEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keypress">DOM L3</a></td>
   <td>A key is pressed down and that key normally produces a character value (use input instead).</td>
  </tr>
  <tr>
   <td>{{Event("keyup")}}</td>
   <td>{{DOMxRef("KeyboardEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keyup">DOM L3</a></td>
   <td>A key is released.</td>
  </tr>
  <tr>
   <td>{{Event("languagechange")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{ SpecName('HTML5.1', '#dom-navigator-languages', 'NavigatorLanguage.languages') }}</td>
   <td>The user's preferred languages have changed.</td>
  </tr>
  <tr>
   <td>{{Event("levelchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="https://dvcs.w3.org/hg/dap/raw-file/tip/battery/Overview.html">Battery status</a></td>
   <td>The <code>level</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{Event("load")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-load">DOM L3</a></td>
   <td>A resource and its dependent resources have finished loading.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/load_(ProgressEvent)">load</a></code></td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-load">XMLHttpRequest</a></td>
   <td>Progression has been successful.</td>
  </tr>
  <tr>
   <td>{{Event("loadeddata")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-loadeddata">HTML5 media</a></td>
   <td>The first frame of the media has finished loading.</td>
  </tr>
  <tr>
   <td>{{Event("loadedmetadata")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-loadedmetadata">HTML5 media</a></td>
   <td>The metadata has been loaded.</td>
  </tr>
  <tr>
   <td>{{Event("loadend")}}</td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-loadend">XMLHttpRequest</a></td>
   <td>Progress has stopped (after "error", "abort" or "load" have been dispatched).</td>
  </tr>
  <tr>
   <td>{{Event("loadstart")}}</td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/progress-events/">Progress </a>and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-loadstart">XMLHttpRequest</a></td>
   <td>Progress has begun.</td>
  </tr>
  <tr>
   <td>{{Event("mark")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechSynthesisEvent")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The spoken utterance reaches a named SSML "mark" tag.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/message_websocket">message</a></code></td>
   <td>{{DOMxRef("MessageEvent")}}</td>
   <td><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A message is received through a WebSocket.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/message_webworker">message</a></code></td>
   <td>{{DOMxRef("MessageEvent")}}</td>
   <td><a href="http://www.w3.org/TR/workers/#communicating-with-a-dedicated-worker">Web Workers</a></td>
   <td>A message is received from a Web Worker.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/message_webmessaging">message</a></code></td>
   <td>{{DOMxRef("MessageEvent")}}</td>
   <td><a href="http://www.w3.org/TR/webmessaging/">Web Messaging</a></td>
   <td>A message is received from a child (i)frame or a parent window.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/message_serversentevents">message</a></code></td>
   <td>{{DOMxRef("MessageEvent")}}</td>
   <td><a href="http://dev.w3.org/html5/eventsource/">Server Sent Events</a></td>
   <td>A message is received through an event source.</td>
  </tr>
  <tr>
   <td>{{Event("messageerror")}}</td>
   <td>{{DOMxRef("MessageEvent")}}</td>
   <td>{{DOMxRef("MessagePort")}}, <a href="/zh-CN/docs/Web/API/Web_Workers_API">Web Workers</a>, <a href="/zh-CN/docs/Web/API/Broadcast_Channel_API">Broadcast Channel</a>, {{DOMxRef("Window")}}</td>
   <td>A message error is raised when a message is received by an object.</td>
  </tr>
  <tr>
   <td>{{Event("message_(ServiceWorker)","message")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("ServiceWorkerMessageEvent")}} or {{DOMxRef("ExtendableMessageEvent")}}, depending on context.</td>
   <td><a href="/zh-CN/docs/Web/API/Service_Worker_API">Service Workers</a></td>
   <td>A message is received from a service worker, or a message is received in a service worker from another context.</td>
  </tr>
  <tr>
   <td>{{Event("mousedown")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mousedown">DOM L3</a></td>
   <td>A pointing device button (usually a mouse) is pressed on an element.</td>
  </tr>
  <tr>
   <td>{{Event("mouseenter")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseenter">DOM L3</a></td>
   <td>A pointing device is moved onto the element that has the listener attached.</td>
  </tr>
  <tr>
   <td>{{Event("mouseleave")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseleave">DOM L3</a></td>
   <td>A pointing device is moved off the element that has the listener attached.</td>
  </tr>
  <tr>
   <td>{{Event("mousemove")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mousemove">DOM L3</a></td>
   <td>A pointing device is moved over an element.</td>
  </tr>
  <tr>
   <td>{{Event("mouseout")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseout">DOM L3</a></td>
   <td>A pointing device is moved off the element that has the listener attached or off one of its children.</td>
  </tr>
  <tr>
   <td>{{Event("mouseover")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseover">DOM L3</a></td>
   <td>A pointing device is moved onto the element that has the listener attached or onto one of its children.</td>
  </tr>
  <tr>
   <td>{{Event("mouseup")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-mouseup">DOM L3</a></td>
   <td>A pointing device button is released over an element.</td>
  </tr>
  <tr>
   <td>{{Event("nomatch")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechRecognitionEvent")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The speech recognition service returns a final result with no significant recognition.</td>
  </tr>
  <tr>
   <td>{{Event("notificationclick")}}</td>
   <td>{{DOMxRef("NotificationEvent")}} {{Experimental_Inline}}</td>
   <td>{{SpecName('Web Notifications','#dom-serviceworkerglobalscope-onnotificationclick','onnotificationclick')}}</td>
   <td>A system notification spawned by {{DOMxRef("ServiceWorkerRegistration.showNotification()")}} has been clicked.</td>
  </tr>
  <tr>
   <td>{{Event("offline")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/offline.html#event-offline">HTML5 offline</a></td>
   <td>The browser has lost access to the network.</td>
  </tr>
  <tr>
   <td>{{Event("online")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/offline.html#event-online">HTML5 offline</a></td>
   <td>The browser has gained access to the network (but particular websites might be unreachable).</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/open_websocket">open</a></code></td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/websockets/">WebSocket</a></td>
   <td>A WebSocket connection has been established.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/open_serversentevents">open</a></code></td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://dev.w3.org/html5/eventsource/">Server Sent Events</a></td>
   <td>An event source connection has been established.</td>
  </tr>
  <tr>
   <td>{{Event("orientationchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/screen-orientation/">Screen Orientation</a></td>
   <td>The orientation of the device (portrait/landscape) has changed</td>
  </tr>
  <tr>
   <td>{{Event("pagehide")}}</td>
   <td>{{DOMxRef("PageTransitionEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-pagehide">HTML5</a></td>
   <td>A session history entry is being traversed from.</td>
  </tr>
  <tr>
   <td>{{Event("pageshow")}}</td>
   <td>{{DOMxRef("PageTransitionEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-pageshow">HTML5</a></td>
   <td>A session history entry is being traversed to.</td>
  </tr>
  <tr>
   <td>{{Event("paste")}}</td>
   <td>{{DOMxRef("ClipboardEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/clipboard-apis/#paste-event">Clipboard</a></td>
   <td>Data has been transferred from the system clipboard to the document.</td>
  </tr>
  <tr>
   <td>{{Event("pause")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-pause">HTML5 media</a></td>
   <td>Playback has been paused.</td>
  </tr>
  <tr>
   <td>{{Event("pause_(SpeechSynthesis)", "pause")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechSynthesisEvent")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The utterance is paused part way through.</td>
  </tr>
  <tr>
   <td>{{Event("pointercancel")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointercancel-event">Pointer Events</a></td>
   <td>The pointer is unlikely to produce any more events.</td>
  </tr>
  <tr>
   <td>{{Event("pointerdown")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointerdown-event">Pointer Events</a></td>
   <td>The pointer enters the active buttons state.</td>
  </tr>
  <tr>
   <td>{{Event("pointerenter")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointerenter-event">Pointer Events</a></td>
   <td>Pointing device is moved inside the hit-testing boundary.</td>
  </tr>
  <tr>
   <td>{{Event("pointerleave")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointerleave-event">Pointer Events</a></td>
   <td>Pointing device is moved out of the hit-testing boundary.</td>
  </tr>
  <tr>
   <td>{{Event("pointerlockchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/pointerlock/#pointerlockchange-and-pointerlockerror-events">Pointer Lock</a></td>
   <td>The pointer was locked or released.</td>
  </tr>
  <tr>
   <td>{{Event("pointerlockerror")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/pointerlock/#pointerlockchange-and-pointerlockerror-events">Pointer Lock</a></td>
   <td>It was impossible to lock the pointer for technical reasons or because the permission was denied.</td>
  </tr>
  <tr>
   <td>{{Event("pointermove")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointermove-event">Pointer Events</a></td>
   <td>The pointer changed coordinates.</td>
  </tr>
  <tr>
   <td>{{Event("pointerout")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointerout-event">Pointer Events</a></td>
   <td>The pointing device moved out of hit-testing boundary or leaves detectable hover range.</td>
  </tr>
  <tr>
   <td>{{Event("pointerover")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointerover-event">Pointer Events</a></td>
   <td>The pointing device is moved into the hit-testing boundary.</td>
  </tr>
  <tr>
   <td>{{Event("pointerup")}}</td>
   <td>{{DOMxRef("PointerEvent")}}</td>
   <td><a href="http://www.w3.org/TR/pointerevents/#the-pointerup-event">Pointer Events</a></td>
   <td>The pointer leaves the active buttons state.</td>
  </tr>
  <tr>
   <td>{{Event("play")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-play">HTML5 media</a></td>
   <td>Playback has begun.</td>
  </tr>
  <tr>
   <td>{{Event("playing")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-playing">HTML5 media</a></td>
   <td>Playback is ready to start after having been paused or delayed due to lack of data.</td>
  </tr>
  <tr>
   <td>{{Event("popstate")}}</td>
   <td>{{DOMxRef("PopStateEvent")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/history.html#event-popstate">HTML5</a></td>
   <td>A session history entry is being navigated to (in certain cases).</td>
  </tr>
  <tr>
   <td>{{Event("progress")}}</td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/progress-events/">Progress</a> and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-progress">XMLHttpRequest</a></td>
   <td>In progress.</td>
  </tr>
  <tr>
   <td>{{Event("push")}}</td>
   <td>{{DOMxRef("PushEvent")}} {{Experimental_Inline}}</td>
   <td>{{SpecName("Push API")}}</td>
   <td>A <a href="/zh-CN/docs/Web/API/Service_Worker_API">Service Worker</a> has received a push message.</td>
  </tr>
  <tr>
   <td>{{Event("pushsubscriptionchange")}}</td>
   <td>{{DOMxRef("PushEvent")}} {{Experimental_Inline}}</td>
   <td>{{SpecName("Push API")}}</td>
   <td>A <a href="/zh-CN/docs/Web/API/PushSubscription">PushSubscription</a> has expired.</td>
  </tr>
  <tr>
   <td>{{Event("ratechange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-ratechange">HTML5 media</a></td>
   <td>The playback rate has changed.</td>
  </tr>
  <tr>
   <td>{{Event("readystatechange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>HTML5 and <a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-readystatechange">XMLHttpRequest</a></td>
   <td>The readyState attribute of a document has changed.</td>
  </tr>
  <tr>
   <td>{{Event("repeatEvent")}}</td>
   <td>{{DOMxRef("TimeEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>A <a href="/zh-CN/docs/SVG/SVG_animation_with_SMIL">SMIL</a> animation element is repeated.</td>
  </tr>
  <tr>
   <td>{{Event("reset")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html">DOM L2</a>, <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/association-of-controls-and-forms.html#form-submission-0#resetting-a-form">HTML5</a></td>
   <td>A form is reset.</td>
  </tr>
  <tr>
   <td>{{Event("resize")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-resize">DOM L3</a></td>
   <td>The document view has been resized.</td>
  </tr>
  <tr>
   <td>{{Event("resourcetimingbufferfull")}}</td>
   <td>{{DOMxRef("Performance")}}</td>
   <td><a href="https://w3c.github.io/resource-timing/#dom-performance-onresourcetimingbufferfull">Resource Timing</a></td>
   <td>The browser's resource timing buffer is full.</td>
  </tr>
  <tr>
   <td>{{Event("result")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechRecognitionEvent")}} {{Experimental_Inline}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The speech recognition service returns a result — a word or phrase has been positively recognized and this has been communicated back to the app.</td>
  </tr>
  <tr>
   <td>{{Event("resume")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("SpeechSynthesisEvent")}} {{Experimental_Inline}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>A paused utterance is resumed.</td>
  </tr>
  <tr>
   <td>{{Event("scroll")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-scroll">DOM L3</a></td>
   <td>The document view or an element has been scrolled.</td>
  </tr>
  <tr>
   <td>{{Event("seeked")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-seeked">HTML5 media</a></td>
   <td>A <em>seek</em> operation completed.</td>
  </tr>
  <tr>
   <td>{{Event("seeking")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-seeking">HTML5 media</a></td>
   <td>A <em>seek</em> operation began.</td>
  </tr>
  <tr>
   <td>{{Event("select")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-select">DOM L3</a></td>
   <td>Some text is being selected.</td>
  </tr>
  <tr>
   <td>{{Event("selectstart")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{ SpecName('Selection API')}}</td>
   <td>A selection just started.</td>
  </tr>
  <tr>
   <td>{{Event("selectionchange")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{ SpecName('Selection API')}}</td>
   <td>The selection in the document has been changed.</td>
  </tr>
  <tr>
   <td>{{Event("show")}}</td>
   <td>{{DOMxRef("MouseEvent")}}</td>
   <td><a href="http://www.w3.org/TR/html5/interactive-elements.html#context-menus">HTML5</a></td>
   <td>A contextmenu event was fired on/bubbled to an element that has a <a href="/zh-CN/docs/DOM/element.contextmenu">contextmenu</a> attribute</td>
  </tr>
  <tr>
   <td>{{Event("slotchange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{ SpecName('DOM WHATWG')}}</td>
   <td>The node contents of a {{DOMxRef("HTMLSlotElement")}} ({{htmlelement("slot")}}) have changed.</td>
  </tr>
  <tr>
   <td>{{Event("soundend")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>Any sound — recognisable speech or not — has stopped being detected.</td>
  </tr>
  <tr>
   <td>{{Event("soundstart")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>Any sound — recognisable speech or not — has been detected.</td>
  </tr>
  <tr>
   <td>{{Event("speechend")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>Speech recognised by the speech recognition service has stopped being detected.</td>
  </tr>
  <tr>
   <td>{{Event("speechstart")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>Sound that is recognised by the speech recognition service as speech has been detected.</td>
  </tr>
  <tr>
   <td>{{Event("stalled")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-stalled">HTML5 media</a></td>
   <td>The user agent is trying to fetch media data, but data is unexpectedly not forthcoming.</td>
  </tr>
  <tr>
   <td>{{Event("start_(SpeechRecognition)","start")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The speech recognition service has begun listening to incoming audio with intent to recognize grammars associated with the current <code>SpeechRecognition</code>.</td>
  </tr>
  <tr>
   <td>{{Event("start_(SpeechSynthesis)","start")}}</td>
   <td>{{DOMxRef("SpeechSynthesisEvent")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The utterance has begun to be spoken.</td>
  </tr>
  <tr>
   <td>{{Event("storage")}}</td>
   <td>{{DOMxRef("StorageEvent")}}</td>
   <td><a href="http://www.w3.org/TR/webstorage/#the-storage-event">Web Storage</a></td>
   <td>A storage area (<a href="/zh-CN/docs/DOM/Storage#localStorage">localStorage</a> or <a href="/zh-CN/docs/DOM/Storage#sessionStorage">sessionStorage</a>) has changed.</td>
  </tr>
  <tr>
   <td>{{Event("submit")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-2-Events/events.html">DOM L2</a>, <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/association-of-controls-and-forms.html#form-submission-algorithm">HTML5</a></td>
   <td>A form is submitted.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/success_indexedDB">success</a></code></td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>A request successfully completed.</td>
  </tr>
  <tr>
   <td>{{Event("suspend")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-suspend">HTML5 media</a></td>
   <td>Media data loading has been suspended.</td>
  </tr>
  <tr>
   <td>{{Event("SVGAbort")}}</td>
   <td>{{DOMxRef("SVGEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>Page loading has been stopped before the <a href="/zh-CN/docs/SVG">SVG</a> was loaded.</td>
  </tr>
  <tr>
   <td>{{Event("SVGError")}}</td>
   <td>{{DOMxRef("SVGEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An error has occurred before the <a href="/zh-CN/docs/SVG">SVG</a> was loaded.</td>
  </tr>
  <tr>
   <td>{{Event("SVGLoad")}}</td>
   <td>{{DOMxRef("SVGEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-CN/docs/SVG">SVG</a> document has been loaded and parsed.</td>
  </tr>
  <tr>
   <td>{{Event("SVGResize")}}</td>
   <td>{{DOMxRef("SVGEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-CN/docs/SVG">SVG</a> document is being resized.</td>
  </tr>
  <tr>
   <td>{{Event("SVGScroll")}}</td>
   <td>{{DOMxRef("SVGEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-CN/docs/SVG">SVG</a> document is being scrolled.</td>
  </tr>
  <tr>
   <td>{{Event("SVGUnload")}}</td>
   <td>{{DOMxRef("SVGEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-CN/docs/SVG">SVG</a> document has been removed from a window or frame.</td>
  </tr>
  <tr>
   <td>{{Event("SVGZoom")}}</td>
   <td>{{DOMxRef("SVGZoomEvent")}}</td>
   <td><a href="http://www.w3.org/TR/SVG/interact.html#SVGEvents">SVG</a></td>
   <td>An <a href="/zh-CN/docs/SVG">SVG</a> document is being zoomed.</td>
  </tr>
  <tr>
   <td>{{Event("timeout")}}</td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><a href="http://www.w3.org/TR/XMLHttpRequest/#event-xhr-timeout">XMLHttpRequest</a></td>
   <td></td>
  </tr>
  <tr>
   <td>{{Event("timeupdate")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-timeupdate">HTML5 media</a></td>
   <td>The time indicated by the <code>currentTime</code> attribute has been updated.</td>
  </tr>
  <tr>
   <td>{{Event("touchcancel")}}</td>
   <td>{{DOMxRef("TouchEvent")}}</td>
   <td><a href="http://www.w3.org/TR/touch-events/">Touch Events</a></td>
   <td>A touch point has been disrupted in an implementation-specific manners (too many touch points for example).</td>
  </tr>
  <tr>
   <td>{{Event("touchend")}}</td>
   <td>{{DOMxRef("TouchEvent")}}</td>
   <td><a href="http://www.w3.org/TR/touch-events/#the-touchend-event">Touch Events</a></td>
   <td>A touch point is removed from the touch surface.</td>
  </tr>
  <tr>
   <td>{{Event("touchmove")}}</td>
   <td>{{DOMxRef("TouchEvent")}}</td>
   <td><a href="http://www.w3.org/TR/touch-events/#the-touchmove-event">Touch Events</a></td>
   <td>A touch point is moved along the touch surface.</td>
  </tr>
  <tr>
   <td>{{Event("touchstart")}}</td>
   <td>{{DOMxRef("TouchEvent")}}</td>
   <td><a href="http://www.w3.org/TR/touch-events/#the-touchstart---------event">Touch Events</a></td>
   <td>A touch point is placed on the touch surface.</td>
  </tr>
  <tr>
   <td>{{Event("transitionend")}}</td>
   <td>{{DOMxRef("TransitionEvent")}} {{Experimental_Inline}}</td>
   <td><a href="http://www.w3.org/TR/css3-transitions/#transition-events">CSS Transitions</a></td>
   <td>A <a href="/zh-CN/docs/CSS/CSS_transitions">CSS transition</a> has completed.</td>
  </tr>
  <tr>
   <td>{{Event("unload")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-unload">DOM L3</a></td>
   <td>The document or a dependent resource is being unloaded.</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/upgradeneeded_indexedDB">upgradeneeded</a></code></td>
   <td></td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#request-api">IndexedDB</a></td>
   <td>An attempt was made to open a database with a version number higher than its current version. A <code>versionchange</code> transaction has been created.</td>
  </tr>
  <tr>
   <td>{{Event("userproximity")}}</td>
   <td>{{DOMxRef("UserProximityEvent")}} {{Experimental_Inline}}</td>
   <td>{{SpecName("Proximity Events")}}</td>
   <td>Fresh data is available from a proximity sensor (indicates whether the nearby object is <code>near</code> the device or not).</td>
  </tr>
  <tr>
   <td>{{Event("voiceschanged")}} {{Experimental_Inline}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td>{{SpecName('Web Speech API')}}</td>
   <td>The list of {{DOMxRef("SpeechSynthesisVoice")}} objects that would be returned by the {{DOMxRef("SpeechSynthesis.getVoices()")}} method has changed (when the {{Event("voiceschanged")}} event fires.)</td>
  </tr>
  <tr>
   <td><code><a href="/zh-CN/docs/Web/Reference/Events/versionchange_indexedDB">versionchange</a></code></td>
   <td></td>
   <td><a href="http://www.w3.org/TR/IndexedDB/#database-interface">IndexedDB</a></td>
   <td>A <code>versionchange</code> transaction completed.</td>
  </tr>
  <tr>
   <td>{{Event("visibilitychange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.w3.org/TR/page-visibility/#sec-visibilitychange-event">Page visibility</a></td>
   <td>The content of a tab has become visible or has been hidden.</td>
  </tr>
  <tr>
   <td>{{Event("volumechange")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-volumechange">HTML5 media</a></td>
   <td>The volume has changed.</td>
  </tr>
  <tr>
   <td>{{Event("waiting")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html#event-media-waiting">HTML5 media</a></td>
   <td>Playback has stopped because of a temporary lack of data.</td>
  </tr>
  <tr>
   <td>{{Event("wheel")}}</td>
   <td>{{DOMxRef("WheelEvent")}}</td>
   <td><a href="http://www.w3.org/TR/DOM-Level-3-Events/#event-type-wheel">DOM L3</a></td>
   <td>A wheel button of a pointing device is rotated in any direction.</td>
  </tr>
 </tbody>
</table>

<h2 id="非标准事件">非标准事件</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Event Type</th>
   <th scope="col">Specification</th>
   <th scope="col">Fired when...</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("afterscriptexecute")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><em>Mozilla Specific</em></td>
   <td>A script has been executed.</td>
  </tr>
  <tr>
   <td>{{Event("beforescriptexecute")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><em>Mozilla Specific</em></td>
   <td>A script is about to be executed.</td>
  </tr>
  <tr>
   <td>{{Event("beforeinstallprompt")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><em>Chrome specific</em></td>
   <td>A user is prompted to save a web site to a home screen on mobile.</td>
  </tr>
  <tr>
   <td>{{Event("cardstatechange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{DOMxRef("MozMobileConnection.cardState")}} property changes value.</td>
  </tr>
  <tr>
   <td>{{Event("change")}}</td>
   <td>{{DOMxRef("DeviceStorageChangeEvent")}}</td>
   <td><em>Firefox OS specific</em></td>
   <td>This event is triggered each time a file is created, modified or deleted on a given storage area.</td>
  </tr>
  <tr>
   <td>{{Event("connectionInfoUpdate")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The informations about the signal strength and the link speed have been updated.</td>
  </tr>
  <tr>
   <td>{{Event("cfstatechange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The call forwarding state changes.</td>
  </tr>
  <tr>
   <td>{{Event("datachange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{DOMxRef("MozMobileConnection.data")}} object changes values.</td>
  </tr>
  <tr>
   <td>{{Event("dataerror")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{DOMxRef("MozMobileConnection.data")}} object receive an error from the <abbr title="Radio Interface Layer">RIL</abbr>.</td>
  </tr>
  <tr>
   <td>{{Event("DOMMouseScroll")}}{{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>The wheel button of a pointing device is rotated (detail attribute is a number of lines). (use {{Event("wheel")}} instead)</td>
  </tr>
  <tr>
   <td><code>dragdrop</code> {{Deprecated_Inline}}</td>
   <td><code>DragEvent</code></td>
   <td><em>Mozilla specific</em></td>
   <td>An element is dropped (use {{Event("drop")}} instead).</td>
  </tr>
  <tr>
   <td><code>dragexit</code> {{Deprecated_Inline}}</td>
   <td><code>DragEvent</code></td>
   <td><em>Mozilla specific</em></td>
   <td>A drag operation is being ended(use {{Event("dragend")}} instead).</td>
  </tr>
  <tr>
   <td><code>draggesture</code> {{Deprecated_Inline}}</td>
   <td><code>DragEvent</code></td>
   <td><em>Mozilla specific</em></td>
   <td>The user starts dragging an element or text selection (use {{Event("dragstart")}} instead).</td>
  </tr>
  <tr>
   <td>{{Event("icccardlockerror")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>the {{DOMxRef("MozMobileConnection.unlockCardLock()")}} or {{DOMxRef("MozMobileConnection.setCardLock()")}} methods fails.</td>
  </tr>
  <tr>
   <td>{{Event("iccinfochange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{DOMxRef("MozMobileConnection.iccInfo")}} object changes.</td>
  </tr>
  <tr>
   <td>{{Event("localized")}}</td>
   <td></td>
   <td><em><a href="https://github.com/fabi1cazenave/webL10n">Mozilla Specific</a></em></td>
   <td>The page has been localized using data-l10n-* attributes.</td>
  </tr>
  <tr>
   <td>{{Event("mousewheel")}} {{Deprecated_Inline}}</td>
   <td></td>
   <td><a href="http://msdn.microsoft.com/en-us/library/ie/ms536951%28v=vs.85%29.aspx"><em>IE invented</em></a></td>
   <td>The wheel button of a pointing device is rotated.</td>
  </tr>
  <tr>
   <td>{{Event("MozAudioAvailable")}}</td>
   <td>{{DOMxRef("Event")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>The audio buffer is full and the corresponding raw samples are available.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozBeforeResize"><code>MozBeforeResize</code></a> {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A window is about to be resized.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowseractivitydone")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when some activity has been completed (complete description TBD.)</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserasyncscroll")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the scroll position within a browser<code> </code>{{HTMLElement("iframe")}} changes.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowseraudioplaybackchange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when audio starts or stops playing within the browser {{HTMLElement("iframe")}} content.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsercaretstatechanged")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the text selected inside the browser {{HTMLElement("iframe")}} content changes.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserclose")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when window.close() is called within a browser {{HTMLElement("iframe")}}.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsercontextmenu")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a browser {{HTMLElement("iframe")}} try to open a context menu.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserdocumentfirstpaint")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a new paint occurs on any document in the browser {{HTMLElement("iframe")}}.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsererror")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when an error occured while trying to load a content within a browser iframe</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserfindchange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a search operation is performed on the browser {{HTMLElement("iframe")}} content (see <a href="/zh-CN/docs/Web/API/HTMLIFrameElement#Search_methods">HTMLIFrameElement search methods</a>.)</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserfirstpaint")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the {{HTMLElement("iframe")}} paints content for the first time (this doesn't include the initial paint from <em>about:blank</em>.)</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsericonchange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the favicon of a browser iframe changes.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserlocationchange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when an browser iframe's location changes.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserloadend")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the browser iframe has finished loading all its assets.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserloadstart")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the browser iframe starts to load a new page.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsermanifestchange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a the path to the app manifest changes, in the case of a browser {{HTMLElement("iframe")}} with an open web app embedded in it.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsermetachange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a {{htmlelement("meta")}} elelment is added to, removed from or changed in the browser {{HTMLElement("iframe")}}'s content.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowseropensearch")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a link to a search engine is found.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowseropentab")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when a new tab is opened within a browser {{HTMLElement("iframe")}} as a result of the user issuing a command to open a link target in a new tab (for example <kbd>ctrl</kbd>/<kbd>cmd</kbd> + click.)</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowseropenwindow")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when {{DOMxRef("window.open()")}} is called within a browser iframe.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserresize")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the browser {{HTMLElement("iframe")}}'s window size has changed.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserscroll")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the browser {{HTMLElement("iframe")}} content scrolls.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserscrollareachanged")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the available scrolling area in the browser {{HTMLElement("iframe")}} changes. This can occur on resize and when the page size changes (while loading for example.)</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserscrollviewchange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when asynchronous scrolling (i.e. APCZ) starts or stops.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsersecuritychange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the SSL state changes within a browser iframe.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserselectionstatechanged")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the text selected inside the browser {{HTMLElement("iframe")}} content changes. Note that this is deprecated, and newer implementations use {{Event("mozbrowsercaretstatechanged")}} instead.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsershowmodalprompt")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when {{DOMxRef("window.alert","alert()")}}, {{DOMxRef("window.confirm","confirm()")}} or {{DOMxRef("window.prompt","prompt()")}} are called within a browser iframe</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowsertitlechange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the document.title changes within a browser iframe.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowserusernameandpasswordrequired")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when an HTTP authentification is requested.</td>
  </tr>
  <tr>
   <td>{{Event("mozbrowservisibilitychange")}}</td>
   <td></td>
   <td><em>Firefox OS <a href="/zh-CN/docs/Web/API/Browser_API">Browser API</a>-specific</em></td>
   <td>Sent when the visibility state of the current browser iframe {{HTMLElement("iframe")}} changes, for example due to a call to {{DOMxRef("HTMLIFrameElement.setVisible","setVisible()")}}.</td>
  </tr>
  <tr>
   <td>{{Event("MozGamepadButtonDown")}}</td>
   <td></td>
   <td><em>To be specified</em></td>
   <td>A gamepad button is pressed down.</td>
  </tr>
  <tr>
   <td>{{Event("MozGamepadButtonUp")}}</td>
   <td></td>
   <td><em>To be specified</em></td>
   <td>A gamepad button is released.</td>
  </tr>
  <tr>
   <td>{{Event("MozMousePixelScroll")}} {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>The wheel button of a pointing device is rotated (detail attribute is a number of pixels). (use wheel instead)</td>
  </tr>
  <tr>
   <td>{{Event("MozOrientation")}} {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>Fresh data is available from an orientation sensor (see deviceorientation).</td>
  </tr>
  <tr>
   <td>{{Event("MozScrolledAreaChanged")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>The document view has been scrolled or resized.</td>
  </tr>
  <tr>
   <td>{{Event("moztimechange")}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>The time of the device has been changed.</td>
  </tr>
  <tr>
   <td><a href="/en-US/DOM/Touch_events_(Mozilla_experimental)">MozTouchDown</a> {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A touch point is placed on the touch surface (use touchstart instead).</td>
  </tr>
  <tr>
   <td><a href="/en-US/DOM/Touch_events_(Mozilla_experimental)">MozTouchMove</a> {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A touch point is moved along the touch surface (use touchmove instead).</td>
  </tr>
  <tr>
   <td><a href="/en-US/DOM/Touch_events_(Mozilla_experimental)">MozTouchUp</a> {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A touch point is removed from the touch surface (use touchend instead).</td>
  </tr>
  <tr>
   <td>{{Event("alerting")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The correspondent is being alerted (his/her phone is ringing).</td>
  </tr>
  <tr>
   <td>{{Event("busy")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The line of the correspondent is busy.</td>
  </tr>
  <tr>
   <td>{{Event("callschanged")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been added or removed from the list of current calls.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/DOM/onconnected">onconnected</a> {{Event("connected")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been connected.</td>
  </tr>
  <tr>
   <td>{{Event("connecting")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to connect.</td>
  </tr>
  <tr>
   <td>{{Event("delivered")}}</td>
   <td>{{DOMxRef("SMSEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An SMS has been successfully delivered.</td>
  </tr>
  <tr>
   <td>{{Event("dialing")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The number of a correspondent has been dialed.</td>
  </tr>
  <tr>
   <td>{{Event("disabled")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>Wifi has been disabled on the device.</td>
  </tr>
  <tr>
   <td>{{Event("disconnected")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been disconnected.</td>
  </tr>
  <tr>
   <td>{{Event("disconnecting")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to disconnect.</td>
  </tr>
  <tr>
   <td>{{Event("enabled")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>Wifi has been enabled on the device.</td>
  </tr>
  <tr>
   <td>{{Event("error_(Telephony)","error")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An error occurred.</td>
  </tr>
  <tr>
   <td>{{Event("held")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call has been held.</td>
  </tr>
  <tr>
   <td>{{Event("holding")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to be held.</td>
  </tr>
  <tr>
   <td>{{Event("incoming")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is being received.</td>
  </tr>
  <tr>
   <td>{{Event("received")}}</td>
   <td>{{DOMxRef("SMSEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An SMS has been received.</td>
  </tr>
  <tr>
   <td>{{Event("resuming")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>A call is about to resume.</td>
  </tr>
  <tr>
   <td>{{Event("sent")}}</td>
   <td>{{DOMxRef("SMSEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>An SMS has been sent.</td>
  </tr>
  <tr>
   <td>{{Event("statechange")}}</td>
   <td>{{DOMxRef("CallEvent")}}</td>
   <td><em>To be specified</em></td>
   <td>The state of a call has changed.</td>
  </tr>
  <tr>
   <td>{{Event("statuschange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The status of the Wifi connection changed.</td>
  </tr>
  <tr>
   <td>{{Event("overflow")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>An element has been overflowed by its content or has been rendered for the first time in this state (only works for elements styled with <code>overflow</code> != <code>visible</code>).</td>
  </tr>
  <tr>
   <td>{{Event("smartcard-insert")}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A <a href="/zh-CN/docs/JavaScript_crypto">smartcard</a> has been inserted.</td>
  </tr>
  <tr>
   <td>{{Event("smartcard-remove")}}</td>
   <td></td>
   <td><em>Mozilla specific</em></td>
   <td>A <a href="/zh-CN/docs/JavaScript_crypto">smartcard</a> has been removed.</td>
  </tr>
  <tr>
   <td>{{Event("stkcommand")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The <abbr title="SIM Application Toolkit">STK</abbr> Proactive Command is issued from <abbr title="Integrated Circuit Card">ICC</abbr>.</td>
  </tr>
  <tr>
   <td>{{Event("stksessionend")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The <abbr title="SIM Application Toolkit">STK</abbr> Session is terminated by <abbr title="Integrated Circuit Card">ICC</abbr>.</td>
  </tr>
  <tr>
   <td>{{Event("touchenter")}}</td>
   <td>{{DOMxRef("TouchEvent")}}</td>
   <td><a href="http://www.w3.org/TR/touch-events/#the-touchstart---------event">Touch Events</a> Removed</td>
   <td></td>
  </tr>
  <tr>
   <td>{{Event("touchleave")}}</td>
   <td>{{DOMxRef("TouchEvent")}}</td>
   <td><a href="http://www.w3.org/TR/touch-events/#the-touchstart---------event">Touch Events</a> Removed</td>
   <td></td>
  </tr>
  <tr>
   <td>{{Event("underflow")}}</td>
   <td>{{DOMxRef("UIEvent")}}</td>
   <td><em>Mozilla specific</em></td>
   <td>An element is no longer overflowed by its content (only works for elements styled with <code>overflow</code> != <code>visible</code>).</td>
  </tr>
  <tr>
   <td><code>uploadprogress</code> {{Deprecated_Inline}}</td>
   <td>{{DOMxRef("ProgressEvent")}}</td>
   <td><em>Mozilla Specific</em></td>
   <td>Upload is in progress (see {{Event("progress")}}).</td>
  </tr>
  <tr>
   <td>
    <p>{{Event("ussdreceived")}}</p>
   </td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>A new <abbr title="Unstructured Supplementary Service Data">USSD</abbr> message is received</td>
  </tr>
  <tr>
   <td>{{Event("voicechange")}}</td>
   <td></td>
   <td><em>Firefox OS specific</em></td>
   <td>The {{DOMxRef("MozMobileConnection.voice")}} object changes values.</td>
  </tr>
  <tr>
   <td>{{Event("msContentZoom")}}</td>
   <td></td>
   <td><em>Microsoft specific</em></td>
   <td></td>
  </tr>
  <tr>
   <td>{{Event("MSManipulationStateChanged")}}</td>
   <td></td>
   <td><em>Microsoft specific</em></td>
   <td></td>
  </tr>
  <tr>
   <td>{{Event("MSPointerHover")}} {{Deprecated_Inline}}</td>
   <td></td>
   <td><em>Microsoft specific</em></td>
   <td></td>
  </tr>
 </tbody>
</table>

<h2 id="Mozilla_特定事件">Mozilla 特定事件</h2>

<div class="blockIndicator note">
<p><strong>备注：</strong> 这些事件不会暴露给 Web 内容使用，只能在 chrome 内容的上下文中使用。</p>
</div>

<h3 id="XUL_事件">XUL 事件</h3>

<table class="standard-table">
 <thead>
  <tr>
   <th>Event Name</th>
   <th>Event Type</th>
   <th>Specification</th>
   <th>Fired when...</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Event("broadcast")}}</td>
   <td></td>
   <td><a href="/zh-CN/docs/XUL/Tutorial/Broadcasters_and_Observers#Broadcast_event">XUL</a></td>
   <td>An <code>observer</code> noticed a change to the attributes of a watched broadcaster.</td>
  </tr>
  <tr>
   <td>{{Event("CheckboxStateChange")}}</td>
   <td></td>
   <td>XUL</td>
   <td>The state of a <code>checkbox</code> has been changed either by a user action or by a script (useful for accessibility).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/close_event">close</a></td>
   <td></td>
   <td>XUL</td>
   <td>The close button of the window has been clicked.</td>
  </tr>
  <tr>
   <td>{{Event("command")}}</td>
   <td></td>
   <td>XUL</td>
   <td>An element has been activated.</td>
  </tr>
  <tr>
   <td>{{Event("commandupdate")}}</td>
   <td></td>
   <td>XUL</td>
   <td>A command update occurred on a <code>commandset</code> element.</td>
  </tr>
  <tr>
   <td>{{Event("DOMMenuItemActive")}}</td>
   <td></td>
   <td>XUL</td>
   <td>A menu or menuitem has been hovered or highlighted.</td>
  </tr>
  <tr>
   <td>{{Event("DOMMenuItemInactive")}}</td>
   <td></td>
   <td><em>XUL</em></td>
   <td>A menu or menuitem is no longer hovered or highlighted.</td>
  </tr>
  <tr>
   <td>{{Event("popuphidden")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-CN/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip has been hidden.</td>
  </tr>
  <tr>
   <td>{{Event("popuphiding")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-CN/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip is about to be hidden.</td>
  </tr>
  <tr>
   <td>{{Event("popupshowing")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-CN/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip is about to become visible.</td>
  </tr>
  <tr>
   <td>{{Event("popupshown")}}</td>
   <td><code>PopupEvent</code></td>
   <td><a href="/zh-CN/docs/XUL/PopupGuide/PopupEvents"><em>XUL</em></a></td>
   <td>A menupopup, panel or tooltip has become visible.</td>
  </tr>
  <tr>
   <td>{{Event("RadioStateChange")}}</td>
   <td></td>
   <td>XUL</td>
   <td>The state of a <code>radio</code> has been changed either by a user action or by a script (useful for accessibility).</td>
  </tr>
  <tr>
   <td>{{Event("ValueChange")}}</td>
   <td></td>
   <td>XUL</td>
   <td>The value of an element has changed (a progress bar for example, useful for accessibility).</td>
  </tr>
 </tbody>
</table>

<h3 id="附加组件特定事件">附加组件特定事件</h3>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Event Type</th>
   <th scope="col">Specification</th>
   <th scope="col">Fired when...</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozSwipeGesture">MozSwipeGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A touch point is swiped across the touch surface</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozMagnifyGestureStart">MozMagnifyGestureStart</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points start to move away from each other.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozMagnifyGestureUpdate">MozMagnifyGestureUpdate</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points move away from each other (after a MozMagnifyGestureStart).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozMagnifyGesture">MozMagnifyGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points moved away from each other (after a sequence of MozMagnifyGestureUpdate).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozRotateGestureStart">MozRotateGestureStart</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points start to rotate around a point.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozRotateGestureUpdate">MozRotateGestureUpdate</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points rotate around a point (after a MozRotateGestureStart).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozRotateGesture">MozRotateGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points rotate around a point (after a sequence of MozRotateGestureUpdate).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozTapGesture">MozTapGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Two touch points are tapped on the touch surface.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozPressTapGesture">MozPressTapGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A "press-tap" gesture happened on the touch surface (first finger down, second finger down, second finger up, first finger up).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozEdgeUIGesture">MozEdgeUIGesture</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A touch point is swiped across the touch surface to invoke the edge UI (Win8 only).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozAfterPaint">MozAfterPaint</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Content has been repainted.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMPopupBlocked">DOMPopupBlocked</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A popup has been blocked</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMWindowCreated">DOMWindowCreated</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window has been created.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMWindowClose">DOMWindowClose</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window is about to be closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMTitleChanged">DOMTitleChanged</a></td>
   <td></td>
   <td><em>Addons specifc</em></td>
   <td>The title of a window has changed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMLinkAdded">DOMLinkAdded</a></td>
   <td></td>
   <td><em>Addons specifc</em></td>
   <td>A link has been added a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMLinkRemoved">DOMLinkRemoved</a></td>
   <td></td>
   <td><em>Addons specifc</em></td>
   <td>A link has been removed inside from a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMMetaAdded">DOMMetaAdded</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code>meta</code> element has been added to a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMMetaRemoved">DOMMetaRemoved</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code>meta</code> element has been removed from a document.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMWillOpenModalDialog">DOMWillOpenModalDialog</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A modal dialog is about to open.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMModalDialogClosed">DOMModalDialogClosed</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A modal dialog has been closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMAutoComplete">DOMAutoComplete</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The content of an element has been auto-completed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/DOMFrameContentLoaded">DOMFrameContentLoaded</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The frame has finished loading (but not its dependent resources).</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/AlertActive">AlertActive</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code><a href="/zh-CN/docs/XUL/notification">notification</a></code> element is shown.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/AlertClose">AlertClose</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A <code><a href="/zh-CN/docs/XUL/notification">notification</a></code> element is closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/fullscreen">fullscreen</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Browser fullscreen mode has been entered or left.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/sizemodechange">sizemodechange</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>Window has entered/left fullscreen mode, or has been minimized/unminimized.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/MozEnteredDomFullscreen">MozEnteredDomFullscreen</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td><a href="/zh-CN/docs/DOM/Using_full-screen_mode">DOM fullscreen</a> mode has been entered.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/SSWindowClosing">SSWindowClosing</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The session store will stop tracking this window.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/SSTabClosing">SSTabClosing</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>The session store will stop tracking this tab.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/SSTabRestoring">SSTabRestoring</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab is about to be restored.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/SSTabRestored">SSTabRestored</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been restored.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/SSWindowStateReady">SSWindowStateReady</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window state has switched to "ready".</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/SSWindowStateBusy">SSWindowStateBusy</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A window state has switched to "busy".</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabOpen">TabOpen</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been opened.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabClose">TabClose</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been closed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabSelect">TabSelect</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been selected.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabShow">TabShow</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been shown.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabHide">TabHide</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been hidden.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabPinned">TabPinned</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been pinned.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/TabUnpinned">TabUnpinned</a></td>
   <td></td>
   <td><em>Addons specific</em></td>
   <td>A tab has been unpinned.</td>
  </tr>
 </tbody>
</table>

<h3 id="开发者工具特定事件">开发者工具特定事件</h3>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Event Name</th>
   <th scope="col">Event Type</th>
   <th scope="col">Specification</th>
   <th scope="col">Fired when...</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/CssRuleViewRefreshed">CssRuleViewRefreshed</a></td>
   <td></td>
   <td><em>devtools specific</em></td>
   <td>The "Rules" view of the style inspector has been updated.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/CssRuleViewChanged">CssRuleViewChanged</a></td>
   <td></td>
   <td><em>devtools specific</em></td>
   <td>The "Rules" view of the style inspector has been changed.</td>
  </tr>
  <tr>
   <td><a href="/zh-CN/docs/Web/Reference/Events/CssRuleViewCSSLinkClicked">CssRuleViewCSSLinkClicked</a></td>
   <td></td>
   <td><em>devtools specific</em></td>
   <td>A link to a CSS file has been clicked in the "Rules" view of the style inspector.</td>
  </tr>
 </tbody>
</table>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="参见">参见</h2>

<ul>
 <li>{{DOMxRef("Event")}}</li>
 <li><a href="/zh-CN/docs/Web/Guide/DOM/Events">事件开发者指南</a></li>
</ul>