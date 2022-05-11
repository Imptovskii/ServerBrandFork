# /new places/ ServerBrand

Кастомный Server Brand, немного перебрал оригинальный плагин и обновил библиотеки чтобы он мог работать с новым BungeeCord/Waterfall и Spigot/PaperMC

![изображение](https://user-images.githubusercontent.com/82046704/167948394-4d6ff402-94f8-43f6-a093-568f1d040c52.png)

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
