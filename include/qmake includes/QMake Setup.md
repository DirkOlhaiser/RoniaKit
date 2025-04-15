# Integrating RoniaKit into a QMake Project

Follow these steps to include the **RoniaKit** module in your QMake project. The steps ensure the module is properly set up and recognized by Qt.

---

## **Step 1: Create a Subfolder**
- Create a subfolder in your project directory to hold the RoniaKit resources. For example:
  - **Directory name**: `RoniaKit`
- Copy the `assets` and `modules/Gauges/` folder into this new subfolder.

---

## **Step 2: Copy the `qmldir` File**
- Copy the `qmldir` file into the newly created `RoniaKit` directory.

---

## **Step 3: Update Your Resource File (`qml.qrc`)**
1. Open your resource file (`qml.qrc`).
2. Add a new prefix for the resource entries:
   - **Prefix name**: `/RoniaKit`
   - Add all the files from the `RoniaKit` subfolder to the new prefix in the `qml.qrc` file.
    - Include:
      - `.qml` files
      - `qmldir` file
  - Any assets, such as images or fonts
   - If you named the subfolder something other than `RoniaKit`, ensure the prefix matches the folder name.
   - **Important**: The prefix name must match the subfolder name; otherwise, QMake will not recognize the module.

### Example `qml.qrc` Entry
```xml
<RCC>
    <qresource prefix="/RoniaKit">
        <file>RoniaKit/Gauges/CircularBasicGauge.qml</file>
        <file>RoniaKit/Gauges/CircularGauge.qml</file>
        <file>RoniaKit/Gauges/FuelGauge.qml</file>
        <file>RoniaKit/Gauges/HalfDial.qml</file>
        <file>RoniaKit/Gauges/LevelGauge.qml</file>
        <file>RoniaKit/Gauges/RangeControl.qml</file>
        <file>RoniaKit/Gauges/RoniaControl.qml</file>
        <file>RoniaKit/Gauges/Thermometer.qml</file>
        <file>RoniaKit/Gauges/Extra/CircularAnalogGauge.qml</file>
        <file>RoniaKit/Gauges/Extra/CircularModernGauge1.qml</file>
        <file>RoniaKit/Gauges/Extra/CircularModernGauge2.qml</file>
        <file>RoniaKit/Gauges/Extra/CircularSpeedGauge.qml</file>
        <file>RoniaKit/Gauges/Extra/Style/CircularAnalogGaugeStyle.qml</file>
        <file>RoniaKit/Gauges/Extra/Style/CircularModernGauge1Style.qml</file>
        <file>RoniaKit/Gauges/Extra/Style/CircularModernGauge2Style.qml</file>
        <file>RoniaKit/Gauges/Extra/Style/CircularSpeedGaugeStyle.qml</file>
        <file>RoniaKit/Gauges/Style/CircularBasicGaugeStyle.qml</file>
        <file>RoniaKit/Gauges/Style/CircularGaugeStyle.qml</file>
        <file>RoniaKit/Gauges/Style/FuelGaugeStyle.qml</file>
        <file>RoniaKit/Gauges/Style/LevelGaugeStyle.qml</file>
        <file>RoniaKit/Gauges/Style/RoniaControlStyle.qml</file>
        <file>RoniaKit/assetes/fonts/Font Awesome 6 Pro-Light-300.otf</file>
        <file>RoniaKit/assetes/fonts/Font Awesome 6 Pro-Regular-400.otf</file>
        <file>RoniaKit/assetes/fonts/Font Awesome 6 Pro-Solid-900.otf</file>
        <file>RoniaKit/assetes/fonts/Font Awesome 6 Pro-Thin-100.otf</file>
        <file>RoniaKit/assetes/fonts/FontsFree-Net-DS-DIGI-1.ttf</file>
        <file>RoniaKit/Gauges/assets/images/gauge/glass.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/knob.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/needle.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/needle-light.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/needle-top.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/numbers-Layer1.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/redNeedle2.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/redNeedle3.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/backScreen.svg</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/innerRing.svg</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/middleRing.svg</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/outerRing.svg</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/preview.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/topScreen.svg</file>
        <file>RoniaKit/Gauges/assets/images/gauge/AnalougeGauge/VoltageGauge.rar</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Fuel/back.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Fuel/fuel-station-green.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Fuel/fuel-station-red.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Fuel/fuel-station-yellow.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/back.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/blueLight.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/blueNeedle.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/knob.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/redLight.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/redNeedle.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/yellowLight.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Modern/yellowNeedle.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Speed/backOff.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Speed/backOn.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Speed/needle-off.png</file>
        <file>RoniaKit/Gauges/assets/images/gauge/Speed/needle-on.png</file>
        <file>RoniaKit/qmldir</file>
    </qresource>
</RCC>
```

---

## **Step 5: Register the Module in `main.cpp`**
- Add the module to your Qt engine to ensure it can locate the resources.
- Use the following code snippet in your `main.cpp` file (or wherever the engine is initialized):

```cpp
#include <QGuiApplication>
#include <QQmlApplicationEngine>

int main(int argc, char *argv[]) {
    QGuiApplication app(argc, argv);
    QQmlApplicationEngine engine;

    // Register the RoniaKit module
    engine.addImportPath("qrc:/RoniaKit");

    engine.load(QUrl(QStringLiteral("qrc:/main.qml")));
    if (engine.rootObjects().isEmpty())
        return -1;

    return app.exec();
}
```

---

## **Step 6: Add the `RoniaKit.pri` to Your `.pro` File**
1. Open your `.pro` project file.
2. Add the following line to include the `RoniaKit.pri` file:
   ```pro
   include(RoniaKit/RoniaKit.pri)
   ```

---

## **Final Checklist**
- [ ] Subfolder `RoniaKit` created and contains the required files.
- [ ] `qmldir` copied to the `RoniaKit` directory.
- [ ] Resource file (`qml.qrc`) updated with a new prefix `/RoniaKit`.
- [ ] All files from the `RoniaKit` subfolder added to the resource file.
- [ ] `main.cpp` updated to register the module with `engine.addImportPath()`.
- [ ] `.pro` file updated to include the `RoniaKit.pri`.

Once all these steps are completed, the **RoniaKit** module will be successfully integrated into your QMake project.