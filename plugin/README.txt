# RandomPlugin - Manual Build Instructions

## Requirements:
- Java Development Kit (JDK) installed (javac and jar in PATH)

## Files:
- RandomNumberPlugin.java

## Build Instructions (Linux/Mac):
```bash
mkdir classes
javac -d classes RandomNumberPlugin.java
jar cf randomplugin-dynamic.jar -C classes .
```

## Plugin Configuration (pluginsvr_config.xml):
<plugin>
  <name>RandomPlugin</name>
  <classname>com.example.RandomNumberPlugin</classname>
  <pathelement type="location">/opt/bmc/ARSystem/pluginsvr/randomplugin-dynamic.jar</pathelement>
</plugin>

Then restart your plugin server:
  systemctl restart arplugin