# MMOEssentials
MMOEssentials is a Bukkit plugin / library that gives you resources needed to create an MMORPG gamemode in minecraft.
This documentation will give you examples and explain what code does from the Library.

#Getting Started
In order to begin setting up, simply import MMOEssentials as an external archive in your project using your IDE.

#Configs (Avaliable since version 1.0)
In order to create or initialize a config, create a config variable, the name is simply just "Config". Example:
```sh
Config c = new Config("test.yml", "Test Plugin");
```
"test.yml" is the file name of your config. This can be almost anything.
"Test Plugin" is the folder you want your configuration to be in, inside of the plugins folder.

In order to set, or get a configuration variable, you will first need to get the config, this can be done using .getConfig(); Example:
```sh
c.getConfig();
```
To actually modify or recieve variables from the config you'll need to use set(); tochange something, and getInt(), getString(), or whatever type of variable you are getting from the config.
```sh
int a = c.getConfig().getInt("configA");
a += 1;
c.getConfig().set("configA", a);
```
To save these changes to the configuration file, you just need to do save the config.
```sh
c.saveConfig();
```
You may also delete the config. However it's experimental.
```sh
c.delete();
```
