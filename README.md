# ServerBrandFork

Кастомный Server Brand, немного перебрал оригинальный плагин и обновил библиотеки чтобы он мог работать с новым BungeeCord/Waterfall и Spigot/PaperMC

![](https://i.imgur.com/YIpk7nK.png)

## Как использовать
### Config
```yaml
# The string to display in the debug menu.
# On bungeecord you can use %%server%% to insert the brand coming from the backend server, eg to show the instance id
brand: "My Server"
```

### API
#### Bukkit/Spigot/Paper
```java

import org.bukkit.plugin.java.JavaPlugin;
import me.theminecoder.minecraft.serverbrand.ServerBrandAPI;

public class MyPlugin extends JavaPlugin {
    
    public void onEnable() {
        ServerBrandAPI.getInstance().setBrand("My Custom Brand");
    }
    
}
```

#### Bungeecord/Waterfall
```java

import net.md_5.bungee.api.plugin.Plugin;
import me.theminecoder.minecraft.serverbrand.ServerBrandAPI;

public class MyBungeePlugin extends Plugin {
    
    public void onEnable() {
        ServerBrandAPI.getInstance().setBrand("My Custom Bungee Brand -> %%server%%");
    }
    
}

```
