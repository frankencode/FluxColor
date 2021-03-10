FluxColor (QML Plugin)
======================

About
-----
__FluxColor__ is a light-weight HSV color chooser for Qt >=5.6.
The implementation is purely based on QtQuickControls 2.

Screenshot
----------

![Screenshot](screenshot.png)

How to use
----------

Copy the __FluxColor__ plugin directory to your project resources or add its parent path to your QML import path.
See https://doc.qt.io/qt-5/qqmlengine.html#addImportPath for details on import path handling in C++ projects.

The __FluxColor__ plugin provides a single `ColorChooser` type (see example below). It works best with a dark style, e.g. Universal Dark. You can select the style by pointing the environemnt variable `QT_QUICK_CONTROLS_CONF` to the `qtquickcontrols2.conf` shipped with this plugin:
```
QT_QUICK_CONTROLS_CONF=qtquickcontrols2.conf
```
See https://doc.qt.io/qt-5/qtquickcontrols2-configuration.html for details on style selection.

Example (QML)
-------------

```qml
import QtQuick.Controls 2.6
import QtQuick.Controls.Universal 2.6
import FluxColor 1.0 as Flux

ApplicationWindow {
    visible: true

    Universal.theme: Universal.Dark
    // Universal.accent: Universal.Violet

    minimumWidth: colorChooser.width
    minimumHeight: colorChooser.height
    maximumWidth: minimumWidth
    maximumHeight: minimumHeight

    title: "Select Color"

    Flux.ColorChooser {
        id: colorChoooser
    }
}
```
