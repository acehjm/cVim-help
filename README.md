cVim--help
------

cVim([GitHub:1995eaton/chromium-vim)](https://github.com/1995eaton/chromium-vim)，ViChrome和vimium都是Chrome的Vim扩展，使用了大量的快捷键，其实就是使用键盘来操作Chrome浏览器的行为，对geeker来说是极好的。ViChrome更切合vim的默认键，但是和chrome本身的某些默认键有冲突，会造成习惯上的差别，vimium简单点，cVim则更加强大。它支持自定义搜索引擎，像谷歌/IMDB/维基/亚马逊/Duckduckgo/雅虎/Bing搜索等，历史与书签搜索，插入符号/可视模式，有效链接提示，自定义键盘映射，正则表达式搜索页面用突出，平滑滚动等。

------

## Keybindings（快捷键）

|Movement	|              |	                   Mapping name|
|:-------------------------|:----------------|:----|
|`j, s`	|向下轻微滚动|	scrollDown|
|`k, w`	|向上轻微滚动|	scrollUp|
|`h	`|向左轻微滚动|	scrollLeft|
|`l`	|向右轻微滚动|	scrollRight|
|`d	`|向下滚动当前页面的一半|	scrollPageDown|
|`unmapped`	|向下滚动一个页面|	scrollFullPageDown|
|`u, e`|	向上滚动当前页面的一半|	scrollPageUp|
|`unmapped`	|向上滚动一个页面|	scrollFullPageUp|
|`gg`	|滚动到页面顶部	|scrollToTop|
|`G`|	滚动到页面底部|	scrollToBottom|
|`0	`|滚动到页面左侧	|scrollToLeft|
|`$`|	滚动到页面右侧|	scrollToRight|
|`gi`|	定位到第一个输入框|	goToInput|
|`gI`	|转到最后集中输入框|	goToLastInput|
|`zz`|	中心页面，当前的搜索匹配（中）|	centerMatchH|
|`zt`|中心页面，当前的搜索匹配（上）|	centerMatchT|
|`zb`|中心页面，当前的搜索匹配（下）|	centerMatchB|
|Link Hints		
|`f`|在当前标签页中打开链接|	createHint|
|`F`|在新标签页中打开链接|	createTabbedHint|
|`unmapped`|在新标签页中打开链接（主动）|createActiveTabbedHint|
|`W`|在新窗口中打开链接|	createHintWindow|
|`A`|重复最后一个命令|	openLastHint|
|`q`|触发悬停事件(鼠标悬停+mouseenter)|createHoverHint|
|`Q	`|触发悬停事件(鼠标移出+鼠标离开)|	createUnhoverHint|
|`mf`|打开多个链接|	createMultiHint|
|`unmapped`|外部编辑器编辑文本	|createEditHint|
|`unmapped`|调用代码块的链接作为第一个参数|createScriptHint(`<FUNCTION_NAME>`)|
|`mr`	|逆转影像搜索的多个链接	|multiReverseImage|
|`my`|	抽出多个链接（打开与P链接列表）|	multiYankUrl|
|`gy`	|复制URL链接到剪贴板|	yankUrl|
|`gr`	|逆转图片搜索（google图片|reverseImage|
|`;	`|更改链接重点提示|
|QuickMarks		
|`M<*>`|	创建快速标记 <*>|	addQuickMark|
|`go<*>`|打开快速标记 <*> 在当前页面|	openQuickMark|
|`gn<*>`|在新窗口中打开快速标记<*>`<N>`次|openQuickMarkTabbed|Miscellaneous		
|`a`|	相当于 ":tabnew google "|	:tabnew google|
|`.`|	重复上一个命令|	repeatCommand||
|`:`|	打开命令栏|	openCommandBar|
|`/`|	打开搜索栏|	openSearchBar|
|`?`|	打开搜索栏(反向搜索)|	openSearchBarReverse|
|`I	`|搜索浏览器历史记录	|:history|
|`<N>g%`|	向下滚页面的`<N>％`|	percentScroll|
|`<N>unmapped`|pass`<N>`keys through to the current page|passKeys|
|`zr`|	重启chrome	|:chrome://restart`<CR>`
|`i`|	进入插入模式（Escape退出）|	insertMode|
|`r	`|重新加载当前标签|	reloadTab|
|`gR`|	重新加载当前选项卡+本地高速缓存	|reloadTabUncached|
|`;<*>`|	创建标签 <*>|	setMark|
|`''`|	到最后滚动位置	|lastScrollPosition|
|'<*>`|	转到标识 <*>|	goToMark|
|`none`|	重载所有标签|	reloadAllTabs|
|`cr`|	在当前页面重新加载所有选项卡|	reloadAllButCurrent|
|`zi`	|缩放页面（缩小）|	zoomPageIn|
|`zo`	|缩放页面（放大）|zoomPageOut|
|`z0`|	缩放页面到原始尺寸|	zoomOrig|
|`z<Enter>`|切换图像变焦（相当于点击图像只有页面图像）|toggleImageZoom|
|`gd`|相当于:chrome://downloads`<CR>`	|:chrome://downloads`<CR>`|
|`yy`|	复制当前页面的url到剪贴板|	yankDocumentUrl|
|`ya`|	复制当前窗口的所有url|	yankWindowUrls|
|`yh`	|复制查找目前匹配的文本（若存在）|	yankHighlight|
|`b`|	书签搜索|	:bookmarks|
|`p`|	在当前标签页打开剪贴板并搜索剪贴板内容|	openPaste|
|`P`|	在新标签中打开剪贴板并搜索剪贴板内容|	openPasteTab|
|`gj`	|隐藏下载文件|	hideDownloadsShelf|
|`gf`|	随机打开页面内链接|	nextFrame|
|`gF`	|到根目录|	rootFrame|
|`gq`	|停止加载当前页面|	cancelWebRequest|
|`gQ`	|停止加载所有页面|	cancelAllWebRequests|
|`gu`	|返回上一个链接|	goUpUrl|
|`gU`	|返回根url	|goToRootUrl|
|`gs`|	查看当前页面的源代码|	goToSource|
|`<C-b>`	|在当前URL创建或切换书签|createBookmark|
|`unmapped`|	关闭所有浏览器窗口|	quitChrome|
|`g-`	|在URL路径的第一个数字上递减(www.example.com/5=>www.example.com/4)|decrementURLPath|
|`g+`	|在URL路径的第一个数字上递增|	incrementURLPath|
|TabNavigation		
|`gt, K, R`|	导航到下一个标签页|	nextTab|
|`gT, J, E`|	导航到上一个标签页|	previousTab|
|`g0, g$`	|转到第一/最后一个标签页|	firstTab, lastTab|
|`<C-S-h>, gh`|在新标签中打开当前标签页使用过的最后一个URL|openLastLinkInTab
|`<C-S-l>, gl`|在新标签中打开当前标签页使用过的下一个URL|openNextLinkInTab
|`x`|	关闭当前标签页|	closeTab|
|`gxT`|	关闭当前标签页的左侧标签页|	closeTabLeft|
|`gxt`|	关闭当前标签页的右侧标签页|	closeTabRight|
|`gx0`|	关闭当前标签页左侧的所有标签页|	closeTabsToLeft|
|`gx$`|	关闭当前标签页右侧的所有标签页|	closeTabsToRight|
|`X`|	打开最后一个关闭的标签页|	lastClosedTab|
|`t`|	:tabnew（新标签页）	|:tabnew|
|`T`|	:tabnew `<CURRENT URL>`（当前标签页）|	:tabnew @%|
|`O`|	:open`<CURRENT URL>`（打开当前页）	|:open @%|
|`<N>%`|	调到第N个标签页	|goToTab|
|`H, S`|	返回|	goBack|
|`L, D`	|前进||	goForward|
|`B`|	寻找另一活动标签|	:buffer|
|`<	`|左移当前标签||	moveTabLeft|
|`>`|	右移当前标签|	moveTabRigh|
|`]]`	|点击页面上的“下一个”链接	|nextMatchPattern|
|`[[`	|点击页面上的“返回”链接	|previousMatchPattern|
|`gp`	|固定/解固定当前选项卡|	pinTab|
|`<C-6>`|	切换到上次使用的选项卡之间的中点|lastUsedTab|
|Find Mode		
|`n	`|下一条搜索结果|	nextSearchResult|
|`N`	|上一条搜索结果|	previousSearchResult|
|`v`|进入可视化/插入符号模式(高亮当前搜索/选择)|toggleVisualMode
|`V`|从插入符模式/当前突出显示搜索进入视线模式|	toggleVisualLineMode
|Visual/CaretMode		
|`<Esc>`|退出可视化/字符/插入符号模式到正常模式|	
|`v`|	在视觉/插入符模式之间进行切换|	
|`h, j, k, l`|	移动光标的位置/扩展可视选择	|
|`y	`|复制当前选择	|
|`p`|	打开当前选项卡中突出显示的文本	|
|`P`|	打开新标签突出显示的文本	|
|Text boxes		
|`<C-i>`|	将光标移到行的开始|	beginningOfLine|
|`<C-e>`|	将光标移到行的末尾|	endOfLine|
|`<C-u>`|	删除的行的开始|	deleteToBeginning|
|`<C-o>`|	删除到行尾|	deleteToEnd|
|`<C-y>`|	删除后面一个字|	deleteWord|
|`<C-p>`|	向前删除一个字|	deleteForwardWord|
|unmapped|删除后面一个字符|deleteChar|
|unmapped|删除前面一个字符|deleteForwardChar|
|`<C-h>`|光标向后移动一个字|backwardWord|
|`<C-l>`|光标向前移动一个字|forwardWord|
|`<C-f>`|将光标前移一个字母|forwardChar|
|`<C-b>`|将光标后移一个字母|backwardChar|
|`<C-j>`|光标向前移动一行|forwardLine|
|`<C-k>`|光标向后移动一行|backwardLine|
|`unmapped`|选择输入文本(相当于`<C-A>`)|	selectAll|
|`unmapped`|在Vim终端编辑(需要cvim_server.py脚本运行)|editWithVim|

##Command Mode（命令模式）

|Command|	Description|
|:----|:----|:----|
|`:tabnew (autocomplete)`	|打开一个新标签并且输入完成搜索|
|`:new (autocomplete)`|	打开一个新窗口并且输入完成搜索|
|`:open (autocomplete)`|	打开输入/ URL完成/谷歌搜索|
|`:history (autocomplete)`|	搜索浏览器历史记录|
|`:bookmarks (autocomplete)`|	搜索书签|
|`:bookmarks/<folder>(autocomplete)`|	打开某个文件夹的所有书签|
|`:set (autocomplete)`|	临时更改cVim设置|
|`:chrome://(autocomplete)`|	打开一个chrome://URL|
|`:tabhistory (autocomplete)`	|在当前页浏览历史|
|`:quit`|	关闭当前页|
|`:qall`|	关闭当前窗口|
|`:restore(autocomplete)`|恢复之前关闭的选项卡(较新版本的Chrome)|
|`:tabattach (autocomplete)`|	将当前标签页移到其它窗口|
|`:tabdetach`|移动当前标签页到一个新窗口|
|`:file(autocomplete)[expirimental]`|打开本地文件|
|`:duplicate`|复制当前选项卡|
|`:settings`|打开设置页|
|`:nohlsearch`|清除最后搜索突出显示的文本|
|`:execute`|执行键序列(“图记者：执行2J`<CR>`”)|
|`:buffer(autocomplete)`|改变不同的标签|
|`:mksession`|在活动窗口的当前标签页创建新session|
|`:delsession(autocomplete)`|删除一个已经保存的session|
|`:session (autocomplete)`|从保存的会话标签中打开一个新的窗口|
|`:script`|在当前标签页运行javascript|
|`:togglepin`|切换当前选项卡的固定状态|
|`:pintab`|固定当前标签页|
|`:unpintab`|取消当前标签页的固定|


作者 [@ace_him](https://github.com/acehjm)     
2015 年 04月 16日    
