# hlx-standup
Helix Innovation Suite (Action Request System) application for daily stand up


# Installation
1. Import the AR application
2. Configure your users and groups from application home page "HLX:Standup:Home" via the settings button. 
The value of "Login" must be same as logged in user
3. Ready to go! Have fun!



# RandomNumber plugin

Add this to pluginsvr on AR Server plugin

<plugin>
  <name>RandomPlugin</name>
  <classname>com.example.RandomNumberPlugin</classname>
  <pathelement type="location">/opt/bmc/ARSystem/pluginsvr/randomplugin-dynamic.jar</pathelement>
</plugin>
