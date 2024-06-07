---
layout: single
title: "[Python Syntax 04] list"
tag:
  - Python
author_profile: false
use_math: false
---

[^]: python 가

<h3 style="font-size: 8px; margin-top: -45px; font-color: #434343;">
  <a href="https://potettang.github.io/Data%20Science/" style="text-decoration: none; color: #3c3c3c; background-color: #f8f9fa; border-radius: 20px; padding: 5px 10px; display: inline-block;">
    <img src="../images/ImgFile/bf.png" style="height: 12.33px; width: auto; margin-top: -4px; vertical-align: middle;" alt="Python 이미지">
    DATA SCIENCE / Python for Data Analysis
  </a>
</h3>



<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>list</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: normal } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0px solid transparent;
  border-right: 0px solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0px solid transparent;
  border-bottom: 0px solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
	border:1px solid transparent;
  background-color: transparent;
  position: absolute;
	z-index:1;
	right:3%;
	top: 0;
	bottom: 0;
	margin: auto;
	padding: 7px 0;
	display: none;
	vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
	content: "X";
	display: block;
	width: 15px;
	height: 15px;
	text-align: center;
	color:#000;
	font-weight: normal;
	font-size: 12px;
	cursor: pointer;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
  background: inherit;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-bottom:10px;
  margin-top:0; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  font-size:36px;
  line-height:40px; }

h2.bp3-heading, .bp3-running-text h2{
  font-size:28px;
  line-height:32px; }

h3.bp3-heading, .bp3-running-text h3{
  font-size:22px;
  line-height:25px; }

h4.bp3-heading, .bp3-running-text h4{
  font-size:18px;
  line-height:21px; }

h5.bp3-heading, .bp3-running-text h5{
  font-size:16px;
  line-height:19px; }

h6.bp3-heading, .bp3-running-text h6{
  font-size:14px;
  line-height:16px; }
.bp3-ui-text{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none; }

.bp3-monospace-text{
  font-family:monospace;
  text-transform:none; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  font-size:14px;
  line-height:1.5; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15);
    margin:20px 0; }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  color:#106ba3;
  text-decoration:none; }
  a:hover{
    color:#106ba3;
    cursor:pointer;
    text-decoration:underline; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  font-size:smaller;
  padding:2px 5px; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  color:#182026;
  display:block;
  font-size:13px;
  line-height:1.4;
  margin:10px 0;
  padding:13px 15px 12px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit;
    font-size:inherit;
    padding:0; }

.bp3-running-text kbd, .bp3-key{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-family:inherit;
  font-size:12px;
  height:24px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  line-height:24px;
  min-width:24px;
  padding:3px 6px;
  vertical-align:middle; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  margin:0 0 10px;
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    font-size:40px;
    margin-right:20px;
    margin-top:0; }

