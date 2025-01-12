---
title: accesskey
slug: Web/HTML/Global_attributes/accesskey
tags:
  - Global attributes
  - HTML
  - Reference
  - accesskey
browser-compat: html.global_attributes.accesskey
---
{{HTMLSidebar("Global_attributes")}}

The **`accesskey`** [global attribute](/en-US/docs/Web/HTML/Global_attributes) provides a hint for generating a keyboard shortcut for the current element. The attribute value must consist of a single printable character (which includes accented and other characters that can be generated by the keyboard).

{{EmbedInteractiveExample("pages/tabbed/attribute-accesskey.html","tabbed-shorter")}}

> **Note:** In the WHATWG spec, it says you can specify multiple space-separated characters, and the browser will use the first one it supports. However, this does not work in most browsers. IE/Edge uses the first one it supports without problems, provided there are no conflicts with other commands.

The way to activate the accesskey depends on the browser and its platform:

<table class="standard-table">
  <tbody>
    <tr>
      <th></th>
      <th>Windows</th>
      <th>Linux</th>
      <th>Mac</th>
    </tr>
    <tr>
      <th>Firefox</th>
      <td colspan="2">
        <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd><em>key</em></kbd>
      </td>
      <td>
        On Firefox 57 or newer: <kbd>Control</kbd> + <kbd>Option</kbd> +
        <kbd><em>key</em></kbd> or <kbd>Control</kbd> + <kbd>Alt</kbd> +
        <kbd><em>key</em></kbd
        ><br />On Firefox 14 or newer: <kbd>Control</kbd> + <kbd>Alt</kbd> +
        <kbd><em>key</em></kbd
        ><br />On Firefox 13 or older: <kbd>Control</kbd> +
        <kbd><em>key</em></kbd>
      </td>
    </tr>
    <tr>
      <th>Internet Explorer</th>
      <td rowspan="3">
        <kbd>Alt</kbd> + <kbd><em>key</em></kbd
        ><br /><kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd><em>key</em></kbd>
      </td>
      <td colspan="2">N/A</td>
    </tr>
    <tr>
      <th>Edge</th>
      <td>N/A</td>
      <td rowspan="3">
        <kbd>Control</kbd> + <kbd>Option</kbd> + <kbd><em>key</em></kbd
        ><br /><kbd>Control</kbd> + <kbd>Option</kbd> + <kbd>Shift</kbd> +
        <kbd><em>key</em></kbd>
      </td>
    </tr>
    <tr>
      <th>Google Chrome</th>
      <td>
        <kbd>Alt</kbd> + <kbd><em>key</em></kbd>
      </td>
    </tr>
    <tr>
      <th>Safari</th>
      <td colspan="2">N/A</td>
    </tr>
    <tr>
      <th>Opera 15+</th>
      <td colspan="2">
        <kbd>Alt</kbd> + <kbd><em>key</em></kbd>
      </td>
      <td>
        <kbd>Control</kbd> + <kbd>Alt</kbd> + <kbd><em>key</em></kbd>
      </td>
    </tr>
    <tr>
      <th>Opera 12</th>
      <td colspan="3">
        <kbd>Shift</kbd> + <kbd>Esc</kbd> opens a contents list which are
        accessible by accesskey, then, can choose an item by pressing
        <kbd><em>key</em></kbd>
      </td>
    </tr>
  </tbody>
</table>

## Accessibility concerns

In addition to poor browser support, there are numerous concerns with the `accesskey` attribute:

*   An `accesskey` value can conflict with a system or browser keyboard shortcut, or assistive technology functionality. What may work for one combination of operating system, assistive technology, and browser may not work with other combinations.
*   Certain `accesskey` values may not be present on certain keyboards, especially when internationalization is a concern. So adapting to specific languages could cause further problems.
*   `accesskey` values that rely on numbers may be confusing to individuals experiencing cognitive concerns, where the number doesn't have a logical association with the functionality it triggers. 
*   Informing the user that `accesskey`s are present, so that they are aware of the functionality. If the system lacks a method of notifying the user about this feature, the user might accidentally activate `accesskey`s.

Because of these issues, it is generally advised not to use `accesskey`s for most general-purpose websites and web apps.

*   [WebAIM: Keyboard Accessibility - Accesskey](https://webaim.org/techniques/keyboard/accesskey#spec)

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

*   {{domxref("Element.accessKey")}}
*   {{domxref("HTMLElement.accessKeyLabel")}}
*   All [global attributes](/en-US/docs/Web/HTML/Global_attributes).
*   [`aria-keyshortcuts`](https://www.w3.org/TR/wai-aria-1.1/#aria-keyshortcuts)
