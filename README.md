# Hyprland's dotfiles
## Prerrequisitos
Para crear el entorno se requiere de:
```bash
sudo pacman -S hyprland pipewire wireplumber brightnessctl
```
> [!NOTE]
> Solo se requiere de `brightnessctl` en el caso de tener un portatil con una pantalla LCD.

En mi caso, uso Waybar para la barra de tareas, Kitty como emulador de terminal, Rofi (en su versión para wayland) como menú de aplicaciones, Dolphin como gestor GUI de archivos, Grim y Slurp para capturas de pantalla, Hyprpaper para tener fondos de pantalla personalizados y Zen como navegador web.
```bash
sudo pacman -S kitty waybar hyprpaper rofi-wayland grim slurp dolphin
yay -S zen-browser-avx2-bin
```
> [!TIP]
> En caso de preferir otras opciones, podrás revisarlas en la wiki de Hyprland o en otras páginas. Mientras se sepa que tienen soporte a Wayland, debería funcionar.

> [!IMPORTANT]
> En caso de instalar otros programas, deberás cambiarlo en [los atajos de teclado](shortcuts.conf) y en [el inicio automatico](autostart.conf)

## Instalación
Primero descargamos el repositorio:
```bash
git clone https://github.com/RayanBel/Hyprland-dotfiles
```
Para tener todo configurado, podemos copiar manualmente los archivos o por comandos (sin antes crear la carpeta `~/.config/hypr/`);
```bash
cp *.conf ~/.config/hypr/
```
Otras opciones más interesantes serían vincular el repositorio local con la carpeta. En ese caso ejecutamos el archivo [install.sh](install.sh). También podemos hacerlo directamente.
```bash
ln *.conf ~/.config/hypr
```

## Ejecución

Para finalizar, ejecutamos Hyprland con la configuración nueva.
```bash
hyprland
```
En caso de que ya se esté ejecutando, podemos actualizarlo así:
```bash
hyprctl reload
```
En caso de únicamente querer ver la configuración sin instalarla, podemos especificarle que la use así:
```bash
hyprland -c hyprland.conf
```
> [!IMPORTANT]
> Se presupone en todo momento que estamos en el directorio del repositorio. Se ha de ejecutar este último comando desde ahí o cambiando la dirección hacia dónde está la configuración.

## Documentación
En caso de requerir de más información, he aquí una lista de enlaces de interes:

- [Hyprland wiki](https://wiki.hyprland.org/)
- [Compatibilidades con Wayland](https://wearewaylandnow.com/)
- [Página de la Arch Wiki de Hyprland](https://wiki.archlinux.org/title/Hyprland)