.bp3-alert-contents{
  word-break:break-word; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  cursor:default;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  height:30px;
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-breadcrumbs > li{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }
    .bp3-breadcrumbs > li::after{
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 00-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 001.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      content:"";
      display:block;
      height:16px;
      margin:0 5px;
      width:16px; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    font-size:inherit;
    font-weight:inherit;
    vertical-align:baseline; }

.bp3-breadcrumbs-collapsed{
  background:#ced9e0;
  border:none;
  border-radius:3px;
  cursor:pointer;
  margin-right:2px;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    content:"";
    display:block;
    height:16px;
    width:16px; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    color:#182026;
    text-decoration:none; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  min-height:30px;
  min-width:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      background-color:#106ba3;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      background-color:#0e5a8a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      background-color:#0d8050;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      background-color:#0a6640;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      background-color:#bf7326;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      background-color:#a66321;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      background-color:#c23030;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      background-color:#a82a2a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-height:40px;
    min-width:40px;
    font-size:16px;
    padding:5px 15px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      margin:0;
      position:absolute; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button.bp3-minimal:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button.bp3-outlined{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    border:1px solid rgba(24, 32, 38, 0.2);
    -webkit-box-sizing:border-box;
            box-sizing:border-box; }
    .bp3-button.bp3-outlined:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-outlined:active, .bp3-button.bp3-outlined.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-outlined{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-outlined:hover, .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-outlined:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover, .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover, .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover, .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover, .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled:hover{
      border-color:rgba(92, 112, 128, 0.1); }
    .bp3-dark .bp3-button.bp3-outlined{
      border-color:rgba(255, 255, 255, 0.4); }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        border-color:rgba(255, 255, 255, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      border-color:rgba(16, 107, 163, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        border-color:rgba(16, 107, 163, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        border-color:rgba(72, 175, 240, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          border-color:rgba(72, 175, 240, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      border-color:rgba(13, 128, 80, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        border-color:rgba(13, 128, 80, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        border-color:rgba(61, 204, 145, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          border-color:rgba(61, 204, 145, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      border-color:rgba(191, 115, 38, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        border-color:rgba(191, 115, 38, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        border-color:rgba(255, 179, 102, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          border-color:rgba(255, 179, 102, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      border-color:rgba(194, 48, 48, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        border-color:rgba(194, 48, 48, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        border-color:rgba(255, 115, 115, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          border-color:rgba(255, 115, 115, 0.2); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    border-bottom-right-radius:0;
    border-top-right-radius:0;
    margin-right:-1px; }
  .bp3-button-group.bp3-minimal .bp3-button{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      height:100%;
      width:unset; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  font-size:14px;
  line-height:1.5;
  background-color:rgba(138, 155, 168, 0.15);
  border-radius:3px;
  padding:10px 12px 9px;
  position:relative;
  width:100%; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout .bp3-heading{
    line-height:20px;
    margin-bottom:5px;
    margin-top:0; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  opacity:0.9;
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  width:100%; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }

.bp3-dialog{
  background:#ebf1f5;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text;
  width:500px; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    background:#293742;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-dialog-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding-left:20px;
  padding-right:5px;
  z-index:30; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    background:#30404d;
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  margin:20px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-multistep-dialog-panels{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }

.bp3-multistep-dialog-left-panel{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column; }
  .bp3-dark .bp3-multistep-dialog-left-panel{
    background:#202b33; }

.bp3-multistep-dialog-right-panel{
  background-color:#f5f8fa;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  border-radius:0 0 6px 0;
  -webkit-box-flex:3;
      -ms-flex:3;
          flex:3;
  min-width:0; }
  .bp3-dark .bp3-multistep-dialog-right-panel{
    background-color:#293742;
    border-left:1px solid rgba(16, 22, 26, 0.4); }

.bp3-multistep-dialog-footer{
  background-color:#ffffff;
  border-radius:0 0 6px 0;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  padding:10px; }
  .bp3-dark .bp3-multistep-dialog-footer{
    background:#30404d;
    border-top:1px solid rgba(16, 22, 26, 0.4); }

.bp3-dialog-step-container{
  background-color:#f5f8fa;
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-dialog-step-container{
    background:#293742;
    border-bottom:1px solid rgba(16, 22, 26, 0.4); }
  .bp3-dialog-step-container.bp3-dialog-step-viewed{
    background-color:#ffffff; }
    .bp3-dark .bp3-dialog-step-container.bp3-dialog-step-viewed{
      background:#30404d; }

.bp3-dialog-step{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#f5f8fa;
  border-radius:6px;
  cursor:not-allowed;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:4px;
  padding:6px 14px; }
  .bp3-dark .bp3-dialog-step{
    background:#293742; }
  .bp3-dialog-step-viewed .bp3-dialog-step{
    background-color:#ffffff;
    cursor:pointer; }
    .bp3-dark .bp3-dialog-step-viewed .bp3-dialog-step{
      background:#30404d; }
  .bp3-dialog-step:hover{
    background-color:#f5f8fa; }
    .bp3-dark .bp3-dialog-step:hover{
      background:#293742; }

.bp3-dialog-step-icon{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:rgba(92, 112, 128, 0.6);
  border-radius:50%;
  color:#ffffff;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:25px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:25px; }
  .bp3-dark .bp3-dialog-step-icon{
    background-color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#2b95d6; }
  .bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#8a9ba8; }

.bp3-dialog-step-title{
  color:rgba(92, 112, 128, 0.6);
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  padding-left:10px; }
  .bp3-dark .bp3-dialog-step-title{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-title{
    color:#2b95d6; }
  .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
    color:#182026; }
    .bp3-dark .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
      color:#f5f8fa; }
.bp3-drawer{
  background:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    height:50%;
    left:0;
    right:0;
    top:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-bottom{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-left{
    bottom:0;
    left:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-right{
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    background:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-drawer-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding:5px;
  padding-left:20px;
  position:relative; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  overflow:auto; }

.bp3-drawer-footer{
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  padding:10px 20px;
  position:relative; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  cursor:text;
  display:inline-block;
  max-width:100%;
  position:relative;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    bottom:-3px;
    left:-3px;
    position:absolute;
    right:-3px;
    top:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  color:inherit;
  display:inherit;
  font:inherit;
  letter-spacing:inherit;
  max-width:inherit;
  min-width:inherit;
  position:relative;
  resize:none;
  text-transform:inherit;
  vertical-align:top; }

.bp3-editable-text-input{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0;
  white-space:pre-wrap;
  width:100%; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    left:0;
    position:absolute;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    border-radius:inherit;
    z-index:2; }
    .bp3-control-group .bp3-input:focus{
      border-radius:3px;
      z-index:14; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    border-radius:inherit;
    z-index:4; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-left-container,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group .bp3-select:focus-within{
    z-index:5; }
  .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:-1px; }
  .bp3-control-group:not(.bp3-vertical) > .bp3-divider:not(:first-child){
    margin-left:6px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    border-radius:0 3px 3px 0;
    margin-right:0; }
  .bp3-control-group > :only-child{
    border-radius:3px;
    margin-right:0; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group .bp3-numeric-input:not(:first-child) .bp3-input-group{
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-control-group.bp3-fill{
    width:100%; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      border-radius:3px 3px 0 0;
      margin-top:0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  cursor:pointer;
  display:block;
  margin-bottom:10px;
  position:relative;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    left:0;
    opacity:0;
    position:absolute;
    top:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    cursor:pointer;
    display:inline-block;
    font-size:16px;
    height:1em;
    margin-right:10px;
    margin-top:-3px;
    position:relative;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none;
    vertical-align:middle;
    width:1em; }
    .bp3-control .bp3-control-indicator::before{
      content:"";
      display:block;
      height:1em;
      width:1em; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    background:#d8e1e8;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-left:10px;
    margin-top:1px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 00-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0012 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:auto; }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      background:#ffffff;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      height:calc(1em - 4px);
      left:0;
      margin:2px;
      position:absolute;
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      width:calc(1em - 4px); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    font-size:0.7em;
    text-align:center; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    line-height:0;
    margin-left:0.5em;
    margin-right:1.2em;
    visibility:hidden; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    line-height:1em;
    margin-left:1.2em;
    margin-right:0.5em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    line-height:1em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    line-height:0;
    visibility:hidden; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      background:#202b33;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  cursor:pointer;
  display:inline-block;
  height:30px;
  position:relative; }
  .bp3-file-input input{
    margin:0;
    min-width:200px;
    opacity:0; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      background:rgba(206, 217, 224, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(92, 112, 128, 0.6);
        cursor:not-allowed;
        outline:none; }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        background:rgba(57, 75, 89, 0.5);
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          -webkit-box-shadow:none;
                  box-shadow:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:rgba(92, 112, 128, 0.6);
  left:0;
  padding-right:80px;
  position:absolute;
  right:0;
  top:0;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-file-upload-input::after{
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026;
    min-height:24px;
    min-width:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    border-radius:3px;
    content:"Browse";
    line-height:24px;
    margin:3px;
    position:absolute;
    right:0;
    text-align:center;
    top:0;
    width:70px; }
    .bp3-file-upload-input::after:hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-file-upload-input:active::after{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-large .bp3-file-upload-input{
    font-size:16px;
    height:40px;
    line-height:40px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-height:30px;
      min-width:30px;
      line-height:30px;
      margin:5px;
      width:85px; }
  .bp3-dark .bp3-file-upload-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        background-color:#30404d;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        background-color:#202b33;
        background-image:none;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:active::after{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    color:#5c7080;
    font-size:12px;
    margin-top:5px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      line-height:40px;
      margin:0 10px 0 0; }
    .bp3-form-group.bp3-inline label.bp3-label{
      line-height:30px;
      margin:0 10px 0 0; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-input-left-container:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-input-left-container:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-height:24px;
    min-width:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-icon{
    z-index:1; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon{
    color:#5c7080; }
    .bp3-input-group > .bp3-input-left-container > .bp3-icon:empty,
    .bp3-input-group > .bp3-icon:empty{
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-height:30px;
    min-width:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle; }
  .bp3-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-input.bp3-large{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-bottom:15px;
  margin-top:0; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    font-weight:400;
    vertical-align:top;
    width:100%; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  min-height:0;
  padding:0;
  width:30px; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  -moz-appearance:none;
  -webkit-appearance:none;
  border-radius:3px;
  height:30px;
  padding:0 25px 0 10px;
  width:100%; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  background:none;
  -webkit-box-shadow:none;
          box-shadow:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    background:rgba(167, 182, 194, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026;
    text-decoration:none; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    background:rgba(115, 134, 148, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      color:rgba(167, 182, 194, 0.6);
      cursor:not-allowed; }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  font-size:16px;
  height:40px;
  padding-right:35px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    background-color:#202b33;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  background-color:rgba(206, 217, 224, 0.5);
  -webkit-box-shadow:none;
          box-shadow:none;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  color:#5c7080;
  pointer-events:none;
  position:absolute;
  right:7px;
  top:7px; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  letter-spacing:normal;
  position:relative;
  vertical-align:middle; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    right:12px;
    top:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select option:disabled, .bp3-dark
  .bp3-select option:disabled{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    text-align:left;
    vertical-align:top; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td,
  .bp3-running-text table tfoot tr:first-child th,
  table.bp3-html-table tfoot tr:first-child th,
  .bp3-running-text table tfoot tr:first-child td,
  table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td,
  .bp3-dark .bp3-running-text table tfoot tr:first-child th,
  .bp3-running-text .bp3-dark table tfoot tr:first-child th,
  .bp3-dark table.bp3-html-table tfoot tr:first-child th,
  .bp3-dark .bp3-running-text table tfoot tr:first-child td,
  .bp3-running-text .bp3-dark table tfoot tr:first-child td,
  .bp3-dark table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-bottom:6px;
  padding-top:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td,
table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
  table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table{ }
  .bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
    background:rgba(92, 112, 128, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td,
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
      -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
              box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
    background-color:rgba(92, 112, 128, 0.3);
    cursor:pointer; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
    background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  padding-bottom:0;
  top:40px; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-left:0;
  margin-right:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  font-family:"Icons20";
  font-size:inherit;
  font-style:normal;
  font-weight:400;
  line-height:1; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagnosis::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-lab-test::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }
  .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{ }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  background:#ffffff;
  border-radius:3px;
  color:#182026;
  list-style:none;
  margin:0;
  min-width:180px;
  padding:5px;
  text-align:left; }

.bp3-menu-divider{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px; }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  color:inherit;
  line-height:20px;
  padding:5px 7px;
  text-decoration:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    color:#5c7080;
    margin-top:2px; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit !important;
    color:rgba(92, 112, 128, 0.6) !important;
    cursor:not-allowed !important;
    outline:none !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    font-size:16px;
    line-height:22px;
    padding:9px 7px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-right:10px;
      margin-top:1px; }

button.bp3-menu-item{
  background:none;
  border:none;
  text-align:left;
  width:100%; }
.bp3-menu-header{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px;
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    line-height:17px;
    margin:0;
    padding:10px 7px 0 1px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    font-size:18px;
    padding-bottom:5px;
    padding-top:15px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item{ }
  .bp3-dark .bp3-menu-item.bp3-intent-primary{
    color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-success{
    color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning{
    color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger{
    color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item::before,
  .bp3-dark .bp3-menu-item > .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item .bp3-menu-item-label{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
    background-color:rgba(138, 155, 168, 0.3); }
  .bp3-dark .bp3-menu-item.bp3-disabled{
    color:rgba(167, 182, 194, 0.6) !important; }
    .bp3-dark .bp3-menu-item.bp3-disabled::before,
    .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  background-color:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  height:50px;
  padding:0 15px;
  position:relative;
  width:100%;
  z-index:10; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    left:0;
    position:fixed;
    right:0;
    top:0; }

.bp3-navbar-heading{
  font-size:16px;
  margin-right:15px; }

.bp3-navbar-group{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px;
  margin:0 10px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:100%;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  text-align:center;
  width:100%; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  bottom:0;
  left:0;
  position:static;
  right:0;
  top:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    overflow:hidden;
    position:fixed; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    overflow:auto;
    position:fixed; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  bottom:0;
  left:0;
  position:fixed;
  right:0;
  top:0;
  opacity:1;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  z-index:20; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }
  .bp3-panel-stack-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-panel-stack2{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack2-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack2-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack2-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack2-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack2-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack2-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-view{
    background-color:#30404d; }
  .bp3-panel-stack2-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter, .bp3-panel-stack2-push .bp3-panel-stack2-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter-active, .bp3-panel-stack2-push .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter, .bp3-panel-stack2-pop .bp3-panel-stack2-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter-active, .bp3-panel-stack2-pop .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  border-radius:3px;
  display:inline-block;
  z-index:20; }
  .bp3-popover .bp3-popover-arrow{
    height:30px;
    position:absolute;
    width:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      height:20px;
      margin:5px;
      width:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-bottom:17px;
    margin-top:-17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-left:-17px;
    margin-right:17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover .bp3-popover-content{
    border-radius:3px;
    position:relative; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  border-radius:2px;
  content:"";
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg); }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  left:0;
  position:absolute;
  right:0;
  top:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  background:rgba(92, 112, 128, 0.2);
  border-radius:40px;
  display:block;
  height:8px;
  overflow:hidden;
  position:relative;
  width:100%; }
  .bp3-progress-bar .bp3-progress-meter{
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    border-radius:40px;
    height:100%;
    position:absolute;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:100%; }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  color:transparent !important;
  cursor:default;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  height:40px;
  min-width:150px;
  width:100%;
  cursor:default;
  outline:none;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    cursor:not-allowed;
    opacity:0.5; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  height:6px;
  left:0;
  right:0;
  top:5px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  height:16px;
  left:0;
  position:absolute;
  top:0;
  width:16px; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab;
    z-index:2; }
  .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    background:#bfccd6;
    -webkit-box-shadow:none;
            box-shadow:none;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    background:#5c7080;
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-slider-handle .bp3-slider-label{
    background:#394b59;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    color:#f5f8fa;
    margin-left:8px; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      background:#e1e8ed;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-bottom-right-radius:0;
    border-top-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    border-bottom-left-radius:0;
    border-top-left-radius:0;
    margin-left:8px; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  font-size:12px;
  line-height:1;
  padding:2px 5px;
  position:absolute;
  vertical-align:top; }

.bp3-slider.bp3-vertical{
  height:150px;
  min-width:40px;
  width:40px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    bottom:0;
    height:auto;
    left:5px;
    top:0;
    width:6px; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-left:0;
      margin-top:-8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      height:8px;
      margin-left:0;
      width:16px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-bottom-right-radius:3px;
      border-top-left-radius:0; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      border-bottom-left-radius:0;
      border-bottom-right-radius:0;
      border-top-left-radius:3px;
      margin-bottom:8px; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round;
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      padding:0 10px;
      width:100%; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        background-color:rgba(19, 124, 189, 0.2);
        -webkit-box-shadow:none;
                box-shadow:none; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      background-color:rgba(19, 124, 189, 0.2);
      border-radius:3px;
      bottom:0;
      height:auto;
      left:0;
      right:0;
      top:0; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  border:none;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  list-style:none;
  margin:0;
  padding:0;
  position:relative; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:#182026;
  cursor:pointer;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  font-size:14px;
  line-height:30px;
  max-width:100%;
  position:relative;
  vertical-align:top; }
  .bp3-tab a{
    color:inherit;
    display:block;
    text-decoration:none; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    background-color:transparent !important;
    -webkit-box-shadow:none !important;
            box-shadow:none !important; }
  .bp3-tab[aria-disabled="true"]{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    font-size:16px;
    line-height:40px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  left:0;
  pointer-events:none;
  position:absolute;
  top:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    background-color:#106ba3;
    bottom:0;
    height:3px;
    left:0;
    position:absolute;
    right:0; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#5c7080;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  color:#f5f8fa;
  font-size:12px;
  line-height:16px;
  max-width:100%;
  min-height:20px;
  min-width:20px;
  padding:2px 6px;
  position:relative; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-left:8px;
    padding-right:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    font-size:14px;
    line-height:20px;
    min-height:30px;
    min-width:30px;
    padding:5px 10px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-left:12px;
      padding-right:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  background:none;
  border:none;
  color:inherit;
  cursor:pointer;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin-bottom:-2px;
  margin-right:-6px !important;
  margin-top:-2px;
  opacity:0.5;
  padding:2px;
  padding-left:0; }
  .bp3-tag-remove:hover{
    background:none;
    opacity:0.8;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:0 5px 0 0; }
    .bp3-large .bp3-tag-remove:empty::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  line-height:inherit;
  min-height:30px;
  padding-left:5px;
  padding-right:0; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    color:#5c7080;
    margin-left:2px;
    margin-right:7px;
    margin-top:7px; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    margin-right:7px;
    margin-top:5px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:20px;
    width:80px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-left:5px;
      margin-top:10px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-height:30px;
      min-width:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:20px 0 0;
  max-width:500px;
  min-width:300px;
  pointer-events:all;
  position:relative !important; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-delay:50ms;
            transition-delay:50ms;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    color:#5c7080;
    margin:12px;
    margin-right:0; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    background-color:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  left:0;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none;
  right:0;
  z-index:40; }
  .bp3-toast-container.bp3-toast-container-in-portal{
    position:fixed; }
  .bp3-toast-container.bp3-toast-container-inline{
    position:absolute; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0; }
  .bp3-toast-container.bp3-toast-container-bottom{
    bottom:0;
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-exit-active ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    height:22px;
    position:absolute;
    width:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      height:14px;
      margin:4px;
      width:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-bottom:11px;
    margin-top:-11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-left:-11px;
    margin-right:11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  list-style:none;
  margin:0;
  padding-left:0; }

.bp3-tree-root{
  background-color:transparent;
  cursor:default;
  padding-left:0;
  position:relative; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:30px;
  padding-right:5px;
  width:100%; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  cursor:pointer;
  padding:7px;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  margin-right:7px;
  position:relative; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  left:calc(50% - 250px);
  top:20vh;
  width:500px;
  z-index:21; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar .bp3-input{
    background-color:transparent;
    border-radius:0; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    background-color:transparent;
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MC45NzggNTAuOTc4IiBzdHlsZT0iZW5hYmxlLWJhY2tncm91bmQ6bmV3IDAgMCA1MC45NzggNTAuOTc4OyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+Cgk8Zz4KCQk8cGF0aCBzdHlsZT0iZmlsbDojMDEwMDAyOyIgZD0iTTQzLjUyLDcuNDU4QzM4LjcxMSwyLjY0OCwzMi4zMDcsMCwyNS40ODksMEMxOC42NywwLDEyLjI2NiwyLjY0OCw3LjQ1OCw3LjQ1OAoJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDAKCQkJYzYuODE2LDAsMTMuMjIxLTIuNjQ4LDE4LjAyOS03LjQ1OGM0LjgwOS00LjgwOSw3LjQ1Ny0xMS4yMTIsNy40NTctMTguMDNDNTAuOTc3LDE4LjY3LDQ4LjMyOCwxMi4yNjYsNDMuNTIsNy40NTh6CgkJCSBNNDIuMTA2LDQyLjEwNWMtNC40MzIsNC40MzEtMTAuMzMyLDYuODcyLTE2LjYxNSw2Ljg3MmgtMC4wMDJjLTYuMjg1LTAuMDAxLTEyLjE4Ny0yLjQ0MS0xNi42MTctNi44NzIKCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzIKCQkJYzQuNDMxLDQuNDMxLDYuODcxLDEwLjMzMiw2Ljg3MSwxNi42MTdDNDguOTc3LDMxLjc3Miw0Ni41MzYsMzcuNjc1LDQyLjEwNiw0Mi4xMDV6Ii8+CgkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik0yMy41NzgsMzIuMjE4Yy0wLjAyMy0xLjczNCwwLjE0My0zLjA1OSwwLjQ5Ni0zLjk3MmMwLjM1My0wLjkxMywxLjExLTEuOTk3LDIuMjcyLTMuMjUzCgkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUKCQkJYzAtMS4wOTYtMC4yNi0yLjA4OC0wLjc3OS0yLjk3OWMtMC41NjUtMC44NzktMS41MDEtMS4zMzYtMi44MDYtMS4zNjljLTEuODAyLDAuMDU3LTIuOTg1LDAuNjY3LTMuNTUsMS44MzIKCQkJYy0wLjMwMSwwLjUzNS0wLjUwMywxLjE0MS0wLjYwNywxLjgxNGMtMC4xMzksMC43MDctMC4yMDcsMS40MzItMC4yMDcsMi4xNzRoLTIuOTM3Yy0wLjA5MS0yLjIwOCwwLjQwNy00LjExNCwxLjQ5My01LjcxOQoJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQoJCQljMCwxLjE0Mi0wLjEzNywyLjExMS0wLjQxLDIuOTExYy0wLjMwOSwwLjg0NS0wLjczMSwxLjU5My0xLjI2OCwyLjI0M2MtMC40OTIsMC42NS0xLjA2OCwxLjMxOC0xLjczLDIuMDAyCgkJCWMtMC42NSwwLjY5Ny0xLjMxMywxLjQ3OS0xLjk4NywyLjM0NmMtMC4yMzksMC4zNzctMC40MjksMC43NzctMC41NjUsMS4xOTljLTAuMTYsMC45NTktMC4yMTcsMS45NTEtMC4xNzEsMi45NzkKCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}
.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}
.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}
.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-border-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0px;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-warn-color0);
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px 5px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FileDialog-Checkbox {
  margin-top: 35px;
  display: flex;
  flex-direction: row;
  align-items: end;
  width: 100%;
}

.jp-FileDialog-Checkbox > label {
  flex: 1 1 auto;
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
  overflow-x: auto;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 50px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -50px; margin-right: -50px;
  padding-bottom: 50px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 50px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
  outline: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -50px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: #1a1a1a;
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .remote-caret {
  position: relative;
  border-left: 2px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .remote-caret > div {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -2px;
  font-size: 0.95em;
  background-color: rgb(250, 129, 0);
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 3;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .remote-caret.hide-name > div {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .remote-caret:hover > div {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
  margin: 8px 12px 0px 12px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: flex-start;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0px;
  padding-right: 2px;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 40px;
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent {
  width: 72px;
  background: var(--jp-brand-color1);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent:focus-visible {
  background-color: var(--jp-brand-color0);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent
  .jp-icon3 {
  fill: white;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileBrowser-filterBox {
  padding: 0px;
  flex: 0 0 auto;
  margin: 8px 12px 0px 12px;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing:focus-visible {
  border: 1px solid var(--jp-brand-color1);
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon:before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

body[data-format='mobile'] .jp-OutputArea-child {
  flex-direction: column;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-OutputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  margin-left: var(--jp-notebook-padding);
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 10px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
  background: whitesmoke;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
  overflow: hidden;
}

body[data-format='mobile'] .jp-InputArea {
  flex-direction: column;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
  overflow: hidden;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border-radius: 7px;
}

body[data-format='mobile'] .jp-InputArea-editor {
  margin-left: var(--jp-notebook-padding);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-InputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

.jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
}

.jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-collapseHeadingButton {
  display: none;
}

.jp-MarkdownCell:hover .jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  position: absolute;
  right: 0;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook-render * {
  contain: none !important;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
  float: left;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt:before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body div {
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #FF69B4; /* Hot Pink */
  --jp-mirror-editor-atom-color: #7FFF00; /* Chartreuse */
  --jp-mirror-editor-number-color: #FFD700; /* Gold */
  --jp-mirror-editor-def-color: #FF4500; /* Orange Red */
  --jp-mirror-editor-variable-color: #EE82EE; /* Violet */
  --jp-mirror-editor-variable-2-color: #ADFF2F; /* Green Yellow */
  --jp-mirror-editor-variable-3-color: #FF8C00; /* Dark Orange */
  --jp-mirror-editor-punctuation-color: #F8F8FF; /* Ghost White */
  --jp-mirror-editor-property-color: #FFA07A; /* Light Salmon */
  --jp-mirror-editor-operator-color: #98FB98; /* Pale Green */
  --jp-mirror-editor-comment-color: #5AC8FA; /* Light Gray */
  --jp-mirror-editor-string-color: #FF6347; /* Tomato */
  --jp-mirror-editor-string-2-color: #40E0D0; /* Turquoise */
  --jp-mirror-editor-meta-color: #9ACD32; /* Yellow Green */
  --jp-mirror-editor-qualifier-color: #FA8072; /* Salmon */
  --jp-mirror-editor-builtin-color: #E9967A; /* Dark Salmon */
  --jp-mirror-editor-bracket-color: #F0E68C; /* Khaki */
  --jp-mirror-editor-tag-color: #F5DEB3; /* Wheat */
  --jp-mirror-editor-attribute-color: #D2B48C; /* Tan */
  --jp-mirror-editor-header-color: #FFA500; /* Orange */
  --jp-mirror-editor-quote-color: #DDA0DD; /* Plum */
  --jp-mirror-editor-link-color: #FFDEAD; /* Navajo White */
  --jp-mirror-editor-error-color: #DC143C; /* Crimson */
  --jp-mirror-editor-hr-color: #F5F5DC; /* Beige */

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

.highlight  {
  margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.CodeMirror pre {
  margin: 0;
  padding: 0;
}

/* Using table instead of flexbox so that we can use break-inside property */
/* CSS rules under this comment should not be required anymore after we move to the JupyterLab 4.0 CSS */


.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  min-width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-OutputArea-child {
  display: table;
  width: 100%;
}

.jp-OutputPrompt {
  display: table-cell;
  vertical-align: top;
  min-width: var(--jp-cell-prompt-width);
}

body[data-format='mobile'] .jp-OutputPrompt {
  display: table-row;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  display: table-row;
}

.jp-OutputArea-output.jp-OutputArea-executeResult {
  width: 100%;
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }

  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}
</style>

<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: {
                    automatic: true
                    }
                }
            });

            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8">&#47532;&#49828;&#53944;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8">&#182;</a></h2>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data:image/png;base64,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" alt="image.png"></p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>리스트, 튜플 == 순서를 가지고 있음</p>
<ol>
<li>인덱싱</li>
<li>슬라이싱</li>
</ol>
<p>리스트 ( 수정 o )
튜플 ( 수정 x)</p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data:image/png;base64,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" alt="image-2.png"></p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>a = [1, 2, 3]</p>
<p>b = ["1", 1, 3]</p>
<p>여러개의 데이터 타입 사용 가능</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[4]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">type</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[6]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>list</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">20</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[10]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[10, 12, 14, 16, 18]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">list</span><span class="p">(</span><span class="nb">reversed</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[9]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[9, 8, 7, 6, 5, 4, 3, 2, 1, 0]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="for-%EB%B3%80%EC%88%98-in-%EB%A6%AC%EC%8A%A4%ED%8A%B8:">for &#48320;&#49688; in &#47532;&#49828;&#53944;:<a class="anchor-link" href="#for-%EB%B3%80%EC%88%98-in-%EB%A6%AC%EC%8A%A4%ED%8A%B8:">&#182;</a></h4>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># for로 리스트 전부 출력</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">a</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>1
2
3
4
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[15]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">9</span><span class="p">,</span> <span class="mi">10</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">1</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>1
2
3
4
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">9</span><span class="p">,</span> <span class="mi">10</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">1</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">i</span><span class="p">,</span> <span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>0 1
1 2
2 3
3 4
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="for-%EC%9D%B8%EB%8D%B1%EC%8A%A4,-%EC%9A%94%EC%86%8C-in-enumerate(%EB%A6%AC%EC%8A%A4%ED%8A%B8):">for &#51064;&#45937;&#49828;, &#50836;&#49548; in enumerate(&#47532;&#49828;&#53944;):<a class="anchor-link" href="#for-%EC%9D%B8%EB%8D%B1%EC%8A%A4,-%EC%9A%94%EC%86%8C-in-enumerate(%EB%A6%AC%EC%8A%A4%ED%8A%B8):">&#182;</a></h4><h4 id="for-%EC%9D%B8%EB%8D%B1%EC%8A%A4,-%EC%9A%94%EC%86%8C-in-enumerate(%EB%A6%AC%EC%8A%A4%ED%8A%B8,-start=%EC%88%AB%EC%9E%90):---%23%EC%B4%88%EA%B8%B0-%EC%8B%9C%EC%9E%91%EA%B0%92-%EC%A7%80%EC%A0%95">for &#51064;&#45937;&#49828;, &#50836;&#49548; in enumerate(&#47532;&#49828;&#53944;, start=&#49707;&#51088;):   #&#52488;&#44592; &#49884;&#51089;&#44050; &#51648;&#51221;<a class="anchor-link" href="#for-%EC%9D%B8%EB%8D%B1%EC%8A%A4,-%EC%9A%94%EC%86%8C-in-enumerate(%EB%A6%AC%EC%8A%A4%ED%8A%B8,-start=%EC%88%AB%EC%9E%90):---%23%EC%B4%88%EA%B8%B0-%EC%8B%9C%EC%9E%91%EA%B0%92-%EC%A7%80%EC%A0%95">&#182;</a></h4>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[21]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="k">for</span> <span class="n">index</span><span class="p">,</span> <span class="n">value</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">a</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">index</span><span class="p">,</span> <span class="n">value</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>0 1
1 2
2 3
3 4
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[13]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="k">for</span> <span class="n">index</span><span class="p">,</span> <span class="n">value</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">a</span><span class="p">,</span> <span class="n">start</span><span class="o">=</span><span class="mi">1</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">index</span><span class="p">,</span> <span class="n">value</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>1 1
2 2
3 3
4 4
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%ED%95%A9-%EA%B5%AC%ED%95%98%EA%B8%B0">&#47532;&#49828;&#53944; &#54633; &#44396;&#54616;&#44592;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%ED%95%A9-%EA%B5%AC%ED%95%98%EA%B8%B0">&#182;</a></h4>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[29]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="n">hap</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">a</span><span class="p">:</span>
    <span class="n">hap</span> <span class="o">=</span> <span class="n">hap</span> <span class="o">+</span> <span class="n">i</span>
    
<span class="nb">print</span><span class="p">(</span><span class="n">hap</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>10
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="n">hap</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">1</span><span class="p">):</span>
    <span class="n">hap</span> <span class="o">=</span> <span class="n">hap</span> <span class="o">+</span> <span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">hap</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>10
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[35]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 리스트 초기화</span>
<span class="n">c</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">hap</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>
    <span class="n">a</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>

<span class="c1"># 리스트 자료 입력 받기</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>
    <span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span><span class="o">+</span><span class="s2">"번째 숫자 입력:"</span><span class="p">))</span>
    
<span class="c1"># 리스트의 합 구하기</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">4</span><span class="p">):</span>
    <span class="n">hap</span> <span class="o">=</span> <span class="n">hap</span> <span class="o">+</span> <span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">]</span>
    
<span class="c1"># 리스트 합 출력</span>
<span class="nb">print</span><span class="p">(</span><span class="n">hap</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>1번째 숫자 입력:1
2번째 숫자 입력:2
3번째 숫자 입력:3
4번째 숫자 입력:4
10
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%9D%B5%EB%8D%B1%EC%8B%B1,-%EC%8A%AC%EB%9D%BC%EC%9D%B4%EC%8B%B1">&#47532;&#49828;&#53944; &#51061;&#45937;&#49905;, &#49836;&#46972;&#51060;&#49905;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%9D%B5%EB%8D%B1%EC%8B%B1,-%EC%8A%AC%EB%9D%BC%EC%9D%B4%EC%8B%B1">&#182;</a></h4>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[38]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">[</span><span class="o">-</span><span class="mi">1</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="mi">2</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">[</span><span class="mi">2</span><span class="p">:</span><span class="mi">2</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>1
4
[1, 2]
[]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[49]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">list</span><span class="p">(</span><span class="nb">reversed</span><span class="p">(</span><span class="n">a</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[49]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[4, 3, 2, 1]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[39]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">len</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>  <span class="c1">#요소 갯수</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[39]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>4</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[41]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="nb">len</span><span class="p">(</span><span class="n">a</span><span class="p">)]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[41]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 2, 3, 4]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EA%B0%92-%EB%B3%80%EA%B2%BD">&#47532;&#49828;&#53944; &#44050; &#48320;&#44221;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EA%B0%92-%EB%B3%80%EA%B2%BD">&#182;</a></h3>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[51]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">aaa</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">aaa</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="mi">0</span>

<span class="n">aaa</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[51]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 0, 3, 4]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[73]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">bbb</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">bbb</span><span class="p">[</span><span class="mi">1</span><span class="p">:</span><span class="mi">3</span><span class="p">]</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span> <span class="p">,</span> <span class="mi">0</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">bbb</span><span class="p">)</span>

<span class="n">bbb</span><span class="p">[</span><span class="mi">1</span><span class="p">:</span><span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="p">[</span><span class="mi">3</span> <span class="p">,</span> <span class="mi">3</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">bbb</span><span class="p">)</span>

<span class="n">bbb</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="p">[</span><span class="s2">"A"</span> <span class="p">,</span> <span class="s2">"A"</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">bbb</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 0, 0, 4]
[1, 3, 3, 0, 4]
[1, [&#39;A&#39;, &#39;A&#39;], 3, 0, 4]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[79]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 리스트 삭제</span>

<span class="n">aaa</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">aaa</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="p">[</span><span class="s2">"a"</span><span class="p">,</span> <span class="s2">"b"</span><span class="p">]</span>        <span class="c1">#2차원 리스트</span>

<span class="nb">print</span><span class="p">(</span><span class="n">aaa</span><span class="p">)</span>

<span class="k">del</span><span class="p">(</span><span class="n">aaa</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">aaa</span><span class="p">)</span>

<span class="k">del</span><span class="p">(</span><span class="n">aaa</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="mi">2</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">aaa</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, [&#39;a&#39;, &#39;b&#39;], 3, 4]
[[&#39;a&#39;, &#39;b&#39;], 3, 4]
[4]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[78]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 또다른 삭제 방법</span>

<span class="n">ccc</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">ccc</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]</span>    <span class="c1">#일케 하면 []가 들어감 xxx</span>

<span class="nb">print</span><span class="p">(</span><span class="n">ccc</span><span class="p">)</span>

<span class="n">ccc</span><span class="p">[</span><span class="mi">1</span><span class="p">:</span><span class="mi">2</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">ccc</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[78]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 3, 4]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%97%B0%EC%82%B0">&#47532;&#49828;&#53944; &#50672;&#49328;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%97%B0%EC%82%B0">&#182;</a></h3>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[80]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>
<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">]</span>

<span class="n">a</span> <span class="o">+</span> <span class="n">b</span>      <span class="c1"># 리스트 결합 시킴</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[80]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 5, 6]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[81]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>
<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">]</span>

<span class="n">a</span> <span class="o">*</span> <span class="n">b</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>
<span class="ansi-red-intense-fg ansi-bold">---------------------------------------------------------------------------</span>
<span class="ansi-red-intense-fg ansi-bold">TypeError</span>                                 Traceback (most recent call last)
Cell <span class="ansi-green-intense-fg ansi-bold">In[81], line 4</span>
<span class="ansi-green-fg">      1</span> a <span style="color: rgb(98,98,98)">=</span> [<span style="color: rgb(98,98,98)">1</span>, <span style="color: rgb(98,98,98)">2</span>, <span style="color: rgb(98,98,98)">3</span>]
<span class="ansi-green-fg">      2</span> b <span style="color: rgb(98,98,98)">=</span> [<span style="color: rgb(98,98,98)">4</span>, <span style="color: rgb(98,98,98)">5</span>, <span style="color: rgb(98,98,98)">6</span>]
<span class="ansi-green-intense-fg ansi-bold">----&gt; 4</span> <span class="ansi-yellow-bg">a</span><span class="ansi-yellow-bg"> </span><span class="ansi-yellow-bg" style="color: rgb(98,98,98)">*</span><span class="ansi-yellow-bg"> </span><span class="ansi-yellow-bg">b</span>

<span class="ansi-red-intense-fg ansi-bold">TypeError</span>: can&#39;t multiply sequence by non-int of type &#39;list&#39;</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[83]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>
<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">4</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="n">a</span> <span class="o">*</span> <span class="mi">2</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">b</span> <span class="o">*</span> <span class="mi">2</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 1, 2, 3]
[4, 5, 6, 4, 5, 6]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%A1%B0%EC%9E%91-%ED%95%A8%EC%88%98">&#47532;&#49828;&#53944; &#51312;&#51089; &#54632;&#49688;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%A1%B0%EC%9E%91-%ED%95%A8%EC%88%98">&#182;</a></h4>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># count</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">1</span><span class="p">]</span>

<span class="n">a</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="mi">1</span><span class="p">)</span>        <span class="c1">#이게 몇개 들어 있는지</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[2]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>2</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># index</span>

<span class="n">a</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="mi">1</span><span class="p">)</span>  <span class="c1"># 첫번쨰로 나오는거 어디 위치에 있는지</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[5]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[27]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># pop</span>

<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>

<span class="n">item</span> <span class="o">=</span> <span class="n">b</span><span class="o">.</span><span class="n">pop</span><span class="p">()</span>

<span class="nb">print</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="c1">#그냥 pop 주면 맨오른쪽꺼 빼감</span>

<span class="nb">print</span><span class="p">(</span><span class="n">b</span><span class="p">)</span> 
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>3
[1, 1, 2]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># append</span>

<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>

<span class="n">b</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mi">3</span><span class="p">)</span> 

<span class="n">b</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[28]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 1, 2, 3, 3]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[29]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># insert</span>

<span class="n">c</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">]</span>

<span class="n">c</span><span class="o">.</span><span class="n">insert</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">9</span><span class="p">)</span>

<span class="n">c</span>          <span class="c1">## insert == 특정 자리에 넣는거 </span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[29]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[9, 0, 1, 2, 3]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[32]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># remove</span>

<span class="n">d</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">9</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span> <span class="mi">0</span><span class="p">]</span>

<span class="n">d</span><span class="o">.</span><span class="n">remove</span><span class="p">(</span><span class="mi">0</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">d</span><span class="p">)</span>

<span class="n">d</span><span class="o">.</span><span class="n">remove</span><span class="p">(</span><span class="mi">4</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">d</span><span class="p">)</span>      <span class="c1">#자리를 삭제하는게 아니라 해당 값을 삭제하는거임</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 9, 4, 0]
[1, 9, 0]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>sort() vs sorted()</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[35]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 오름차순</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">a</span><span class="o">.</span><span class="n">sort</span><span class="p">()</span>

<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>

<span class="c1"># 내림차순</span>

<span class="n">a</span><span class="o">.</span><span class="n">sort</span><span class="p">(</span><span class="n">reverse</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 6, 8]
[8, 6, 4, 3, 2, 1]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[42]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#sorted() 오름차순</span>

<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="nb">sorted</span><span class="p">(</span><span class="n">b</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 6, 8]
[2, 3, 8, 6, 1, 4]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[47]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#sorted() 내림차순</span>

<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">8</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">1</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="nb">sorted</span><span class="p">(</span><span class="n">b</span><span class="p">,</span> <span class="n">reverse</span><span class="o">=</span><span class="kc">True</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[8, 6, 4, 3, 2, 1]
[2, 3, 8, 6, 1, 4]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>sort는 원본 영향 o</p>
<p>sorted는 원본 영향 x</p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>리스트 복사</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[48]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="n">b</span> <span class="o">=</span> <span class="n">a</span>

<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 4]
[1, 2, 3, 4]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[49]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># soft copy </span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">b</span> <span class="o">=</span> <span class="n">a</span>

<span class="n">a</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mi">9</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 9]
[1, 2, 3, 4, 9]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data:image/png;base64,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" alt="image-2.png"></p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[50]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">id</span><span class="p">(</span><span class="n">a</span><span class="p">)</span> <span class="p">,</span> <span class="nb">id</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>     <span class="c1">#아이디 같은거 보이지 ?</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[50]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(2837712002432, 2837712002432)</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[51]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># hard cpopy</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="n">b</span> <span class="o">=</span>  <span class="n">a</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

<span class="n">a</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mi">8</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 8]
[1, 2, 3, 4]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[52]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">id</span><span class="p">(</span><span class="n">a</span><span class="p">),</span> <span class="nb">id</span><span class="p">(</span><span class="n">b</span><span class="p">)</span>       <span class="c1">#id다른거 보이지 ?</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[52]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(2837712521344, 2837712562752)</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>append() vs extend()</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[57]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># append </span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>

<span class="n">a</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="mi">9</span><span class="p">)</span>

<span class="n">a</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[57]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 9]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[58]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># extend</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">]</span>
<span class="n">b</span> <span class="o">=</span> <span class="p">[</span><span class="mi">5</span><span class="p">,</span> <span class="mi">6</span><span class="p">,</span> <span class="mi">7</span><span class="p">,</span> <span class="mi">8</span><span class="p">]</span>

<span class="n">a</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span><span class="n">b</span><span class="p">)</span> <span class="c1">#리스트 끼리 결함</span>

<span class="n">a</span>       
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[58]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 2, 3, 4, 5, 6, 7, 8]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%97%B0%EC%8A%B5">&#47532;&#49828;&#53944; &#50672;&#49845;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%97%B0%EC%8A%B5">&#182;</a></h4>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[60]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span> <span class="p">[</span><span class="s2">"쭈쭈바"</span><span class="p">,</span> <span class="s2">"돼지바"</span><span class="p">,</span> <span class="s2">"쌍쌍바"</span><span class="p">]</span>
<span class="n">price</span> <span class="o">=</span> <span class="p">[</span><span class="mi">10</span> <span class="p">,</span> <span class="mi">20</span><span class="p">,</span> <span class="mi">30</span><span class="p">]</span>


<span class="c1"># 쭈쭈바의 가격은 ? (간단하게)</span>

<span class="n">jj_price</span> <span class="o">=</span> <span class="n">price</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"</span><span class="si">{}</span><span class="s2">원"</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">jj_price</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>10원
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[61]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span> <span class="p">[</span><span class="s2">"쭈쭈바"</span><span class="p">,</span> <span class="s2">"돼지바"</span><span class="p">,</span> <span class="s2">"쌍쌍바"</span><span class="p">]</span>
<span class="n">price</span> <span class="o">=</span> <span class="p">[</span><span class="mi">10</span> <span class="p">,</span> <span class="mi">20</span><span class="p">,</span> <span class="mi">30</span><span class="p">]</span>


<span class="c1"># 쭈쭈바의 가격은 ? (index 활용)</span>

<span class="n">jj_price_index</span> <span class="o">=</span> <span class="n">menu</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s2">"쭈쭈바"</span><span class="p">)</span>

<span class="n">jj_price</span> <span class="o">=</span> <span class="n">price</span><span class="p">[</span><span class="n">jj_price_index</span><span class="p">]</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"</span><span class="si">{}</span><span class="s2">원"</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">jj_price</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>10원
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h4 id="%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%BB%A8%ED%94%84%EB%A6%AC%ED%97%A8%EC%85%98">&#47532;&#49828;&#53944; &#52968;&#54532;&#47532;&#54760;&#49496;<a class="anchor-link" href="#%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EC%BB%A8%ED%94%84%EB%A6%AC%ED%97%A8%EC%85%98">&#182;</a></h4>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ol>
<li>[식 for 변수 in 리스트]  </li>
</ol>
<ol>
<li>list(식 for 변수 in 리스트)</li>
</ol>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[63]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 0부터 9까지 리스트 생성</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>

<span class="n">a</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[63]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjIAAACvCAYAAADnqzTtAAAgAElEQVR4nO3deXxM5/4H8M9kkQ2JtRVVpJZQUpQiVY1QFcSWcMUeXLdVv6Jaa1suQi0/vSlaS1UlthC0toRagjb2fblEqBCxK7LJNvP7I785nTNL5sxk9nzer9e8nHPmnPM8J5I533me7/McmUKhUICIiIjIDjlZuwJERERExmIgQ0RERHaLgQwRERHZLQYyREREZLcYyBAREZHdYiBDREREdsslPj7e2nUgIiIiMoqM88gQERGRvWLXEhEREdktBjJERERktxjIEBERkd1iIENERER2i4EMERER2S0GMkRERGS3XKxdASq9ly9fIj09HXl5eZDJZMjPz7d2lYiIiCyCgYwDSE9PR8WKFVGxYkVrV0WvjIwM+Pr6WrsaRETkINi15ADy8vLsIoghIiIyNQYyDkAmk1m7CkRERFbBQMYBMCeGiIjKKgYyREREZLcYyBAREZHdYiBDREREdouBDBEREdktBjJERERkt8r8hHjNg34Wls8mDXOYsoiIiMoCtsigOKiwRGBhqXKodDxmzjTLvpY4jymYsi6WvC5b+hlagur1Sr12ffuVtZ8hOQabbZFpHvSzzdz0pbSklKXWlpiYGAwZMsRi5XnMnIncr7/WWDbmPEq6zmHI+Uvat6QbgvoxpbkmbWVpO7/6+7qOMfaatJVtqv8rfeUYU5axdTPkRl+a/1PV8rSdx5i/CX37lfb3kMhabDaQsRXqAZW2AEvKPmRd6h/Spb1hG1KWOWm7LnXa3td3jDamDsAMKUu9XGvgjZ7INjGQKYG2gORs0jDRdin7mKJcWxATE2PxMk3RGmPocYa0yFgTb6zGsfb/m1Sm/P/l7wo5MrsLZJQ3edWuHMCy3Tm2GGRYgrI7yRoBjSWYolvJkl0chh6n7RhjA0VrdVPouwYpxxtbriHHmzMAMfT/TLmP6r/mrDORpdldIANI696xFHOUWVYDJSX1D1r1pEZLBArkeFS71YwJaCz5e6Qv6DAkuVdZb9VgxtjzEdkiuwxkLH2jNzSR11a7huyFtm+blgpITPGNu6RvvOa8YVjqZmTucgxJlDb0nFJu6tYmJZ9L9e9C6nmUx9nqdRMZyy4DGUuSmshblkYtWYIpbpaGdv+U9sNdyg3CVKN6tJWtfn59dVMPFE1Vp9KOVjJli1tJPxfVwNJWRvOol6Ue/EoJ7qVcU0llEtkbBjJ6SE3k5agl07N0a4y9UR9OXtrgT+oQXqn7WpPUeqoHcqYYyVaaYd2m+LkaEkwTOQIGMmZQ2lFLZZUpc2NKKkPfPCtSWfOGYEjCa2kTZKWe05YYWreS9rfEdUotX9eyucomsgcMZErJHAFLWQ2CTJkbY8hx1hh9ZMmcH31BjDETqpWUhGor3Ur2Sl9gbaoRWo74s6OyiYEM2RRz3pzs/canq/vBkFyg0gw/tvbPzl66tYwl9fpKkxdkyHmI7AUDmRJo6yJSX5eyjzHlUumoj86w5oe2ei6Lqc+tK1iRul3f+XUdY4mfqTl/drZIyjVKGXlkqvMQ2QMGMnqoT76nLciQsg/pZ2yXh75zAobfvEuTsKnOVPkpyhuPvpu7IUGHobk12upiymBR/WdoaN1Mle9kq3lTpmqVcvTWLSpbZAqFQmHtSliTNfJRTF3muXPn4O/vb7LzmVNGRgZ8fX2tXY0Smftbqi19Czb1EHBrDVN2FMyPITIcAxkLtqSYqywGMkREVFaV+a4lPqOJiIjIfjlZuwJERERExmIgQ0RERHaLgQwRERHZLQYyREREZLcYyBAREZHdKvOjlsgwMTExwvKQIUOsWJOy66+//sL27dvRokUL+Pv7w9XV1dpVIiKyGgYyJFlMTIwoeFFfJ/O4desWdu3ahVOnTuHUqVNITU0V3nNyckK9evXQsGFDNGjQAK1bt0bnzp3h5uZmxRoTEVlOmZ8QzxFYYkI8XUGLocEMJ8ST5vHjx4iPj8fGjRtx/Phxg4718fFB3759ERERgTZt2kAmk5mplkRE1scWGSITkMvlSExMBAB06dIFTk6Gp59lZ2djx44diIuLw2+//YaioiKj6vLs2TOsXLkSK1euRJ06dRAREYGIiAjUr1/fqPMREdkytsg4AGs+ooAtMsV2796NsLAwAMDWrVsREhIi6biCggLs378fGzduxI4dO5CTk6Oxj4uLC1q1aoUePXogMDAQAQEBcHd3B1Ac/Ny4cQMpKSnYvn07jh07hjt37mgtq2XLlhgwYAD69u2LqlWrGnmlRES2hS0yZDTmyPztzJkzwvLp06dLDGQUCgWOHz+OjRs3Ij4+Hk+ePNG6X5s2bdC/f3+EhYXpDDy8vLwQEBCAgIAAhIeHQy6XIzk5GRs2bMCWLVvw/PlzYV9ljs3EiRMRHh6OcePG4a233jLqeqW0QKWmpuLu3btQKBR6X8qfi7bX8ePH0b17d7Ro0YK5P0SkgYEMGYVBjHEuXLiACRMm4Pfff9f6fqNGjdC/f3/069cPderUMfj8Tk5OaNeuHdq1a4f//d//xZ49e7B+/XokJCSgoKAAAFBYWIiNGzdi48aN6NChA8aPH49OnToZlEuTmJioswUqIyMDX3/9NdatW2dw/XVZtGgRnJyc0LhxYwQEBODtt99GaGgoatWqZbIyiMg+cR4ZMkhMTAyDGCM8ffoUY8eORdu2bTWCGF9fX4wbNw7Hjx/H6dOnMXHiRKOCGHXu7u7o2bMn4uLikJaWhiVLlmh0QR48eBA9evRAq1atsH79esjlcknnVm+BAoq7uaKiotC0aVOTBjFKcrkcly5dwvr16zFhwgQ0aNAA7du3R3R0NG7fvm3y8ojIPrBFhiRjAGO4wsJCrFq1CjNmzMCzZ89E7wUFBWHKlClo166dUcnBhqhUqRJGjBiBESNG4OzZs/j222+xdetWIaH48uXLGDFiBFatWoUffvgBDRo0MOj89+7dQ5cuXZCSkqLxXvv27SGTyfS+AGhsS01NxbVr13SWe/LkSZw8eRKTJ09Gy5YtMWTIEAwYMABeXl4G1Z+I7BcDGZKEQYzhjhw5ggkTJuDixYui7cHBwVi4cCEaNWpklXo1b94cMTExmDVrFpYsWYLVq1cjOzsbAJCcnIx33nkH06dPx/jx4yWdLysrCx9++CGuX78ubAsICMCCBQvQvn17k9U7MzMTly9fxr59+3DixAkcPHgQhYWFwvvKHKCvvvoKI0aMwEcffcSuJ6IygF1LRCb24sULDBo0CJ07dxYFMbVr18amTZuwc+dOqwUxqmrXro0FCxYgNTUVw4YNg7OzMwAgLy8PU6dOxY4dOySdZ926daIgZsyYMUhOTjZpEAMAFSpUQJs2bfDll19i+/btuH37NpYtW4bOnTvDxeXv72TPnz/HokWL0KhRIwwYMABHjx4FB2cSOS4GMkQmtmzZMmzZskVY9/T0xPTp03H27FmEhoba3AR1Pj4++OGHH5CcnCwaxfTixQtJxz9+/BgA4OzsjA0bNmDBggVCUGROlSpVwtChQ/Hrr78iLS0Nc+fOhZ+fn/B+UVERtm3bhuDgYLRr1w4bNmxAfn6+2etFRJbFriWSTPU5S6rY5SSmHB0EAH379sWcOXPw2muvWbFG0gQEBODIkSNYv349KleujNDQUMnHOjs7IyYmBr169TJjDXWrXLkyxo0bh//5n/9BQkICli5diqSkJOH9M2fOYPjw4ZgyZQr+9a9/YeTIkahWrZpV6kpEpsVAhiRhsGKY+vXrY+HChejcubO1q2IQV1dXDB061KBjypcvjxUrVqB3795mqpV0zs7O6N69O7p3746LFy/i+++/x4YNG5CXlwcAePDgAWbOnIl58+bhH//4Bz755BMEBARYudZEVBqc2dcBWHNmX0M56sy+e/fuRc+ePUXbXFxcIJPJ0KlTJ7i4uMDV1RXlypWDq6ur6KV8z9PTE3Xr1kXDhg3h7+8vzN5ri2bPno2oqCgAwJQpU/D1119buUa6PX78GKtWrcKyZctw//59jffbtm2LgQMHIiwsDD4+PlaoIRGVBgMZB8BAxvoUCgXGjx+P5cuXm+R8NWvWRHx8PJo1a2aS85maaiADAElJSahTpw4KCwuRlZWF7OxsZGVlISsrCzk5OcJycnIybt++jezsbGzduhV169a1WJ3z8/Oxbds2LF68WJj7RpWLiwvee+89REZGom/fvharFxGVDgMZB8BAxnYkJycjISEB+/btw7lz50p1rhkzZmDSpEkmqplp7dy5s9Q3+6FDh2LZsmUmqpF0CoUCJ06cwOLFi/HLL79ofTjnTz/9hIiICIvXjYgMxxwZIgPkfre0xPebA2he7VVMjRiExz164eLdDOQVFaKgqEh4yTq8j4KCAhQUFKCwsBAFBQXIz8/HzZs38ddffyElJQVeXl745z//aZmL0kLfdXZQKBDerDniz5016vze3t5Wa/WQyWRo3bo1WrdujfT0dKxduxbbt2/H2bN/Xwuf6URkP9gi4wDYImM5+m7wUnh8+okJamJeUq6zSC7HzksXsfrYUdz+6y9k5eXBzdUFnq7lUKHWa/Dy8hK9ypcvD29vb7Rs2RKBgYEWzUeRcj13nz3DnqtXUN7NDf2av22BWtkPe/idpbKLLTJEZBRnJyf0DHgLPQM0n6Btjze+mj4+GN4m0NrVICIDcUI8Igk8PDzg4eGBypM+t3ZVqIwy5++e1HMr/w48PDzMVhciQzGQIZIoNzcXT+cttHY1qAyqPOlzs/7uPZ23UFIwk5ubi9zcXLPVg8gYDGTIIDExMcKLNJniW3NGVgYa/NAAHvM80OCHBsjIyjBBzUzHlNdoi9dna6QEMZUPl/x/Uvnw58JLF6nBDJGtYY4MSab+BGw+Edv0MrIyEBQbBAC48ckN+Ja338Rosg2VD3+Op+0X6lwnsndskSFJtAUtQ4YMYcuMmrLQ9WSKa/Qt74uUj1OQ8nEKg7VS0NfKYii2ypA9YosM2RzVREJ76483dy6DkrLl5s6LOwCAWhVrIWlwkigoUO7zaatP8d3J74R9de0vlSmuUbXlyRL1rnzgczwNXojKB8Q36afBCzX2K+k9KefQdh7lsVLLEvbR87NWtqzoCma0tb48bb+QrTLkUBjIkCSW6kLy8PAQBS/q6/rkPZEheVg5ZN2U6dynvJ8CgT/nw62KbU2hpB6cvLH0jRIDFKC4+wkAgmKDEBQbpPUm/8X+L1CrYi2766pSr7fyunVdpz7agomS3tcVfOjbpm3dmLKISBoGMmQ0U+fIaAtacnNzDQpm3Koo0GFHnsnqZEm+5X2RNDhJZ0sFoLslQ3mctpt8aVpfrMnU9TYkiFHur75dX7BR0nkMLYuIpGEgQwZRzYkxdSuNvXUjkeNgAEFkvxjIkEEsMWqJk22RtWjrBrLncojKAgYyZDTlqCVzdy8ZEtjYc44MWZe+hFxTYgsQkekwkCFJLDFnjKGJvdrYc44MWQ/zU4jsF+eRISIyEW3Ds6W26mjbr7TzuiiHWovK4dBrcjAMZEgSbZPfmbqVRjlCSRXzZcSUI5uA4iHXGVkZJc7JQtKUJgDRdS7lS98oJmVZttAiZKl5kGyZXC5HQkICEhISIJfLrV0dkoBdSySZejBjjq4m9WBG2dVkim4nR6E6TPuNpW8AsN8h1rZEPcBQBhaGBBnKffXtr6ssQ+QVFiL10SM8zs4C7gFTd/yK47duYdIHnfF+vfpwcyn+eFdvlWFrTMn27NmDPn36AAC2bduGLl26WLlGpI9MoVAw49HOnTt3Dv7+/tauhiQZGRnw9bW/m60ykMr9bmnpz/XpJyaokXmV9jpt7RpN8f8mlTkmu1O2lNx/8QKxJ4/j9xs3cCLtFvIKC7Xu7+bignf93sD0kG5oKvHvraTWGPX/T0f+YjFjxgzMmzcPAPDVV19h6tSpVq4R6cMWGSKJlC1FZaHp3dYCEXtiitYWdde+moHKkz6Hm4uLzuBFVV5hIQ6kXMPJ22nYPHwk3qldp8T9pXYp2XNX78aNG+Hm5obevXsL2xQKBdavX4979+5h4MCBqFGjBgoKCoT33dzcrFFVMhADGSIJlN8+LfnNnuyXqfJdnubkYMmhJCz/4wgAaA1i2vm9gUqenniUlYVjt/5ERXd3vHj5EgCQ+fIl+vy4ApuH/xNt69bVXY7E4NxeW2G2bduGyMhIAMDSpUsxfPhwAEBcXBxGjhwJoLj1JScnB/n5+cJxrq6uks4vl8vx+++/o1mzZqhYsaKJa0/6MJAhMgBbKuyTPf6/LVmyBDMXLUBmZqZoe/PmzREaGoqhQ4fq7KZNSkrC0KFD8fDhQ+Tk52NC0n6cWXQGMpnu+ZXUFRUVYc+ePVAoFOiqUBh0rK159uyZsDxz5kwMGDAA7u7uKFeunGi/GzduiFpkpAYyU6dORXR0NKpUqYKUlBR4enqapuIkCUctERHZmOjoaHzxxReiIKZp06bYtGkT/vjjD0yZMqXEXLOgoCDs2bNHWL969SrOnDkjufysrCz0798fYWFhCA8PR2JionEXYiMiIiLg5FR8u3vw4AFSUlIAQNTNBAD3798XBTLqgY42Fy9eRHR0NADgyZMn2LFjh6mqTRKxRYYcmlwuR2JiIs6fPw93d3e4ubnBy8sLXbp0wSuvvGLt6hFp+PnnnzF58mTRtnXr1qFXr17CzVgKf39/DB48GLGxscI53n77bb3HpaenIywsDBcuXBC26RsTolAocPv2bezcuRM1a9ZE9+7d4eIi7fai/BsFgC5duhh0jUqbNm1CZmYm+vfvDy8vL4333d3d8d577+HQoUMAgIcPHwIALl++LEpcfvjwoUFdSwqFAl988YVoG7uWLI+BDDm0xMREhIWFaWz38vLCvHnzMGLECADFH0ixsbGoXLkyunXrZtfN6GS/tm3bhk8++bsbLDAwENu3b9d6c5Zi0KBBQiATFxeHb775psRWhqysLPTs2RNXrlwRtn322WcICQkp8ZiQkBCcOnVKtH3kyJGIiorSe2NX/RvdunVriWVpEx8fj6FDhwIA1qxZg0OHDmn9+61ataqw/OjRIwDA119/Lcr7UQ9k9LXITJw4UQiOlFSPJ8tg1xKVSdnZ2RgzZgxOnz4NANi5cyf+9a9/oW/fvli7dq3G/gqFArt370ZCQoLeb6dKGzduxK+//mrSepPjSklJwbBhw4RJ2N566y1s3bpVUhCjDMS3b98u+v1s166dsPz06VOhS0XXOT766CNREDN48GDMmDGjxMA+Li5OI4gBgB9//FFIpC2JapeX8u/REKqT1p08eRJ37tzRup9qUPLkyRPI5XIkJyeL9ikoKJDUtaRsiVmyZInGey//P9GaLIeBDBklJiZGY6ZfW9SlSxds2bIFkyZNwtixY9G3b1/R+8r5In777Tdhm2pioNKcOXMQFhaGPn36SMoX8PDwQGRkJPr37w8PDw+7HrZKlrFkyRLRt/mdO3fC29tb0rHbt2/HqFGj8I9//EMUiDs5OYm6k0oadbRkyRJs2bJFtC02NhZt27bF0aNHdR5XoUIFne/t2LFDlKtjDv369ROt//e//9W6X5UqVYRlhUKBI0eO4Pnz56J9FAqFpGTf3bt3aw1iACAvj896szQGMuTQnJyc0LVrV8yYMQPffPMNYmJicPLkSeH9HTt24PHjx1i5cqWw7Y033hCd47fffkNUVJSwzjkkydSePXuGdevWCeu//vqrqCtEn507dwrL6jdn1RE0OTk5Wo8/cuQIpkyZIqx/8MEHwvLly5cRHByMkJAQ7N27V2Pa/n79+iE2NhZr1qxBbm4ucnJy8Oabbwrvf/fdd5Kvw1h16vw9T467u7ve/fPy8rTO2KtQKAwefh0aGoqIiAhhnS0ylsdAhgxmiSdhm1OTJk1E66o3EE9PT7Ru3VpYf/jwISIiIoTgpUKFCmjbtm2J58/KytJokrbX+TfIMnbs2CEEGS4uLqJAQopLly4Jy+q/36qtgdoCmYyMDAwcOBBFRUUAgFatWmHz5s1YsGCBKAhKSkpCz549ERAQgMWLF4taLsPDw4WWEZlMJuSsANKHMBursLAQ9+/fF9abNm2q95ivvvpK63a5XC7qmtLVtdS1a1fEx8cjPj4eGzZsELX2sEXG8hjIUJkUGhoqLK9YsUJYHjlypOhDaf78+cjOzhbWMzMzMW7cuBJbZQ4ePCh8q2vatCmDGNJL9XckKCjIoGTzwsJCUXdKSYGM+u9ifn4+IiIihOTXatWqYcOGDXBzc8OYMWNw9uxZ9OjRQ3TMjRs3MHHiRPj5+WHatGlaH6yo2v366quvSr4WY5w8eVJoBfH19UXlypW17nf16lWt29966y1h+dq1azq7plTJZDJ069YN3bp1g7Ozs2gGYLbIWB4DGTKIvbfGKF2+fFlYvnnzJoDi6cjHjx8vbL97966oy0lp06ZNolYcdQkJCcKyoSMwqGxSHar82muvGXTsxYsXhVaAV199VaNLSrVVRT2QmTp1Kk6cOAEAcHZ2xtq1a1GzZk3h/ddffx1xcXG4cOECxowZI8rZyc3NxaJFi7B+/XrROW/cuCEayaOew2Jqqnk9JbWWqnc5eXt7Y/Xq1ejQoYOw7cWLF6J9Ro8eLRqGrovqlx0GMpbHQIYcVmFhodaWk7NnzwrBi6rIyEjRt8f58+cLLSutWrUSBXDjxo3Dn3/+qXEOuVwuCmS6du1aqmugskG1+0U12VSK1atXC8vaulV05cjk5eVh1apVwvqcOXPQvn17jeMVCgWuXr2KgIAApKamYunSpQgICBDOrZoPo1Ao0L17d6Gb6v333xcFCqaWk5MjSm5WPnpAG9XctyFDhuDKlSvo37+/qPVLvSUsLS0NQUFBorw6bVRbZJjYb3mcR4Yks5fWmCtXrqBbt25Cv7mPjw8qV64MHx8fnbOburq6YsKECcL67du3RTeI6dOno02bNjh06BDS0tKQnZ2NRYsWYfHixcI+CoUCS5cuFcqtUKECioqKUFRUBGdnZ3NcKjkIYwOZ9PR0YZ4YABg4cKDGPrq6lsqVK4e2bdvi4MGDGDlyJCZNmoRJkyaVWN6oUaNE68eOHUP9+vUBFP/+T5w4Ebdu3RLe//e//23WOZni4+OF5OYaNWqgcePGGvvk5eXh4MGDop+rv7+/0AWlWr8bN24Iy66urigoKEBubi6mTZuGvXv36qyHsmsOAKpXr278BZFR2CJDDqOgoADDhg3D22+/LUr+e/bsGW7evKkRxKg25w8ePFjUpD937lzhgy8wMBDBwcHw8vLCrFmzhH3WrVuHv/76S1jfvXs3Jk6cKKxnZmaiY8eOaNiwIWbOnInbt2+b7mLJoRgbyMyYMUPoymjRooXG9AKA7mRfmUyGXbt24caNG6KA3BCqQcy0adNEQ5IHDRokSpw3h4UL/37Y5b1791C3bl306tULhw8fhkKhwMuXLxEcHIzevXuLhoGrttSqBjKqLbXKqRmA4lFdhw8f1lkP1UCmWrVqxl8QGYWBDEli660xCoUCn376KeLi4vTuK5PJ0KhRIxT+/5OEnZ2d8fnnnwvv//nnn6JvudOnTxc+7MLDw4UchNzcXK2T56m7e/cu5s6di7ffflvIRyBSpTo65sCBA5KOuXDhgig/5ZtvvtE6vb/qBHfqibkymUx4ZpOhSenK/bdt24ZGjRrh22+/Fd7r1asXvv/+e4POZ6gLFy7g+vXrGtv37NmDDz/8ENWrV0elSpWELzD37t0T9tEVyCifbeXt7Y1Ro0aJuqpmz56tsy7KRx4AbJGxBgYyJJlyEjzVyfBsZWK8/fv34+effxbWa9WqhQMHDuDFixe4c+cOzp8/j6SkJCQkJCAjIwO1a9cW9o2IiEDdunWF9fPnzwt9/EFBQaK8AZlMJpoATLVFpkWLFsKyk5MT3nnnHVEds7KyzD45GNkn1ZEz+fn5ehNGFQoFpkyZItyQu3Xrhvfee0/rvqqtMKr5LNrk5uaKXqrBSFhYmOg9AFi/fj0GDBiAtLQ0Yb+QkBCsWbPGJMOuHzx4gLt372p9TzW/p27duhrPTsvKyhKtBwYGCsu6Ahml9u3bw9nZGRMnThRablVbZR49eiQK/NgiY13MkSFJtLXG2FIrzS+//CIse3t749q1a8IHVNWqVUUjOc6ePSsMD5XJZBoPfQsNDcXgwYORlpaGH3/8UaOs3r17Y9GiRXBxcUGvXr2E7apBSvv27ZGQkICCggIkJiZizZo1cHJywrhx40xzweRQXn/9ddSrVw+pqanIzc1FcnIygoODde5//PhxoeXG2dlZo7WgqKgIe/bsgVwuF3WpNmvWzKB6qY7u05ZIrDojtpJcLjc6L6aoqAgJCQk4cOAA9u/fj//+979wdXXFgQMH0LJlS2G/rKwsbNiwQVhfvnw53nvvPaSmpiI6Olrj7zYkJASNGzfGvn37AOgPZN5//30AQO3atTFo0CDhS1K3bt2wefNmhIWFwc/PD4mJifD19RUFMoZMZEimwRYZsntyuRy7du0S1uPj40v8IJ07d66wHB4ejgYNGojed3Z2xooVK7Bnzx7RUFSlmTNnIjo6Gps3bxZGbwDFiY9KytYZV1dXhIaGIj4+Hps2bSpxOncq2zp27Cgsq84Uq42np6fQUvDxxx/D399feO/ly5cYNGgQwsLC0LdvXyEZ1sfHB6+//rpBdbp48aKwrN6as2zZMmzcuFHjmD179mDMmDFGzYC9cuVK9OnTB0uWLBHmcykoKMCOHTtE+ymfdg0ADRs2FJ4pVa9ePSxevBhpaWnC3+53332HuLg4ZGRkCMcvX74c//nPf/D8+XOtnxVBQUHC8sSJE4XWpcLCQvTu3RtyuRypqak4deoUnj9/LuQ1eXl5iUaJkWUwkCG79+LFC1Fyr65p2IHiGVBVPxT1jdLQxtnZGaNGjdKY4lx1xIO2YaxEJenUqZOw/OLFC8yaNUtnMBAQEICtW6CF9VQAABNfSURBVLdi6dKlQlLq06dPER8fj0qVKolaKJU+/vhjg1pKFAqFaMbg9PR0YfnEiROilsygoCCMHTtWWI+JicH06dMllaPsxgWKH+aoqly5cujTp4+oJTMvL0/0hPCRI0dqXFf16tWF1q3g4GC8//77ohacu3fvYsqUKQgMDBS1pgDFc9Gojn6qW7euKKlYVYsWLUT5MexWsg6Zgg+OsXvnzp0TfSOzZRkZGUJyoSm1bdsW586dE23r0qWLMCQzMjISXl5eJpnjQVdSpJ+fn5BQeOHCBWFEB5EURUVF6NevH3bv3i1sq1mzJnx9fREUFIT8/Hzk5eXh5cuXwku5fvDgQchkMo3AZ/To0Zg7dy6uXLmCgIAArcnAuty4cUNjluBvv/0Wffv2RZs2bYTAxtfXFxcuXICnpydGjRolSoBfuHChKOjQds2tWrXSmE03NDQUI0eORLt27TRaOL7++mssWLAAQHHLVGpqKipVqqT1/Js3b8Ynn3witN5o4+7uLuQkhYWF4bvvvtOYHVj5ZHD1fMDc3Fz88ccfQhDaqlWrEkc3kXkwR4YcwuzZs9GrVy9hJBIgnib94sWL+Oyzz0xSVkJCAs6cOQNXV1e4uLjA1dUVzs7OomfPDBw4EIcPH0a5cuVw/vx5lCtXTm+iJZVtzs7OiI2NRUhIiDC67e7du7h7967eCdkAzYeZzp07F2PHjoVMJjMoN6aoqAjR0dGi4cdK48ePx5QpU4Qbv7e3Nw4cOAAvLy8AwPfff48nT54Ik0J+8cUXeOWVVxAeHq61rMTERFEQ8/rrryMpKQk1atTQWT/VB2RGRUXpDGKio6MxefJkre+pBn2qidXvvvuu1kccyGQyREdHiwIZ5bwynEPG+hjIkEPo2LEjTp06hVmzZommLFeSyWTCt7jSiI+PR58+ffTud/HiRdEHrKurK/bv349WrVqVug7kuDw9PfHLL79g8uTJ+OWXXzSmzC+Js7MzWrZsiQ4dOiA0NFQ0ik6qx48fIzIyUkiK1Ub1xr98+XLRCEBXV1esXbtWCMYUCgWGDx+OKlWqaJ3hV71LaPDgwSUGMQDw5ZdfYvTo0YiMjNSYoE/pwIEDmDp1qrDu5+cnmiPGyckJX331FWbMmCE6TjXnTZ27uzsyMzPx888/w9PTE05OTvjzzz9Fo6rYtWQd7FpyAOxaEnv06BFu376NjIwMZGRkwMPDA4GBgWjWrJnQHz9nzhyMGzfO4NEVCQkJkgIZbV555RWEhISgdevWCA8PR/ny5Y06D5UNBQUFOHbsGH7//XcAxTdSNzc3uLu7a7w8PDzw5ptvomLFikaXd+zYMQwcOFCUFFu1alWEh4cjNzcXKSkpOHr0qOiYQYMGaX0e2dOnT9GxY0fhQY0VKlTA3r17NVqG5HI5IiMjsWnTJgDAtGnT8OWXXxp9DUBxy9Sbb74pPEKkYsWKuH79umh4tpOTE+7fvy9qQfHz88OZM2dEjxtQt3z58hJHHk6YMKHE+WbIPBjIOAAGMvo9e/YMAQEBombgFStWYPDgwQadRy6XIzExEadOnUJhYSEKCgpQWFgovJKTk5Genq73m3S9evVw6tSpEj80iSwlNjYWo0ePFnXNTpw4EdOmTRNN1vf06VMMGzZMGHbt6uqKx48fi/ZRunPnDoKCgoTAyN/fH2fOnNH48jB79mxERUUBME0gc+LECWH4NFA8weWrr74qyo+TyWTIyclBmzZtcP78eQDFra3dunUr8dxRUVElBipubm7Cox4MyUei0mHXEpUJPj4+2Lt3L0aPHi18qzSk2V7JyckJXbt21fswyPT0dBw4cACHDh3CtWvXcP78edFN4t69e8jNzWUgQ1aXmZmJcePGCb+flSpVwk8//aQxKg8AKleujG3btmHhwoWIjY1F//79tQYxQPGklDt27EBwcDCeP3+Ox48fo6CgQOf+pqJs3QE0HwSrpPz+rppILOU7/dixY7Fq1SrRLMHOzs5CS29eXh5mzpwJd3d3jB8/3uhrIMMwZKQyo27duqKmcfURGab02muvYciQIVi1ahV+//13PHz4EPv370dUVBT69euHNWvWwMfHx2zlE0nl4eGBhg0bAgBatmyJY8eOaQ1ilJydnTFp0iRcunRJb+tJ48aNceTIEXz22WfYtGmT2YOYoqIixMfHC+v9+vUTlr29vYVlZf6a6txP6o9v0CY3NxfZ2dnC+rJly/D8+XMkJCSgSpUqou1SzkemwRYZcljKbiCgeCj2nDlzhPc8PDxE08KbmzJPR3WadCJb4OLigsOHD+PcuXN46623TPJoAVX169cXuo7M7d69e3jw4IGwrvrYhvj4eHzwwQcAiodl37t3T2iFkclkePfdd/Wef8aMGUJLbsOGDTFgwAA4OzsjKCgIKSkpQjBz+/ZtXLlyxaxfluhvDGRIkpKep2QrjylQl5iYiLCwMADFE1epTtU+e/ZsjRYR9cCHfdxUVri4uIgeAWCv1B8imZmZKfydt2vXDqdOnYJMJkPjxo1F+XHNmzcXtahoc+7cOaxevVpYnz9/vijo8/T0hL+/v5DgbEzXNRmHgQxJZqsBixSqQcz777+Pjz76SGMf1cBn69atCAkJsVj9iKj0WrduLVr/8MMPcfz4cWH9zTffxJMnT9ClSxccOnRI2P7xxx/rPffs2bOFFpyQkBB07txZYx9lEAMY/jRxMh6/cpJDUigUePbsmUYybe3atbFixQqtrS2qwc7p06cB/P0cp927d7PPm8gMVCe4Ky1PT0/4+fkJ6xcuXMDmzZvx/PlzXL9+Hf/+97/RqFEjURAzYMAADBw4sMTzKhQKUT6NtkTe7OxsUQ6QMu+IzI8tMmRzVIdJGvqtJiEhAVFRUUIgou3c2h4EqUtiYqIwK+mWLVv0jlYiIukuX74sDH8GYJJk4KSkJNHDMUtqSQ4MDER0dLTe+aRyc3NFz4G6d+8e5HK56AvRvHnzkJ+fD6A4yfm1114z9hLIQGyRIYPExMQIL3Pw8PBAbm6u8DL02UjDhg3TCGJU5625evUqjhw5Ivl8qqOcLly4YFBdiKhk6n/f6l1DxqhWrRoOHjyIWrVq6dyncePGiIuLw759+yRNTOnp6YnmzZsL60OHDoWXlxf69++P8ePHo1mzZqKZw7V1O5H5MJAhyWJiYjBkyBDhZepgRhnEqDI0mOnVq5ew7O3tjcjISJw9exYjR44Utqs+BVeVaqCi/KalWh/l82Q2b94sGuJJRMbx8/MTWjnr1auHtm3bmuS8bdq0wcmTJxEZGYkKFSqgfPnyqFq1KgICAvDTTz/hxIkT6NGjh0Eze8+aNUujxejXX3/FsmXLcO3aNWFbjRo1RE8CJ/PjzL4OwBIz+yqDGKnbdTFmZl9tAY4uhYWFuHbtGmrUqIFKlSoJH1QnT55E+/btARRPl56WlqYRIH3wwQfCdPBr165FUFAQWrVqJUx+tWTJEnh4eGDEiBEAimdD1fUwPCKSJjs7G8nJyWjZsqXOB0DaiqtXr2LVqlWIjY3F8+fPNd6vWbMmNm/eLGq9IfNjjgxJYskRS4Z2J6lycXHR+pTpli1bol69ekhNTUVmZiZ2794tjFACip9ro9olVa9ePTRq1AiZmZnCtiZNmmDMmDHCuup76hQKBRISEqBQKNC1a1eDn+lEVFZ4eXkJ87vYOn9/fyxYsAAzZ87EH3/8gcePH+PJkyfIy8vDO++8g1atWnG2bitgIEM2RVvrS2kCGyWZTIYBAwZg5syZAIq7l5SBjFwux7Jly4Ryvby80KZNG9HxlSpVQnp6Oi5dugSguM+8pIdH7t69W2it4VBuIsfi4eGBTp06Wbsa9P+YI0OSmCu5V5UhXUjGGDBggDCB1f3794XtiYmJmDhxorCuOgW5Urt27fDJJ58I6/369RNNea5OdXjnlStXSlVvIiLSjYEMlRm1a9fGunXrEB4ejrVr1wrbdQVPqt1BFy9eFPrE3d3dRV1M2qjOMFqtWrXSVJuIiErAQIYk0TZKydBEX320jVAyRbeSqtDQUMTGxqJOnTrCtrS0NGG5UqVKWLhwIQYNGiTM4uni4oJbt24BKB7NFBMTozUPR+nUqVPYs2ePsF61alWTXgMREf2NOTIkmXowY44EYPVgRtlaYo5upzt37iA9PR3R0dHCtlmzZmHo0KGiB0oWFhYKy/Pnz0doaKjGuYqKinDz5k2sXr0a3377rei96tWrm7TeRET0NwYyZBBLjF7SFrCYOog5fvw4unbtipycHGGbr68vBg0ahK1bt+LmzZtaj1N2GSkUCmzfvh27du3CpUuXcPXqVZ11ZNcSEZH5MJChMuPhw4f4/vvvsX79ety5c0fj/dq1ayMvLw/z58/XeY4VK1YgIiICKSkpGDVqlKRy2bVERGQ+zJGhMmH//v1o1KgR5s2bpzWIAYofR/DOO+/g8uXLou0ffvihMHxaoVBgzJgxqFChgsbx1atXR8eOHTF8+HBhW8WKFYUZgYmIyPTYIkMOLzk5GWFhYcjLy9O7r2rir9K6devw9OlTJCQkAAAuXboET09PrFixAs+ePUOTJk3QpEkToQtp5cqVwrHvvvuuia6CiIi0YSBDDm/69OmiICYmJgY9evRAUVERdu/ejYYNGyI0NBQPHjzQOHbfvn3w8vKCl5cXPv74Y/zwww8AgJ49e+rMifnPf/4jLAcHB5v4aoiISBUDGXJot27dEp6fBABJSUnCE3blcjk8PT0RFxenNYgJDg4WtaiMGjVKCGQA4IsvvkCNGjXg6ekpBDuPHj0SJQpz9k8iIvNiIEMO7cmTJ6L1x48fIycnBxkZGZg8eTJ27dql9Thvb2/MmTNHtE39wZxLliwpsez69euL5qshIiLTY7IvObSCggLRenh4OKpUqYKmTZuKJq1TKl++PBISEnD69GnRXDJKDx8+RN++fSWVff36dQwdOhRFRUXGVZ6IiPRiIEMOraTnIalOdAcUz9q7ceNGBAUFoWbNmlqPqVChAtasWSPa5uLigoEDB6JXr15wd3cXPdpg+/bt+Oabb0pxBUREVBIGMuTQGjVqpLGtSZMmGts6deqE5ORkdOzYUe85L1y4ICy7ubnhzp07+PHHH7Fhwwb89ddfuHfvHgICAoR91AMfIiIyHebIkMObNGkS5s2bBwDw8vLCiRMncPToURw6dAjZ2dno2LEjOnToIPl8qo9p6NWrF3x8fETve3t7o3fv3kLAU7FiRRNcBRERacNAxgGUL1/e2lWwaTNmzEDVqlWRmZmJSZMmQSaTITAwEIGBgUad748//hCW8/PzRe+lpaVh0aJFWLFihbBNOUqKiIhMT6ZQPuKX7NbLly+Rnp6OrKwsa1elTIiKikJ8fLywXqtWLbx8+RKPHj3S2LdWrVpYvXo1qlSpYskqEhGVGQxkiAx09epVtGzZEtnZ2SXu17p1a2zYsAF169a1UM2IiMoeJvsSGcjf3x8nT55Ehw4d4OKi2TvboUMH7Nu3D0ePHmUQQ0RkZmyRISqFvLw8XLx4EVevXoWPjw/8/PzQuHFja1eLiKjMYCBDREREdotdS0RERGS3GMgQERGR3WIgQ0RERHaLgQwRERHZLQYyREREZLfK/CMKrnWqLiw33PfQYcoiIiIqC8p8IANYLqhQlqMa0FiSTCYTljnqnoj4mUCOwCYDGVtruZBSH1ursy78sCIiJeXngWpAQ2RvbC6QudapuigQUF8vzbnMVR9T1tnaLP0NTSaTWawcJXOXZ41vucoyzVFeSTc5c12fJX6Gjnpd1iiLyJpsKtlXWwDQcN9Dq3XFSKmPOepsza4nhUIhvBzlW5olr8tRf4aq16T6MgdL/QwteU0Afw+JzMWmAhkpdN3kLXnzt9fWFlsik8ks8uGqrcXHXB/slixLX7n2ylo/w5LKN9d5He33kMha7C6QkUoZ2FzrVN2sQY45ghprBEqW/vAz97dfciyO1M1JRKZlczkypqLs3jFFUGBoIq8958g4GkvemKxxE7TkzZc5F8ZTfilQ/bkxcCIyDYcNZExFaiKvvYxaIsvf/B3hZmXpm7AjJp2rt3A6wu8FkS1gIKOHrkRebduV2CJjuyxxw7LUzcqSQZKubkdL5JMwGDSMrtYfIkflsDky1mTNkVaknTK52BI3REcbLWLpIMIRE1WtkYOm/J13lECQSBcGMqVkjoCFQZBpqQ5FtTRLjkwh4zjqz9ISQ8qJbAEDGXJo1kqGtVR5qi/VbaYuh+wH/7+orLGpQEZbl4x6vomufWytPqXJkbFGfo22lgNH/abqCHRN5MZv4ERU1thcsq96YKDtpq5tH23BjOp2Y4MDY+vj6Bx15E9pyjJ0iC2vy7plGcperotDvamskSnK+G+3NUYYWWtUk5QPM6kjbkz1wSi1TsaWZejzdExxXZb+GUo5n71dl6XLknIOe7wuKWWZqjwia7G5FhlrKG2rjaHl2DJrj1Cxt/PbSpmWKNdRJxdkWUT2rcy3yJQlpprfxF6a81kWy2JZ+stS4q2A7BUDGSIiIrJbNjVqiYiIiMgQDGSIiIjIbjGQISIiIrvFQIaIiIjsFgMZIiIislsMZIiIiMhuMZAhIiIiu8VAhoiIiOwWAxkiIiKyW/8HjItoGEoIH6wAAAAASUVORK5CYII=" alt="image.png"></p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[65]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">b</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">))</span>

<span class="n">b</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[65]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[67]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 0 ~ 9까지의 값에 +2씩 해서 리스트 생성</span>

<span class="n">c</span> <span class="o">=</span> <span class="p">[</span><span class="n">i</span> <span class="o">+</span> <span class="mi">2</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)]</span>

<span class="n">c</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[67]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[2, 3, 4, 5, 6, 7, 8, 9, 10, 11]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[68]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># if문도 사용 가능 </span>
<span class="c1"># 0 ~ 9까지 숫자 중에 짝수만 뽑아서 리스트 만들기</span>

<span class="n">d</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span> <span class="k">if</span> <span class="n">i</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">)</span>

<span class="n">d</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[68]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[0, 2, 4, 6, 8]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data:image/png;base64,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adu2bRo2bJhmzpypAQMG0NIfQwzD0L///W8z3O/cuVNffPFFvet06NChRrjv2rUrv3MAMYs++w4TrT77kiJ6gq6vvvn02Uc0XLp0SXPnztWCBQtUXV1d47Hvf//7mjlzpkaNGqWmTZtaVCG8uXLlioqLi1VcXKyDBw/qyJEj2rFjh86cOVPveikpKRo4cKAGDRqkrKws9ejRg3APwDEI+w7jlBN0Cfuwg4MHD+r3v/+93n77bdV+q7zhhhs0bdo0/eQnP1GrVq0sqrBxqKys1Llz51RcXKyioiIVFRWZ993h/uzZs3WGwfSldevWGjBggNly37NnT/rdA3AsuvEAgA99+vTRmjVrdPLkSb388stavny5rl69KkkqLCzUE088oSeeeEKTJk3S5MmTlZmZSYtwAAzDUElJic6ePWuG9toBvri4WF9++WWdD1uBaNmype68805lZWVp0KBB6t27t+Li4sJ4JABgX4R9AGhA9+7dNX/+fP3mN7/RK6+8okWLFumrr74yH1+2bJmWLVumnj17atKkSRo/frxSUlIsrDh6DMNQeXm5SktLdfHiRb9/nj59WqWlpaqoqAhbLfHx8UpLSzNvffv2VVZWlvr06UOXKwCNFmEfAPyUmpqqJ598UrNmzdIbb7yh+fPn6/jx4+bjx44d05w5c/TUU08pIyNDEyZMUI8ePZSRkaEbbrghql1FDMPQ5cuXdeHCBa+3b775RtXV1aqqqjJvtadr30pLS1VZWVknvH/77bcRP5727dsrPT1d6enpSktLq/HTfT81NZXuOABQC332HcZJV9D1NfQmffZhF4Zh6IMPPlBeXp7WrVvn9cqqbs2bN1f37t2VkZGhxMREpaenyzAMs3uK+77nraH5klRWVqbKysoaQb6kpEQXL16MSggPVevWrc2WeHdoT0tLU6dOncx5HTp0UEJCgtWlAkBMIuw7TLTCvhT60Jv+XEG39kW1OEEXdlVWVqY1a9YoLy9PH330kdXlRFXTpk3Vpk0btWnTRq1bt/brZ0pKitLS0tSyZUurywcARyPsO0w0w36o/An7QCw6fPiwtm/frhMnTqigoEAFBQW6cOFC1OtISkpS27ZtlZKSorZt29a473K5lJycrLi4uBq3Jk2a1JnnvsXHxys5OblOeE9MTOTEZACwKfrsA0CY9e7dW717964x7/z58yooKNCJEydUXFwsl8tV4yapzjx/5ycnJ9cJ9G3atOEidAAAwj4AREO7du3Uv39/9e/f3+pSAACNCMMWAAAAAA5F2AcAAAAcirAPAAAAOBRhHwAAAHAowj4AAADgUIR9AAAAwKEI+wAAAIBDEfYBAAAAhyLsO0zLli2tLgEAAAA24TIMw7C6CITP1atXVVhYqEuXLlldCgAAACxG2AcAAAAcim48AAAAgEMR9gEAAACHIuwDAAAADkXYBwAAAByKsA8AAAA4FGEfAAAAcCjCPgAAAOBQhH0AAADAoeKtLsBOTtzTwbzfY8uXjtkXAAAAGifCfi3RCt7u/XiG/mhyuVzmfS6i3HjwewcAoHGxfdi3Wwu4P/XYrWZfCHuNj/t37hn6AQCAc9k67J+4p0ONsFx7OpRtRaqecNZstWi2AlvR4uzeZyT35/TnEAAA2JttT9D1FpJ7bPnSsm4v/tQTiZqt7OZjGIZ5i2RLcDT3FU08hwAAwGq2Dfv+8BWEoxmQY7XV3i7cIdVTNMKqt/1GevuROi6rnkMAAGB/MR32/eUO/yfu6RDRDwLeWvFD7cZjxYcJwmPk0L0GAABEk6377IeLO4SHIzg3dPJt7cBPy3/9rAi/kW7Vjzb3BzHPY3LaMQIAgOA0irAfLo3tBF2rOCmoRuuk2drfvDjl+QMAAKFpFN14wsWKE3QbGyv60kd6X5ygCwAArELYhy24XC5HtehLdVvXOUEXAABEG2Hf5hrDtwKerdLR2A8AAEBjQZ99WCraAdxba3c0Lq4FAABgBdu27PszjKWvZexWT6wNvemtC4gTWsU9+7R7fpMQjW8VAAAArGDrln1/hrH0toy3wO85P9gAHWw9TmfFSa9231egw2FGc18AAKDxcBkkApMVw2RaNTSnP2HQ36EcQwmW9Z1E6m2b4Q6xkQrgnttwi9RzGOi+wrU/AABgf7Zu2bdCqK3/ge7HzqIRBq0OnJHefzSPz+rnEgAA2A8t+41UuC7AFCvdatjXf/blxp8+AADOR9gHAAAAHMq2o/EAAAAACA1hHwAAAHAowj4AAADgUIR9AAAAwKEI+wAAAIBDEfYBAAAAhyLsAwAAAA5F2AcAAAAcirAPAAAAOBRhHwAAAHAowj4AAADgUIR9AAAAwKEI+wAAAIBDEfYBAAAAhyLsAwAAAA5F2AcAAAAcKn7dunVW1wAAAAAgAlyGYRhWFwEAAAAg/OjGAwAAADjU/wF0webBmqWiPwAAAABJRU5ErkJggg==" alt="image.png"></p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>컨프리헨션을 이용한 구구단 만들기</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[73]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 2단</span>

<span class="n">gugu</span> <span class="o">=</span> <span class="p">[</span><span class="mi">2</span><span class="o">*</span> <span class="n">i</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">10</span><span class="p">)]</span>

<span class="n">gugu</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[73]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[2, 4, 6, 8, 10, 12, 14, 16, 18]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[76]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># 2단 ~ 5단</span>

<span class="n">gugu</span> <span class="o">=</span> <span class="p">[</span><span class="n">a</span> <span class="o">*</span> <span class="n">b</span> <span class="k">for</span> <span class="n">a</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span><span class="mi">6</span><span class="p">)</span> <span class="k">for</span> <span class="n">b</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">10</span><span class="p">)]</span>

<span class="n">gugu</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[76]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[2,
 4,
 6,
 8,
 10,
 12,
 14,
 16,
 18,
 3,
 6,
 9,
 12,
 15,
 18,
 21,
 24,
 27,
 4,
 8,
 12,
 16,
 20,
 24,
 28,
 32,
 36,
 5,
 10,
 15,
 20,
 25,
 30,
 35,
 40,
 45]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>리스트 map() 함수</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[78]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mf">1.1</span><span class="p">,</span> <span class="mf">2.3</span><span class="p">,</span> <span class="mf">3.6</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span><span class="mi">7</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[79]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># for 반복문 사용해서 float - &gt; 정수 변환</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mf">1.1</span><span class="p">,</span> <span class="mf">2.3</span><span class="p">,</span> <span class="mf">3.6</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span><span class="mi">7</span><span class="p">]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">a</span><span class="p">)):</span>
    <span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">a</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    
<span class="nb">print</span><span class="p">(</span><span class="n">a</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[1, 2, 3, 5, 7]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># map 함수 이용</span>

<span class="n">a</span> <span class="o">=</span> <span class="p">[</span><span class="mf">1.1</span><span class="p">,</span> <span class="mf">2.3</span><span class="p">,</span> <span class="mf">3.6</span><span class="p">,</span> <span class="mi">5</span><span class="p">,</span><span class="mi">7</span><span class="p">]</span>

<span class="n">a</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="nb">map</span><span class="p">(</span><span class="nb">int</span><span class="p">,</span> <span class="n">a</span><span class="p">))</span>

<span class="n">a</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[1]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[1, 2, 3, 5, 7]</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">b</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="nb">map</span><span class="p">(</span><span class="nb">str</span><span class="p">,</span> <span class="nb">range</span><span class="p">(</span><span class="mi">10</span><span class="p">)))</span>

<span class="n">b</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[4]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[&#39;0&#39;, &#39;1&#39;, &#39;2&#39;, &#39;3&#39;, &#39;4&#39;, &#39;5&#39;, &#39;6&#39;, &#39;7&#39;, &#39;8&#39;, &#39;9&#39;]</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data:image/png;base64,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" alt="image-2.png"></p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div>
</body>







</html>
