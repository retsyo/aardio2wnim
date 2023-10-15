# 这是啥

将[aardio](https://www.aardio.com/)的界面转换给[wNim](https://github.com/khchen/wNim)使用

# 窗体类型对应表

| 是否支持转换 | aardio中的窗体类型 | wNim中对应窗体 | 备注 |
| ------------ | ------------------ | -------------- | ---- |
| √            | win.form           | Frame上的Panel |      |
|              |                    | Window         |      |
|              |                    | ToolTip        |      |

# 菜单类型对应表

| 是否支持转换 | aardio中的菜单类型 | wNim中对应菜单 | 备注 |
| ------------ | ------------------ | -------------- | ---- |
|              |                    | MenuBar        |      |
|              |                    | Menu           |      |
|              |                    | MenuItem       |      |
# 控件对应表

| 是否支持转换 | aardio中的cls | wNim中对应控件                                               | 生成事件处理代码                                | 备注                                                         |
| ------------ | ------------- | ------------------------------------------------------------ | ----------------------------------------------- | ------------------------------------------------------------ |
| √            | button        | [wButton](https://khchen.github.io/wNim/wButton.html)        | wEvent_Button                                   | 即便wNim设置backgroundColor，也这是在按键外边画了这个颜色的框<br>设置foregroundColor，没效果<br/><br/>[wButton](https://khchen.github.io/wNim/wButton.html)还可以放图片/图标 |
| √            | calendar      | [wCalendarCtrl](https://khchen.github.io/wNim/wCalendarCtrl.html) |                                                 |                                                              |
| √            | checkbox      | [wCheckBox](https://khchen.github.io/wNim/wCheckBox.html)    |                                                 |                                                              |
| √            | checklist     | [wCheckComboBox](https://khchen.github.io/wNim/wCheckComboBox.html) |                                                 |                                                              |
| √            | combobox      | [wComboBox](https://khchen.github.io/wNim/wComboBox.html)    |                                                 |                                                              |
| √            | datetimepick  | [wDatePickerCtrl](https://khchen.github.io/wNim/wDatePickerCtrl.html) |                                                 |                                                              |
| √            | edit          | [wTextCtrl](https://khchen.github.io/wNim/wTextCtrl.html)    |                                                 |                                                              |
| √            | richedit      | [wTextCtrl](https://khchen.github.io/wNim/wTextCtrl.html)    |                                                 | style=wTeRich                                                |
| √            | groupbox      | [wStaticBox](https://khchen.github.io/wNim/wStaticBox.html)  |                                                 |                                                              |
| √            | ipaddress     | [wIpCtrl](https://khchen.github.io/wNim/wIpCtrl.html)        |                                                 | wNim未限定只能输入数字、无法设置允许IP范围                   |
| ⍻            | listbox       | [wListBox](https://khchen.github.io/wNim/wListBox.html)      |                                                 |                                                              |
| ⍻            | listview      | [wListCtrl](https://khchen.github.io/wNim/wListCtrl.html)    |                                                 |                                                              |
| √            | progress      | [wGauge](https://khchen.github.io/wNim/wGauge.html)          |                                                 | plus控件有太多种用途，这里只在指定background的时候，把它当作picturebox |
| ⍻            | plus          | [wStaticBitmap](https://khchen.github.io/wNim/wStaticBitmap.html) |                                                 |                                                              |
| √            | picturebox    | [wStaticBitmap](https://khchen.github.io/wNim/wStaticBitmap.html) | 当设置有事件回调时，生成wEvent_CommandLeftClick | [wStaticBitmap](https://khchen.github.io/wNim/wStaticBitmap.html) 支持的图片类型较多<br>[wStaticBitmap](https://khchen.github.io/wNim/wStaticBitmap.html)不能设置自动等比例缩放图片以便适应控件大小 |
| √            | radiobutton   | [wRadioButton](https://khchen.github.io/wNim/wRadioButton.html) |                                                 |                                                              |
| √            | scrollbar     | [wScrollBar](https://khchen.github.io/wNim/wScrollBar.html)  |                                                 |                                                              |
| √            | spin          | [wSpinButton](https://khchen.github.io/wNim/wSpinButton.html) | wEvent_SpinUp 和 wEvent_SpinUp                  |                                                              |
| ⍻            | splitter      | [wSplitter](https://khchen.github.io/wNim/wSplitter.html)    |                                                 |                                                              |
| √            | static        | [wStaticText](https://khchen.github.io/wNim/wStaticText.html) |                                                 |                                                              |
| √            | hotkey        | [wHotkeyCtrl](https://khchen.github.io/wNim/wHotkeyCtrl.html) |                                                 |                                                              |
| ⍻            | tab           | [wNoteBook](https://khchen.github.io/wNim/wNoteBook.html)    |                                                 |                                                              |
| √            | trackbar      | [wSlider](https://khchen.github.io/wNim/wSlider.html)        |                                                 | [wSlider](https://khchen.github.io/wNim/wSlider.html)不显示刻度。拉动时，tooltip不能实时显示当前读数 |
| ⍻            | custom        |                                                              |                                                 | 暂时输出为StaticText。拟通过分析变量名，支持以下在aardio界面设计器中没有的控件，以及其它控件 |
|              |               | [wStatusBar](https://khchen.github.io/wNim/wStatusBar.html)  |                                                 |                                                              |
|              |               | [wToolBar](https://khchen.github.io/wNim/wToolBar.html)      |                                                 |                                                              |
|              |               | [wStaticLine](https://khchen.github.io/wNim/wStaticLine.html) |                                                 |                                                              |
|              |               | [wSpinCtrl](https://khchen.github.io/wNim/wSpinCtrl.html)    |                                                 | wTextCtrl和wSpinButton的组合                                 |
|              |               | [wTimePickerCtrl](https://khchen.github.io/wNim/wTimePickerCtrl.html) |                                                 |                                                              |
|              |               | [wTreeCtrl](https://khchen.github.io/wNim/wTreeCtrl.html)    |                                                 |                                                              |
|              |               | [wHyperlinkCtrl](https://khchen.github.io/wNim/wHyperlinkCtrl.html) |                                                 |                                                              |
|              |               | [wWebView](https://khchen.github.io/wNim/wWebView.html)      |                                                 | wNim不支持webview2                                           |
|              |               | [wRebar](https://khchen.github.io/wNim/wRebar.html)          |                                                 |                                                              |
|              |               | [wMenuBarCtrl](https://khchen.github.io/wNim/wMenuBarCtrl.html) |                                                 |                                                              |



# 历史

- 2023某年某月某日（管它呢，先立个flag）
  - 提供GUI使用界面
    - 可选界面、文字大小是否可以缩放
    - 可选是否输出为Python模块      
  - 公开发布
  - 支持splitter、tab
  - 根据自定义控件的名字，生成更多控件（包括菜单、状态条、rebar、StaticLine）的代码。不过好像有些控件有没有关系不大
  - 开源？
  - 有没有其它小巧、支持更多控件、靠拖拽（即使用绝对坐标）放置控件的界面设计器？
  - 将wxGlade之类使用grid方式布局的界面，转成wNim的autolayout。不过工作量大，意义不大？
  - 支持wNim以外的库（比如iup？），以便支持跨平台  


- 20231015
  - 控件大小、文字随界面大小缩放

- 20231010
  - 为picturebox/wStaticBitmap 添加点击事件

- 20231004
  - aardio没有SpinCtrl，因为wSpinCtrl combines wTextCtrl and wSpinButton in one control.
  - aardio没有StaticLine
  
- 20231001    开始写
  - 最初使用python写。使用ShedSkin转换成EXE。但是使用中发现问题
  - 换用nim
