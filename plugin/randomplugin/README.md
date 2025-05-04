# Download correct versions of files to project
arapi<version>.jar
arutil<version>.jar
arpluginsvr<version>.jar

These can be copied from container running ar-server (copy files to bmcapi-folder inside randomplugin folder):
    podman cp ars-arserver-arserver:/opt/bmc/ARSystem/api/lib/arapi251_build001.jar .
    podman cp ars-arserver-arserver:/opt/bmc/ARSystem/api/lib/arutil251_build001.jar .
    podman cp ars-arserver-arserver:/opt/bmc/ARSystem/pluginsvr/arpluginsvr251_build001.jar .

2. Kompilera java-filen
    javac -cp "bmcapi/arapi251_build001.jar:bmcapi/arutil251_build001.jar:bmcapi/arpluginsvr251_build001.jar" -d classes RandomNumberPlugin.java

3. Skapa jar
    jar cf randomplugin-dynamic.jar -C classes .


# Bonus

Verifiera jar-filen:
    jar tf randomplugin-dynamic.jar