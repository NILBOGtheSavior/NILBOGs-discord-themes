# NILBOGs-Discord-Themes

![Header](/img/NILBOG's-discord-themes.png)

> [!WARNING]  
> This is still in beta. Themes may not work as expected.

Welcome to the official repository for NILBOG's Discord Themes! This theme pack is designed to give your Discord interface a cleaner, more modern look, with a minimalist feel. On top of that, it lets you show off your favorite fandom with custom themes that add a personal touch to your experience.

*These themes take advantage of plugins and window transparency to help boost the asthetic, however, it is not mandatory for all themes. Check the table below to see what features are available for each theme.*

## Available Themes
[[Preview Themes]](./THEMES.md)

| Standard Themes | Tags                  |  | Crossover Themes   | Tags                     |
|-----------------|-----------------------|--|--------------------|--------------------------|
| Acrylic         | `Transparent`         |  | Razer              | `Transparent` `Plugin`   |
| Space Age       | `Coming Soon`         |  | One Piece          | `Transparent` `Opaque`   |
|                 |                       |  | Ahri (LoL)         | `Coming Soon`            |
|                 |                       |  |                    |                          |

## Installation Instructions

`Windows` `Mac` `Linux`

### 1: Install Discord mod of your preference

- Install either Vencord, BetterDiscord, or Powercord.

> <img src="https://vencord.dev/assets/logo-nav-oneko-padding.png" alt="Vencord" height="25"/>   [Vencord](https://vencord.dev/)

>> <img src="https://betterdiscord.app/resources/branding/logo_small.svg" alt="BetterDiscord" height="25"/>   [BetterDiscord](https://betterdiscord.app/)

>>> <img src="https://avatars.githubusercontent.com/u/46755359?s=48&v=4" alt="Powercord" height="25"/>   [Powercord](https://betterdiscord.app/)

### 2: Install the theme pack

You may decide whether you would like to install the entire theme pack, or just a few.

- #### Vencord
1. Navigate to **User Settings > Vencord**
2. Check `Enable Custom CSS` and `Enable window transparency`. You may need to restart Discord.
3. Navigate to **Themes**.
4. Click on the `Open Themes Folder` button.
5. Move the `themes/____.css` files from this repository into the `Vencord/themes/` directory.
6. Enable the theme in the Vencord settings.

- #### BetterDiscord
1. Download the `themes/____.css` file.
2. Place it in the BetterDiscord themes folder:
   - **Windows**: `%AppData%\BetterDiscord\themes`
   - **Mac/Linux**: `~/.config/BetterDiscord/themes`
3. Enable the theme in the BetterDiscord settings.

- #### Powercord
1. Clone this repository into your Powercord `themes` folder:
   ```bash
   git clone https://github.com/NILBOGtheSavior/NILBOGs-discord-themes.git ~/.powercord/themes/custom-css
2. That was easy...

## Background Blur (Optional)

`Windows` `Linux`

Some of the transparent themes are slightly difficult to read in front of certain windows or wallpapers. To fix this issue, you can apply a background blur to your Discord window. To add background blur to your Discord, identify your operating system below and follow the instructions.

- ### Windows
1. Download [MicaForEveryone](https://github.com/MicaForEveryone/MicaForEveryone).

> [!CAUTION]
> Make sure you download the latest *stable* release. Previews are often incomplete and may cause issues during daily use.

2. Launch the app and look through general settings. I recommend checking `Run on Startup`.
   - ![Mica](img/tutorial/mica.png)
3. Click on the `+` button on the bottom left of the window, then on `Add Process Rule`. Enter **'Discord'** as the process name.
   - ![addRule](img/tutorial/addRule.png)
   - ![processName](img/tutorial/processName.png)
4. Turn `Blur Behind` on.
   - ***Optional:** Turn on `rounded edges`.*
   - ![blurBehind](img/tutorial/blurBehind.png)

- ### Linux
   #### Debian/Ubuntu
1. Install [GNOME Shell extensions](https://extensions.gnome.org/).
2. Install the [Blur my Shell](https://extensions.gnome.org/extension/3193/blur-my-shell/) extension.
3. Open the **Extensions** manager program, find `Blur my Shell` and click `Settings`.
4. Under `Applications > Whitelist`, click `+ Add Window` and select **Discord**.
- #### Arch Linux / NIX OS
1. Install `picom` with `sudo pacman -S picom`.
2. Use your preferred text editor to edit the `~/.config/picom/config.conf` file.

   - `sudo vim ~/.config/picom/config.conf`
   - Search for the `rules` section:
   ```
   rules: ({
      ...
   });
   ```
   - Add a rule to apply background blur on discord:
   ```
   rules: ({

   }) ({
      match =
      "class_g = 'discord'";
      background-blur = 10px;
   })
   ```
   - `:w` save and `:q` quit the text editor.
3. Set `picom` to launch on startup in your Window Manager's config file, or use a service like x-startup to automatically launch when your computer boots up.
   - For example, in `~/.config/i3/config`, add this:
   ```
   exec picom;
   ```
4. Terminate and relaunch `picom`:
   ```
   pkill picom
   ```
   ```
   picom &
   ```

## Conclusion

Congratulations, your Discord client now officially looks awesome! Your experience should now be cleaner, modern, and personalized to your liking.

If you ever find that the theme isn’t displaying as expected, double-check that your CSS file is properly linked and that the theme is enabled through your Discord settings.

In case the theme still isn’t working right, check for any conflicts with other installed themes or extensions. A quick restart of Discord can often resolve minor issues. If you're having trouble with specific customizations, feel free to revisit the installation steps or refer to the troubleshooting section for more detailed guidance.

Enjoy your new look and feel free to customize further as you see fit!

### Quick Links

- [Preview](THEMES.md)
- [Troubleshooting](man/TROUBLESHOOTING.md)
- [NILBOG's Discord Server]()
